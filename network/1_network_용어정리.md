# Network 주요 용어 정리

## 🔖 네트워크의 정의

**전송 매체(Transmission Media)** 를 매개로 **서로 연결(Interface)** 되어 데이터를 교환하는 **시스템(System)** 의 모음  
시스템끼리 데이터 교환하게끔 해주는 인프라라고 할 수 있다.


#### 시스템(System)
- 내부 규칙에 따라 능동적으로 동작하는 대상을 가리킨다.
- **물리적 대상**: Computer, Micro-processor, Hard-disk, Machine...
- **논리적 대상**: 운용체제, 프로세스, 운영 시스템 등...
- `외부 입력` + `내부 정보` 조합에 따른 `출력(결과물)`이 존재할 수 있다.

#### 인터페이스(Interface)
- **시스템과 시스템을 연결하기 위한 표준화된 접근 방법**
- 상호 연결을 위한 서로 간의 약속
- 물리적(잭의 크기 등), 논리적(RS-232C, USB 등) 규격의 표준화 필요

#### 전송 매체(Transmission Media)
- 시스템끼리 정해진 인터페이스를 연동해 데이터 전달할 때 필요한 **물리적인 전송 수단**
- 동축 케이블, 소리를 전파하는 공기, 무선 신호 등 다양함

#### 프로토콜(Protocol)
- 네트워크를 통해 데이터를 교환할 때 따르는 표준화된 특정 규칙
- 동등한 위치에 있는 시스템 사이의 규칙(주종 관계 X)
- (연동을 위한 접촉 지점보다) 주고받는 정보의 형식, 일련의 절차적 순서에 무게를 둠

#### 인터넷(Internet)
- **IP(Internet Protocol)**의 Internet에서 유래
- 전 세계 모든 네트워크가 유기적으로 연결되어 동작하는 통합 네트워크

<br>

## 🔖 시스템 관련 용어

일반적으로 컴퓨터 시스템으로 생각한다.

#### 노드(Node)
- 인터넷에 연결된 시스템을 **가장 일반화한 용어**
- 데이터를 주고받을 수 있는 모든 시스템을 통칭

#### 호스트(Host)
- **컴퓨팅 기능이 있는 시스템**(연산기능 등을 수행할 수 있는 능력)
- 사용자가 네트워크에 접속하는 창구 역할

#### 클라이언트(Client)
- 호스트 사이에 제공되는 서비스를 기준으로 서비스를 이용하는 시스템
- 클라이언트와 서버는 고정적인 개념 X
- 이용하는 서비스의 종류에 따라 클라이언트, 서버 둘다 될 수 있음

#### 서버(Server)
- 호스트 사이에 제공되는 서비스를 기준으로 서비스를 제공하는 시스템
- 마찬가지로 고정적인 개념 X

#### 클라이언트 - 서버 관계
- 클라이언트와 서버는 서비스 이용의 상대적 위치에 따라 결정된다.
  - FTP 서비스를 기준으로 A가 서버, B가 클라이언트 / 텔넷 서비스 기준으로 B가 서버, C가 클라이언트라고 한다면  
    B는 서비스에 따라 클라이언트, 서버 둘다 될 수 있다.
- 호스트에서 실행되는 **운용 서비스별**로 구분하는 것이 정확
- **클라이언트 프로세스**, **서버 프로세스**라는 호칭이 정확

<br>

## 🔖 시스템 관련 용어

#### 인터페이스(Interface)
