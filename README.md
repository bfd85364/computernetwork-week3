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

TCP: 연결지향 

UDP: 비연결지향

SCTP: 멀티미디어 제공용 (제공하는 자료를 미리 버퍼해서 가져옴)

# 네트워크 계층

기계 vs 기계 

호스트 vs 호스트 통신 

발신지에서 목적지까지 경로상의 라우터들은 최선의 경로 선택 책임 

인터넷 프로토콜(IP)

 ICMP, IGMP, DHCP(데이터 링크계층), ARP: address를 해결하기 위한 프로토콜

 R(reverse)ARP: rkxdms tjqj soidptj thrgks rocpdml ㅁㅇㅇㄱㄷㄴㄴfmf tjfhtjfh rkwudhrl dnlgka 
 
 MAC Address -> 유일한 address로 lan카드에 이식됨 -> 통신간 충돌이 일어나지 않게 하기 위해 

데이터 링크 계층 

테이터그램을 받아서-> 프레임이라는 패킷으로 캡슐화 

꼬리가 붙는다. -> 여기에는 "오류해결 코드"가 첨부되어 있다.

 
