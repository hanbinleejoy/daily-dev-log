# Scheduling에 대한 프로젝트 적용

<br>

## Controller에 Scheduling 적용 (Java)

```java
@Scheduled(cron = "0 30 16 20 2,5,7,11 *", zone = "Asia/Seoul")
public ResponseEntity<String> bulkUpdate() 
        throws JsonParseException, JsonMappingException, IOException {
    //...
}
```
- 주기적으로 자동 실행하고 싶은 메서드에 `@Scheduled` annotation을 적용
- 그 전에 Spring Boot Container에 Scheduling 기능을 사용하겠다고 알려야 한다.

```java
@SpringBootApplication
@EnableScheduling
public class QuantApplication {

	public static void main(String[] args) {
		SpringApplication.run(QuantApplication.class, args);
	}
}
```
- `@EnableScheduling`를 설정함으로써 Container에게 알려준다.

<br>

## Ubuntu Linux내 `crontab` 설정시 유의사항

linux OS에서 `crontab`을 통해 scheduling을 설정할 수 있다.

```cmd
$crontab -e (scheduling할 명령어 설정, vim형식)


$crontab -l (scheduling했던 설정 내용들 확인)

35 11 30 7 * python3 /home/ec2-user/app/diq/web_crawling_logo.py
20 12 30 7 * aws s3 sync /home/ec2-user/app/diq/data/logo/ s3://webservice-image-bucket/do-it-quant --acl public-read
```

여기서 유의할 것은 `crontab -e` 명령어를 통해 설정하는 내용 중 directory path 설정하는 부분이다.  
상대경로가 아닌 **절대경로**를 기준으로 file path를 설정해야 한다.

```python
# jongmok_code = ExcelRead("./data/sangjang_jongmokCode.xlsx")
jongmok_code = ExcelRead("/home/ec2-user/app/diq/data/sangjang_jongmokCode.xlsx")
```
- `./data`로 설정하면 해당 디렉토리에서 python 명령을 통한 실행은 가능하지만 crontab상에서는 인식을 못한다.
- 절대경로로 설정해주어야 한다.

<br>

#### crontab 관련 참고 블로그
[리눅스 반복 예약 작업](https://zetawiki.com/wiki/%EB%A6%AC%EB%88%85%EC%8A%A4_%EB%B0%98%EB%B3%B5_%EC%98%88%EC%95%BD%EC%9E%91%EC%97%85_cron,_crond,_crontab)
