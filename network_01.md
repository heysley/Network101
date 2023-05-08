# 0418 네트워크

복습: No
유형: 이론
작성일시: 2023년 5월 2일 오전 8:07

<aside>
💡 [https://www.youtube.com/playlist?list=PL7zRJGi6nMRzg0LdsR7F3olyLGoBcIvvg](https://www.youtube.com/playlist?list=PL7zRJGi6nMRzg0LdsR7F3olyLGoBcIvvg)

</aside>

<aside>
💡 [https://www.brianlinkletter.com/open-source-network-simulators/](https://www.brianlinkletter.com/open-source-network-simulators/)

</aside>

**[🦈](https://www.emojiall.com/ko/emoji/%F0%9F%A6%88)** <**WIRESHARK>**

>캡쳐-옵션 - enable promiscuous mode on all interfaces 혼잡 모드. 내 것 아닌 패켓도 다 받을 건가

<aside>
💡 [https://e-koreatech.step.or.kr/page/lms/?m1=course%25&m2=course_detail%25&course_id=170317](https://e-koreatech.step.or.kr/page/lms/?m1=course%25&m2=course_detail%25&course_id=170317)

</aside>

<aside>
💡 [https://www.youtube.com/playlist?list=PL30o9a_lTg-KN4UmwKj2txuY3Vrd1nMrx](https://www.youtube.com/playlist?list=PL30o9a_lTg-KN4UmwKj2txuY3Vrd1nMrx)

GNS 강좌 : 

</aside>

<aside>
💡 [https://www.netacad.com/courses/packet-tracer](https://www.netacad.com/courses/packet-tracer)

또는 cisco 패킷트레이서 사용 : 

</aside>

<aside>
💡 [https://www.youtube.com/playlist?list=PLxbwE86jKRgMpuZuLBivzlM8s2Dk5lXBQ](https://www.youtube.com/playlist?list=PLxbwE86jKRgMpuZuLBivzlM8s2Dk5lXBQ)

CCNA 강좌 : 

</aside>

# **OSI 7 LAYERS**

***open system interconnection***

현재는 **TCP/IP 프로토콜** 스택 사용(4계층)
네트워크 액세스 - 인터넷 - 트랜스 포트 - 애플리케이션

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled.png)

**IPsec** : *IP security* 네트워크 계층

**SSL** : 

*Secure Sockets Layer* 데이터 암호화. 보안. 안전. 웹페이지가 안전함. 인증서 사용 

https → TCP443
http → TCP80

응용 프로세서의 데이터전송> 다른 응용 프로세스 전달 가능. 포트번호 사용(프로세스 구별)

**TCP** : 제어O. 전송 제어 프로토콜. 오버헤드o(신뢰성). 연결 지향형 서비스.

**UDP :** 제어X. 정보 오픈. 간단한 메세지. ex)라디오. 제어 없이 보냄 → 통신 속도 빠름. 

오버헤드x(연결보장, 신뢰성). 비연결성. 비연결형 IP전달 서비스 + 검사합 기능
응용프로그램 간단해짐. 시간에 민감한 전송에 사용. ex) 스트리밍 서비스
**[발신지포트 | 목적지포트] [전체길이 | 검사합] [데이터] […]** 16 16 | 16 16 | 32 | 32
* 가짜헤더 pseudo header : 검사합 계산용 12바이트 가짜헤더 사용. 
2중 확인 [가짜 | 진짜]
** udp는 ip주소 없고 포트번호만 있음.*
*process-to-process* P2P 
서버는 잘 알려진 포트, 클라이언트 프로세스는 임시 포트 번호 사용

**IP** : 주소. 제어X. host-to-host

**NAT** *network address translation* 네트워크 주소 변환

내 ip주소를 외부에서는 다른 주소로 보이게 변경

사설 네트워크에 속한 여러 개의 호스트가 하나의 공인 ***IP*** 주소를 사용하여 인터넷에 접속

**비연결형 서비스** : **UDP**

인터넷 계층의 투명성. IP는 호스트 주소 지정, 데이터그램 전송.

경유해야하는 데이터 링크, 라우터 정보 무시. 신뢰성 없음. 빠름. 
중간에 라우터 어쩌고 거침.

**연결형 서비스 : TCP**

**💰**토큰 : 증명해주는

**🍪**쿠키 : 고유한 사용자의 데이터. 사용자 브라우저에 저장.

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%201.png)

같은 : 스위칭

다른 : 라우팅

**TCP/IP 프로토콜** : 

스택은 현재 사용되는 프로토콜 스택 중 가장 일반적. IP 주소와 서브넷 마스크를 설정하여 노드를 구성. 또한 **DHCP**를 사용하여 IP 주소, DNS 서버 및 게이트웨이와 같은 네트워크 정보를 자동으로 할당.

**IP** : 192.168.0.xx IP . 

서브넷 마스크. 이종 네트워크 패킷 전달 필요→비연결형 프로토콜 설계

주소 지정, 패킷 전달. 전달만 할 뿐. 여부는 관심x.
투명성 : 송신자 호스트는 각 데이터그램이 수신자 호스트에 도착하기 위해 경유하는 데이터 링크 및 라우터에 관한 물리적 세부를 몰라도 전송할 수 있게함.  네트워크 계층의 투명성제공
IP계층의 패킷은 데이터그램(헤더 20~60byte)

- ip scanner [https://www.advanced-ip-scanner.com/kr/](https://www.advanced-ip-scanner.com/kr/)
    
    

> 실행 ncpa.cpl 네트워킹 설정

**host-to-host** :

 IP사용. 호스트까지 연결만 해줌. 데이터링크L2→네트워크L3. PACKET

**process-to-process** : 

port번호 사용. 호스트의 포트번호로 해당 응용프로그램. *SOCKET. SEGMENT→DATA

네트워크L3→ 전송계층L4

socket address = ip + port

**FTP : 포트번호 22부터. 소켓 주소(ip주소, port번호)**

**MAC** : 

= BIA burned-in address (정해져 나온다) 상태로 NIC network interface card (랜카드) 에 할당.

00-00-00-00-00-00 16진 12자리 48비트/ 물리 주소 24bit OUI / 제조사 코드 24bit UAA. ip하난데 mac정보 두 개면 최신 할당 받은 ip가 받음.

**DNS :** *domain name system*

**ARP** : *address resolution protocol* 테이블. 주소 결정 프로토콜 

→ IP - ARP - MAC 네트워크 상에서 IP 주소를 물리적 네트워크 주소로 대응(bind). 

요청 : 브로드캐스트(동적바인딩) | 응답 : 유니캐스트

TCP 3계층 논리적 주소 - 이더넷 2계층 물리적 주소 연결

상대방의 mac주소를 질의해야 캡슐화 할 수 있음. arp브로드캐스트를 받은 목적지는 arp프로토콜을 이용해 자신의 mac주소를 응답

**프록시 ARP** : 대신 응답. 같은 소속 네트워크 일 때.

**RARP :** reverse. 

물리주소만 알고 있는 호스트가 자신의 IP주소를 찾을때 사용 프로토콜.

*IP주소는 디스크에 저장된 구성 파일에서 확인.
디스크가 없는 호스트는 물리주소만 알고 있어서 IP주소 얻고자 함.
처음 연결 시. 근거리 통신망. 이더넷, 토큰링, FDDI

**ICMP** : *internet control message protocol*. 인터넷 계층 프로토콜.

**전송 오류 제어**.IP는 비연결성, 비신뢰성(실패 가능성)
오류 발생 시 오류 메세지, 제어 메세지 제공 프로토콜. = IP전송 실패 대신 처리.
**[유형 | 코드 | 검사합] [ICMP메세지] [옵션데이터]** 8 8 16 | 32 | 32
-오류 보고 메세지 - 보고만. 수정 안함.
-질의 메세지 - 일부 네트워크 문제 진단.
오류보고 메세지 : 발신지 억제, 시간초과(TTL), 목적지 도당 불가, 재지정
질의 메세지 : 에코요청 및 응답, 주소 마스크 요청 및 응답, 타임 스탬프 요청 및 응답, 라우터 요청 및 응답

**IGMP** : *internet group management protocol.* 인터넷 계층 프로토콜.

인터넷에서 **멀티캐스트** 서비스를 위해 사용 프로토콜. 
IP호스트가 어떤 멀티캐스트 그룹에 참가하고 있는지 멀티캐스트 라우터에 통보. TTL = 1(하나의 라우터에만)
**[유형 - 최대 응답시간 - 검사합 | 그룹주소(클래스D)]** 8 8 16 | 16(ver.2)

**DHCP :** *Dynamic Host Configuration Protocol* IP주소 관리

규칙에 따라 내가 쓰는 IP주소 자동으로 정해줌. 동적. IP DNS GATEWAY
허용 안 하면 남이 볼 수 없음. 보안. IP주소를 중앙에서 관리.

**<IP주소 관리>**

| 호스트테이블 | 정적할당. 
 | 중앙 집중형, 구조가 간단, 평면구조=중복정보 |
| --- | --- | --- |
| DNS | 동적 할당.  | 계층적 구조. 분산 관리, 
분산관리문제(특정 네트워크 영역만)
 =다른DNS와 연결 필요. 데이터 복잡성=오류가능성. |
| BOOTP(bootstrap) | 동적 할당.  | 디스크 없는 호스트 관리. |
| DHCP | 발전된 동적 주소 할당 프로토콜. | 응용계층 프로토콜.
IP주소 재사용 가능. IP주소 풀pool.
DHCP 클라이언트 - DHCP 서버 |

> **Unicast** : 1 to 1
> 

> **Multicast** : 1 to many 하나의 그룹에 속한 호스트들에게 메세지 전송.
> 

> **Brodcast** : 1 to all
> 

### **ARP테이블 정보 확인**

<aside>
💡 >arp -a

</aside>

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%202.png)

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%203.png)

단계를 거칠 때 마다 인캡슐레이션 ↔ 디캡슐레이션 

### **HEADER**

헤더길이 : **20~60byte**. 보통 20= 필드값 5(5x4=20) | 최대 필드값= 15(15x4=60)

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%204.png)

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%205.png)

**헤더의 구성:** 

**[버전4 | 헤더길이4 | 서비스유형8((QoS:품질)우선순위3(혼잡시폐기)+TOS(타입)4+사용x3) | 전체길이16]** 

**[식별자16(단편화) | 플래그3 | 단편오프셋13 | TTL8 - 프로토콜8 | 헤더검사합16(checksum)]**

**[발신지 IP 32]**-**[목적지 IP 32]**-**[옵션 및 패딩]**-**[데이터]**
(옵션이 사용되면 IP헤더는 40까지 확장. 4단위로 맞추려고 필요 시 0으로 채움=패딩

* **TOS비트**는 서브필드. 오직1비트만 1의 값.
0000 기본 | 0001 비용최소 | 0010 신뢰성최대 | 0100 처리량최대 | 1000지연최소

***플래그** : 단편화에 사용. 3비트 필드. 첫비트x - 2번째비트:DF(don’t fragment) 1이면 단편화 하지 말것.(데이터그램 폐기 후 발신호스트에 ICMP오류 메세지 보냄)
0이면 단편화 할 것. - 3번째비트:MF(more fragment) 1이면 마지막 단편 아님. 0이면 마지막이거나 유일한 단편임.

***단편오프셋** : 데이터 내에서 어느 위치였는지. 단편 오프셋 값은 원래 데이터를 기준으로 8바이트 단위로 계산.

***TTL :** *time to live* 패킷의 활동 시간. 라우터 건널때마다 감소. 0이면 폐기. 대략 두 호스트 사이 위치한 라우터 수의 두배.

***프로토콜** : 데이터그램과 관련된 상위 계층의 프로토콜 식별 필드. 필드 값이 1이면 데이터 부분이 ICMP메세지를, 6이면 TCP세그먼트를, 17이면 UDP 사용자 데이터 그램을 나타냄.

### **PACKET**

**= data(payload) + 제어정보(head, trail) 네트워크 계층 L3 | driver**

IP계층의 패킹 = 데이터그램.

헤더 + 데이터

*단편화 : **MTU** : *maximum transfer unit.* IP데이터그램은 중간 네트워크를 경유할 때마다 그MTU에 적합한 세그먼트로 분할. 세그먼트들은 목적지에서 재 조립. 

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%206.png)

### **>ipconfig/all & IP class**

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%207.png)

![화면 캡처 2023-04-18 151255.png](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/%25ED%2599%2594%25EB%25A9%25B4_%25EC%25BA%25A1%25EC%25B2%2598_2023-04-18_151255.png)

IPv4  :  32비트,  8비트.8비트.8비트.8비트 각 옥텟은 0~255

IPv6  : 128비트,  16비트:16비트:16비트:16비트:16비트:16비트:16비트:16비트

- 네트워크 주소. 호스트 주소
로컬 네트워크 : 주소가 같은

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%208.png)

>>172, 192로 시작되면 사설 망

**IP Class - 구분자 = 서브넷마스크(네트워크.호스트주소)**

**A클래스:** 0네트워크.로컬 1~127.0.0.0 $2^8$(256)네트워크, 한 네트워크당 $2^{24}$-2 (16,777,216)개 호스트 
****1.0.0.0~126.255.255.255 *127은 루프백, 자신
구분자 첫번째 옥텟

**B클래스:** 10네트워크 128~191.0.0.0 $2^{16}$(65,536), $2^{16}$-2(65,536) IP, 
구분자 두번째 옥텟 

**C클래스:** 110네트워크 192~223.0.0.0 $2^{24}$(16,777,216), $2^8$-2(256) 호스트, 구분자 세번째 옥텟

*앞은 네트워크 주소, 맨 뒤는 브로드캐스트 주소

**D클래스:** 1110멀티캐스트 129~233.0.0.0

**E클래스:** 예약(for future) 224~239.0.0.0 

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%209.png)

### **클래스풀/ 클래스리스**

클래스풀 : 클래스 기반 IP주소 체계, 구분자(서브넷 마스크)필요 없음. 앞자리 보면 어느 클래스인지 알 수 있음.

- 클래스리스: 반드시 서브넷 마스크 필요.
    
    **<IP 포화상태 해결을 위한 방법들>**
    
    CIDE ****교재85p *classless inter-domain routing*
    
    NAT
    
    사설 IP
    
    IPv6
    
    **서브네팅 Subnetting** : 클래스 단위보다 더 쪼개서 쓰는 것. 교재 88p
    
- [https://www.calculator.net/ip-subnet-calculator.html](https://www.calculator.net/ip-subnet-calculator.html)
    
    ![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%2010.png)
    

### **PING : ICMP 프로토콜 사용 
internet control message protocol**

핑은 IP 네트워크를 통해 특정한 호스트가 도달할 수 있는 지의 여부를 테스트하는 데 쓰이는 컴퓨터 네트워크 도구 중 하나 이다.

**>ping ip주소**

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%2011.png)

- **>tracert 8.8.8.8(주소)** 라우터추적
    
    ![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%2012.png)
    
    게이트웨이 어디 거치는지
    

### **API** 프로토콜 Application Programming Interface

응용 프로그램 프로그래밍 인터페이스. [프로그래밍](https://namu.wiki/w/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D)에서, 프로그램을 작성하기 위한 일련의 부(Sub) 프로그램, 프로토콜 등을 정의하여 상호 작용을 하기 위한 [인터페이스](https://namu.wiki/w/%EC%9D%B8%ED%84%B0%ED%8E%98%EC%9D%B4%EC%8A%A4) 사양을 말한다.

해당 인터페이스로 보냄.

### **라우터와 스위치의 차이**

스위치

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%2013.png)

라우터

![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%2014.png)

**1. 라우터 3계층 패킷** : 네트워크 사이에 데이터 전송을 수행하는 기기

- 라우터에 의해 네트워크를 상호 연결할 수 있다.
- 라우터는 IP 주소를 사용하여 네트워크 간의 데이터 전송을 수행하며, 이를 '라우팅' 이라고 한다.
- 라우팅을 수행하기 위해서는 미리 **라우팅 테이블**에 네트워크 정보를 등록해두어야 한다.
- 라우팅 테이블에 등록되어 있지 않은 네트워크가 목적지인 데이터는 라우터에 의해 파기 된다.
- IP: 송신자, 수신자, 경로 상에 있는 모든 라우터가 IP데이터그램 전달에 관여.연결이 안되서 그럼. 다 전달.
- TCP: 송신자와 수신자만 TCP 세그먼트 전달에 관여. 연결이 되어 잇어서.
- IP데이터그램(패킷) 헤더에 TTL 정보는 라우터 건널때마다 하나씩 사라지는
- **WAN** *wide area network* | 데이터 패킷
- ***PDU** : *protocol data unit* 계층마다 데이터를 부르는 이름

**2. 스위치 2계층 프레임** : 같은 네트워크 내부에서 데이터 전송을 수행하는 기기

- 스위치는 PC나 서버에 있어서 네트워크 입구에 해당하는 네트워크 기기이다.
- 스위치는 MAC 주소를 사용하여 같은 네트워크의 LAN 포트 간 데이터 전송을 수행한다.
- MAC 주소는 48비트의 LAN 포트 주소이다.
- **ARP 테이블**
- **HUB 허브**
모든 곳으로 다 보냄. 스위치는 지정된 곳으로만 보냄
    
    허브와 스위치는 같은 네트워크 내에서 **LAN** *local area network* 사용됨. 얘네는 IP를 읽지 않음.
    

**3. 게이트웨이 :** 원격 네트워크에 필요. 어플리케이션 레이어(세션+표현+어플).data

### CABLE -

**TWISTED PAIR** 

- **STP/FTP 케이블** shielded twisted pair / foiled twisted pair : Rj-45커넥터 이용
- **UTP 케이블** unshielded twisted pair 4pair 저
    
    DIRECT CABLE : 양 쪽이 568-B
    CROSSOVER CABLE : 이기종간 568-B - 568-A
    
    10GBASE-T 기본 
    
    568-A, 568-B 국가별 표준
    
- **Fiber-optic cable 광케이블** 원거리,
    
    ![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%2015.png)
    
    SM 싱글모드: 신호하나, 반사 각 작아서 더 멀리, 노랑케이블 
    
    ![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%2016.png)
    
     MM 멀티 모드: 신호 여러 개, 주황케이블
    
    ![Untitled](0418%20%E1%84%82%E1%85%A6%E1%84%90%E1%85%B3%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%209c0ecb839b64456eb3415ebb805ea404/Untitled%2017.png)
    
    **Coaxial cable** 동축케이블 원거리, 고가
    
    네트워크 장치들을 파이버 채널이나, 기가비트 이더넷과 같은 광섬유 기반의 전송 시스템이 부착하기 위한 인터페이스, 1Gbps 이상부터 시작
    
- **MDI/MDI-X 자동감지 기능**
    - 다이렉트 케이블이든 크로스 케이블이든 연결만 되면 케이블의 종류를 감지함
    - 노드/단말기 에 맞게 TX/RX 방식을 자동으로 바꾸어서 통신하도록 하는 기능
    - 요즘은 L2/L3 switch, 공유기, 단말기기 등에서 이 기능을 탑재하여 나옴

****GBIC(Gigabit Interface Converter) : 기가비트 접속 변환기****