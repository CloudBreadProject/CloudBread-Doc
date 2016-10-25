# CloudBread-Doc 프로젝트
이 문서는 CloudBread 프로젝트의 주요기능에 대해 소개하는 Repository

### CloudBread는
클라우드 기반 모바일 게임 서버 플랫폼: MGBaaS  
100% 국산 공개SW 프로젝트인 클라우드브레드(CloudBread)는 클라우드 기반의 오픈소스 프로젝트로서 폭발적인 성장을 하고 있는 모바일 게임을 위한 올인원(all-in-one) 서버 엔진 플랫폼이다.  

모바일 게임을 통해 축적되는 빅데이타인 사용자 행동(패턴) 분석을 중요한 첫 번째 이정표로 목표하고 있으며, 특히 머신러닝(Machine Learning) 엔진을 프로젝트의 중장기적인 차별화 기능중 하나로 개발하고 있다.  

클라우드브레드 프로젝트는 현재 모바일 게임을 위해 최적화된 토탈 서버 엔진과 빅데이타 분석 그리고 이를 통한 머신러닝으로 이어지는 성장 로드맵(roadmap)을 고려하고 있으며, 이런 다양한 공개SW 모듈들이 다양한 타 공개SW 에서도 활용할 수 있도록 공개성이 높은 MIT 라이센스를 채택하고 있다.  

한국의 아틀라시안(Atlassian)을 지향하는 클라우드브레드 프로젝트는 클라우드 환경에서 모바일 게임을 위란 통합 서버 엔진으로서 MGBaaS(Mobile Game Backend as a Service) 플랫폼을 추구한다.  

### CloudBread 프로젝트 공식 웹사이트
CloudBread 프로젝트 : https://github.com/CloudBreadProject  
CloudBread 메인 : https://github.com/CloudBreadProject/CloudBread  
CloudBread 웹사이트 : http://www.cloudbread.org/  
CloudBread 공식 페이스북 그룹 : https://www.facebook.com/groups/cloudBreadProject/  
CloudBread 개발자 가이드wiki(한글) : https://github.com/CloudBreadProject/CloudBread/wiki/Home-kor  
CloudBread 설치 가이드 wiki(한글) : https://github.com/CloudBreadProject/CloudBread/wiki/Install-guide-kor  
CloudBread API 레퍼런스 : http://cloudbreadproject.github.io/  

###1. 모바일 게임을 위한 로직
모바일 게임에 필요한 100여가지의 다양한 behavior 들을 구현해 API를 호출해 즉시 사용가능하도록 로직 구현  
[CloudBread 설치가이드 문서 참조](https://github.com/CloudBreadProject/CloudBread/wiki/Home-kor)  
[CloudBread API 가이드 문서 참조](https://github.com/CloudBreadProject/CloudBread/wiki/CloudBread-behaviors-list)

###2. PaaS 클라우드 기반 게임 서버 (엔진)
CloudBread는 PaaS/DaaS 기반 게임서버로 모바일 게임 개발자(사)가 클라이언트   개발에만 집중할 수 있도록 관리 포인트를 최소화할 수 있음  
[CloudBread 캠프 아키텍처 가이드 문서 참조](https://github.com/CloudBreadProject/CloudBread-Doc/tree/master/camp-docs)

###3. 개발/테스트/배포 통합환경
클라우드 서비스가 제공하는 환경을 모바일 게임 개발사가 더 쉽게 활용 가능하도록 도움  
개발자가 개발/게시/배포 할 경우 익숙한 git/github을 이용 가능하며, node.js로 개발된 Admin-Web이나 Socket 등의 프로젝트도 즉시 App Service로 배포 가능하도록 기본 PaaS의 기능으로 제공  
[CloudBread ARM 배포 Repo](https://github.com/CloudBreadProject/CloudBread-ARM)
[App Service의 git/github 등 통합 배포](https://azure.microsoft.com/ko-kr/documentation/articles/web-sites-deploy//)

###4. 서비스 규모에 따른 클라이언트 게임변경 없음
모바일 게임 클라이언트는 제공되는 API를 호출하면 되며, 무제한에 가까운 클라우드 기반 API 처리 기능을 그대로 활용   가능  
이미 카카오 입점 게임 등의 stress test 등을 진행했으며, 클라우드 PaaS App Service의 scale-up과 scale-out을 활용해 무제한에 가까운 인스턴스를 활용 가능. 지난 Unity United 행사에서 jmetor 및 cloud 기반 성능 테스트 관련 시연을 수행했고, 6000RPS 이상의 처리 성능 기본 제공  
[Unity United 2016 발표자료 성능지표](http://www.slideshare.net/daewkim73/unity-60)

###5. 테스트/개발 가이드
POSTMAN / Github wiki 및 CloudBread 캠프를 통해 제공된 콘텐트를 이용해 게임 백엔드로 구현 가능  
특히, 100여개의 Behavior를 테스트 하기 위해 직접 Rest API를 제작하거나 만들 필요 없이, Postman의 collection을 이용할 수 있어 바로 Camp 등에서도 참여자와 협업 가능한 환경 제공  
[CloudBread wiki 개발 가이드](https://github.com/CloudBreadProject/CloudBread/wiki/Home-kor)


###6. 게임 서버 글로벌 배포
ARM 패키지를 이용해 전세계 원하는 지역의 데이터센터에 손쉬운 배포 가능하도록 자동화된 배포환경 구현  
데이터 센터가 제공되는 어느곳에서나 10분 이내에 모든 CloudBread의 서비스 환경을 배포 가능해 동남아 pre-launching이나 북미 유럽 지역에 최적화된 latency 제공 가능  
[데이터 센터 위치](https://azure.microsoft.com/en-us/regions/)
[CloudBread ARM 프로젝트 Repo](https://github.com/CloudBreadProject/CloudBread-ARM)

###7. 글로벌 동시 배포/트래픽 분산
글로벌 동시 론칭시 게이머가 가까운 데이터센터에 자동 접속할 수 있도록 돕는 환경 구현  
Traffic manager를 이용한 글로벌 론칭 프로젝트 가능  
![글로벌 론칭1](images/07-01.png)

Traffic manager를 이용하면 사용자로부터 가장 가까운 데이터센터로 request가 요청됨  

![글로벌 론칭2](images/07-02.png)
백엔드의 데이터 동기화 기술이 어려운 부분이며, 이렇게 ServiceBus Topic을 이용해 replication 수행  
[Traffic Manager 참조문서](https://azure.microsoft.com/en-us/documentation/articles/traffic-manager-overview/)

###8. AES 데이터 암호화
AES256으로 기본 Encryption된 데이터 처리
[CloudBread 개발자 가이드 암호화 참조링크](https://github.com/CloudBreadProject/CloudBread/wiki/Home-kor)
- Crypt 처리로 web.config의 설정을 이용해 AES256 암호화 처리 가능
```
    <!-- Encryption configuration. 암호화 설정-->
    <add key="CloudBreadCryptSetting" value="AES256"></add>
    <add key="CloudBreadCryptKey" value="1234567890123456"></add>
    <add key="CloudBreadCryptIV" value="1234567890123456"></add>
```
- 클라이언트에서 암호화 구성을 수행해 CloudBread API를 호출
- 암호화되어 전달된 텍스트를 CloudBread가 복호화해 서버에 저장
- 암호화 설정시 자동 클라이언트에 암호화된 문자열 response
- **[CloudBread-Encrypt-Text-Tool](https://github.com/CloudBreadProject/CloudBread-Encrypt-Text-Tool)**로 암호화 복호화를 개발시 문자열 테스트 가능
- Postman에 기본 설정된 예제(Encrypt로 시작)를 활용 가능
- DEMO 용도로, "https://cb2-crypt-demo.azurewebsites.net" 서버 이용 가능

###9. 게임 로그 저장
NoSQL 저장소를 활용해 JSON기반 데이터를 향후 목적으로 적재
CloudBread에서의 로그는 기본적으로 Behavior API를 통해 데이터가 변경되는 모든 루틴에서 호출됨
예를 들어, 
[CBComInsMemberItem API](https://github.com/CloudBreadProject/CloudBread/blob/master/Controllers/CBComInsMemberItemController.cs)  
의 경우 아래와 같이 로그를 적재하고 RunLog()를 수행
```
...
// task end log
logMessage.memberID = p.MemberID;
logMessage.Level = "INFO";
logMessage.Logger = "CBComInsMemberItemController";
logMessage.Message = jsonParam;
Logging.RunLog(logMessage);
...
```
RunLog()는 [CBLoggers](https://github.com/CloudBreadProject/CloudBread/blob/master/CBLoggers.cs) 에 implement 되어있고, config에 따라 NoSQL Table Storage 등에 적재 가능  
```
...
switch (globalVal.CloudBreadLoggerSetting)
{
    case "SQL":
        /// Save log on SQL

    case "ATS":
        /// Save log on Azure Table Storage

    case "AQS":
        /// Save log on Azure Queue Storage

    case "redis":
        /// Save log on Azure Redis Cache
        /// yyyymmdd:memberid:Controller:GUID
}
...
```
이렇게 원하는 타입의 분석 성향과 목적에 맞는 NoSQL에 적재 가능하며 기본 ATS - Table Storage를 권장  
참고링크 : [CloudBread CBLogger 로그 처리 클래스](NoSQL 저장소를 활용해 JSON기반   데이터를  향후 분석 목적으로 적재)

###10. 기본 관리자 화면
게임 관련 데이터를 관리하는 기본 관리자 화면과 통계 정보를 확인 가능한 화면 제공  
[CloudBread Admin Web Repo 공식](https://github.com/CloudBreadProject/CloudBread-Admin-Web)
[현재 배포 중인 React로 개발된 2.1 project](https://github.com/CloudBreadProject/CloudBread-Admin-Web/tree/2.1.0-LeeJeongYeop)를 아래 링크에서 검토 가능  
```
관리자 페이지 프로젝트(2.1 stable) 
Admin-Web 데모 링크 : https://cb2-admin-demo.azurewebsites.net/  
id : demo@cb2admin.onmicrosoft.com  
pwd : P@ssw0rd!  
```

[CloudBread Admin Web 2.5 - node](https://github.com/CloudBreadProject/CloudBread-Admin-Web/tree/master) 프로젝트를 전체 node.js 로 개발 중  

###11. DAU/HAU/ARPU 통계
일일 사용자 등의 통계 정보를 위의 10번 Admin-Web 프로젝트에서 확인 가능  
통계 데이터를 generate하는 schduler 프로젝트는 [CloudBread-Scheduler](https://github.com/CloudBreadProject/CloudBread-Scheduler) Repo에서 처리  

현재 Schduler를 실행하면 아래의 Slack 채널에 messgae가 도착하도록 구성된 상태  
CloudBread Slack Notification : https://cloudbread.slack.com/messages/general/  
즉, 해당 notification을 받아야 하는 팀원은 slack channel에서 관련 batch 작업이 완료 되는 것을 확인 가능  

설치 및 구성에 대해서는 [CloudBread 설치 가이드 wiki](https://github.com/CloudBreadProject/CloudBread/wiki/Install-guide-kor)의 CloudBread-Scheduler 참조  

12. 이벤트/쿠폰/선물관리
게임에 필요한 기능 구현 완료  
관리자 페이지에서 모두 처리 가능하며, 클라이언트에서는 Postman 및 [Behavior 리스트 문서](https://github.com/CloudBreadProject/CloudBread/wiki/CloudBread-behaviors-list) 를 참조해 해당 API를 호출 처리  

13. 로그분석
적재되는 NoSQL기반 로그 데이터를 Big-data를 활용해 분석  


