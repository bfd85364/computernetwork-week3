
# Computer-network_week1
컴퓨터와 네트워크 1주차 정리노트 

-통신 수단의 성능 평가 기준 
초당 전송량, 안정성 
+많은 송수신측

통신모델1
송신측(Source) 전달될 데이터를 생성 -> 송신기가 전달할 데이터를 신호로 변환 -> 전송시스템 -> Receiver -> Destination(수신측)

일반적으로 통신은 N:N 

->1:1 통신의 예시로는 군용 무전기 (PRC-96k)

통신공학에서 중요한거 

name, adress -> DNS 방식  

데이터의 손상을 대비 -> 오류발견 및 회복 

주소방식과 라우팅

(해당 과목에서 보안은 안 배움) 

통신모델3

source(input info)---->//Digital bit stream//-----> Transmiter(input data)------>//Analog//----->transmissionsystem------->//Analog//-----> Receiver-> Destination 

네트워크 VS 네트워킹 

가장 비효율적인거---> point-to-point(점대점) 방식 ---> 송수신측관 통신선을 직접 "물리적"으로 연결하는 것은 비현실적.
                    (가상으로 연결선을 잇는건 가능)

물리적으로 연결해야 한다면----> 중앙 교환장치(TRANSMISSION SYSTEM) 필요 
ex) switch


-크기- 

LAN =  근거리 통신 

MAN = 대도시 통신

WAN = 광역 통신

-교환방식-

Circuit Switching : 전달하려는 메세지를 그대로 보냄 

Packet Switching :전달할려는 메세지를 패킷 단위로 분해후 공유되어 수신시 재조립됨

![패킷 스위치 도식화](https://github.com/user-attachments/assets/411ff243-ad15-400e-9892-42982dc111b6)




ex) 송신측 A가 수신측 B에게 메세지를 전달한다고 하면 

A의 메세지 -> (A의 메세지-a), (A의메세지-b), (A의 메세지-c) -> B가 받는 메세지: 재조립된 A의 메세지 (A의 메세지-a, A의 메세지-b, A의 메세지-c)

-통신방식-


A----->B 단방향(simplex) -> 주요 예시: 라디오, TV 


A--------->B, A<--------B 양방향(half duplex) 


A<-------->B 전이중통신(full duplex)

-동작 방식-

동기 

비동기 


-연결제어-

![TCPIP 전송](https://github.com/user-attachments/assets/a1be9f01-af5c-4328-b30a-196b25a324e1)

연결지향형

1.연결설정 (연결요청 --->  확인)


2.DATA 전송  (데이터 전달---> 확인)


3. 연결해제
   

연결 지향형 특징

-data 경로대로 순서대로 전달됨 (절차적임)  

(연결요청 ---> 확인 -----> 데이터 전달----> 확인 ------> 연결해제) 

-전송속도가 느리다, 규모가 크기 때문에 비용이 많이 든다. 

-경로 설정이 되어있어 전송이 확실함 (비연결형 보다는) ----> 신뢰성이 있다. 

-연결 지향형 예시) 패킷 스위치(연결지향형), PSTN(전화망: 회선교환방식), TCP



비연결형

-비용이 적게 든다. 

-주로 작은 단위의 데이터를 보낼때 사용한다.

-연결 지향형보다는 전송이 불확실하다. 

-비연결형 예시) UDP


# 주소방식-DNS
Name->address로 바뀌어야만 찾아갈수 있다.
DNS(Domain Name server: Name을 address로 변환 하는 형식의 주소지정 방식

참여하고 있는 송수신책은 주로 Address로 분류됨


NIC(Network interface card):또 다른 주소방식을 사용함 MAC address 사용
MAC address는 재사용이 불가하다 

# programing language
1. syntax (구문)
2. data (데이터)

--------------------------------

# protocol 
1. syntax (구문)
2. data (데이터)
3. timing (시간)

인터넷 계층- 네트워크 계층 
응용계층- 웹 브라우저 접속, 이메일, 파일 전송 p2p(토렌토)
전송계층-TCP/IP의 TCP 부분 UDP도 해당계층에 포함된다  


----------------------------------------------------------------------------------------------------------------------------------

# computer-networking-week2

# 컴퓨터와 네트워크 2주차 정리 노트

# OSI 7계층->이거 시험에나옴 

응용(application)->표현(presentation)->연결(session)->전송(transport)->네트워크(network)->데이터링크(DL)->물리(Physical)  

물리계층은 신호만 존재하기 때문에 header를 붙이지 않음 

(그리고 헤더는 생각보다 크지 않다)

AH: header: user data->PH: presentation: Application Protocol Data Unit(A-pdu)-> SH: Session header (p-pdu) -> NH: Tranport-pdu(T-PDU) -> N-PDU -> DL-PDU

-OSI(국제전기통신표준기구)

-기존 네크워크 장비(이진 네트워크 장비) -> 같은 회사가 아니면 호환이 잘 안됨

따라서 이런 하드웨어적, 소프트웨어적 호환성 문제를 해결하기 위해 ('상호개방'을 통해 이질적인 네트워크를 연결하기 위해) 
-> 이를 위해  엔지니어들과 개발자들이 모여서 회의 -> 이를 표준화 하여 네트워크 시스템을 개방화시킴

-표준화 기준-

-규격의 범위와 적용
-상호 연결시 적합성을 위한 공통된 토대 마련


# Reference Model(참조 모델)

# 미리 잘 설계할 개념 필요 
  -Layering (계층화)
  -Abstraction (추상화)

# 계층화
  -각 계층의 기능에 대한 (독립성)을 최대화 (별도의 장비와 각각의 기능을 분리) -> (But) 유사기능은 동일 계층에 정의

  IBM의 360모델-> 성능은 뛰어나지만, 기능 구현에만 몰두하여 OS 호환성 문제가 생김

  (주의) 새로운 기능을 추가하기 위해서는 모듈화가 되어야 한다. 

  -인접 상하위 계층에 대한 "인터페이스" 정의

  Abstraction 추상화

  상위->하위계층에 대한 서비스 게공 
  하위-> 상위계층에 서비스 제공



  계층 & 추상화 

송신측
  의미계층 -> 언어계층-> 음성계층 ->


  <- 물리 계층->

수신측
  음성계층 -> 언어계층 -> 의미계층

(대화는 같은 계층끼리만 가능하다)


같은 계층끼리 수평관계 대화하면 -> protocol(프로토콜) -> Peer-to-peer (같은 계층끼리) -구성요소: Syntax:구문--> ex) 주요언어: CHILL, Estelle Lotos, -Data: 정보->Abstract ASN.1, Timing: 순서 시간  

각기 다른 계층끼리 수직적인 관계 -> 서비스 (서비스 접근점으로만 제공가능 SAP)

쉽게 말해서 프로토콜 방식은 내가 신관캠 중앙도서관 3층에서 천암캠 도서관의 3층까지 이동하는 방법과 같다. 


엘레베이터를 타고  신관캠 4층에서 엘레베이터를 타고 (중간에 목적지 같은 이름 모르는 타과학생들도 3층에서 타고 -> 2층에서 타고 -> 1층 도착) 천안캠 가는 셔틀을 탄후-> 천안캠 도서관 1층에서 나는 다시 4층으로 올라간다. (중간에 신관캠 3층에 탔던 사람들은 3층에서 내리고, 2층에서 탄 사람은 2층에서 내린다.)


4(transport) -> [0][1][2][3][4]
session 전송 계층 
ex)Q.o.s (Quality of service)

Protocol Engineering 프로토콜 엔지니어링 기준

- 두 시스템의 같은 계층에 대한 통신 
- 서로 다른 운영체제 에서도 동작가능
- 프로토콜 기술문서에서는 다음 사항을 포함 


TCP/IP->얘는 국방부 표준임, 국재표준기구 아님 (그래도 호환은 됨)


# 네트워크 릴레이(중계) - 네트워크를 연결하는 방법 

1. 네트워크 상의 어떠한 문제가 있는지 진단하고 해결해가는 과정

2. 릴레이 구성 : 물리계층: 반복자(Reapeter), 데이터 링크 계층 브리지(bridge), "네트워크 계층": Router(설계 후 선택), Gate_Away(경로 설정)

# 물리계층
  -Reapeter-
물리계층에서, 그리고 또 하나의 네트워크에서 다른 네트워크로 전송할때 거리의 제약에 따라 감쇄된 신호를 복구해주는 역할

# 데이터 링크 계층
 -Bridge-
데이터 링크 계층에서 하나의 네트워크 프레임을  복사하여 다른 네트워크로 전송해주는 역할

*****그러나 bridge는 reapeater의 기능도 포함할수 있다*****

ex)

Token ring ------------> Bridge ---------------> Token Bus

(서로 다른 네트워크를 연결할 때 Bridge가 필요하다) --> 왜냐화면 미리 Access control 하기 때문이다. 
따라서, 이전 논리 계층에서의 프레임을 그대로 전송해야하기 때문이다.


# 네크워크 계층
-router-
네트워크 계층에서 경로를 설정 (개설)
만약 설정된 경로거 많다? -> 라우터도 많아진다. 


-GateWay-
네트워크 계층에서 단순한 연결(relay)뿐만이 아닌 신호를 변환(conversion)하고 번역(translate)하는 기능도 함 

# Gate way-관문국

-conversion-
데이터 형식을 디지털 (digit:0100) -> 아날로그 (4)로 변환

-Translation-
데이터 형식이나 주소체계등을 번역해줌 (암호체계가 다를 경우 중간에서 바꾸어줌) 


# Encryption, Decryption

Encryption: 암호화(Encoding)

Decryption: 복호화(Decoding) 

![암호화와 복호화](https://github.com/user-attachments/assets/b6bbaed8-65ca-4d60-bd43-9bd083a035fe)


# 네트워크의 구현과 관련하여 

-하드웨어-

1.물리 계층-Reapeater

2.데이터링크 계층-Bridge(허나 부분적으로 소프트웨어로도 구현됨)

-소프트웨어 (주로 네트워크 계층 애들이 이렇게 구현됨) 

1.네트워크 계층-Router

2.네트워크 계층-GateWays 

(대부분의 라우터와 게이트웨이는 소프트웨어로도 구현됨) 


# Byte Ordering

-16bit int 표현할 때 

![byte 우선순위](https://github.com/user-attachments/assets/e667e327-263d-4069-a283-7f11d7f89aac)

*실제 저장 방식은 CPU에 따라 다릅니다. 


-과거: High byte 위주-

Big-Endian 방식

[[High Byte: Addr A(1)][Low Byte: Addr A+1(7)]]

빅 인디안 방식이 채택된 모델들: IBM360, 370 시리즈, Motorola 68000, Sun


-현재 Low Byte 위주-

[[Low Byte: Addr A(7)][Low Byte: Addr A+1(1)]]

Intel 80x86, DEC VAX, DEC PDP-11


# 그렇다면, 표현 방식이 다른 메모리의 데이터를 PDU로 인코딩 할때는 어떻게 해야하나?

진법 변환으로 각각의 (4)Byte를  (2)bit 단위로 바꾸어줘야 한다


ex) 32bit <---> 4byte (1byte == 8bit)


# 그렇다면, TCP-IP 프로토콜 네트워크에서는 뭘 쓰는가?

현재 대부분의 컴퓨터는 Intel의 Little-Endian 방식을 사용함 

-----> 아쉽게도 TCP-IP는 Big-Endian 방식을 사용함 


(송신)Little-Endian ->(변환)Big-Endian->(변환)Big-Endian->(수신)Little-Endian

-------------------------------------------------------------------------------------------------------------------------------------------------------
# computernetwork-week3

# programing language
1. syntax (구문)
2. data (데이터)

--------------------------------

# protocol 
1. syntax (구문)
2. data (데이터)
3. timing (시간)

----------------------------------------------------------------

인터넷 계층- 네트워크 계층 
응용계층- 웹 브라우저 접속, 이메일, 파일 전송 p2p(토렌토)
전송계층-TCP/IP의 TCP 부분 UDP도 해당계층에 포함된다  


data-link :Switch


# 응용계층 

-프로세서 단위로 처리해야함
-메시지교환
-계층간 논리적인 연결 종단-대-종단
-프로토콜: HTTP, SMTP(이메일전송방식), telnet, SSH(Secure server-보안기능), SNMP(망 관리 프로토콜), DNS

PING:
1. 연결하는 접속이 가능한지 확인
2. 연결하는 네트워크에 응답을 확인

# 전송 계층 

응용 계층에 서비스 제공 책임 

TCP: 연결지향 (데이터의 크기가 클때)

# 연결지향형의 단계

 1.연결설정 (연결요청 ---> 확인)
 2.DATA 전송 (데이터 전달---> 확인)
 3.연결해제

연결 지향형 특징 -data 경로대로 순서대로 전달됨 (절차적임) (연결요청 ---> 확인 -----> 데이터 전달----> 확인 ------> 연결해제)

UDP: 비연결지향 

-비연결형-> 단일개체 전송시-

-단점: 불확실함-

Time to Live(생존시간) -> 노드를 거칠때마다 전송비용을 지불 (무조건 도착전까지 비용을 아껴야함) 

SCTP: 멀티미디어 제공용 (제공하는 자료를 미리 버퍼해서 가져옴)

# 네트워크 계층

기계 vs 기계 

호스트 vs 호스트 통신 

발신지에서 목적지까지 경로상의 라우터들은 최선의 경로 선택 책임 

인터넷 프로토콜(IP)

 ICMP, IGMP, DHCP(데이터 링크계층), ARP: address를 해결하기 위한 프로토콜

 R(reverse)ARP: 같은 서버 내에 속하는 개체의 address를 서로서로 가져위한 프로토콜
 
 MAC Address -> 유일한 address로 lan카드에 이식됨 -> 통신간 충돌이 일어나지 않게 하기 위해 

데이터 링크 계층 

테이터그램을 받아서-> 프레임이라는 패킷으로 캡슐화 

꼬리가 붙는다. -> 여기에는 "오류해결 코드"가 첨부되어 있다.

Service Acess Protocol -> 운영체제의 형태로 구현되어 있다.

 -TCP IP 그룹-

 FTP, HTTP -> TCP


 TCP-> 연결 지향형


# Internet 

1960년 전신과 전화망 같은 통신망 존재 




