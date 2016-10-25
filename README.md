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
데이터 센터가 제공되는 어느곳에서나 10분 이내에 모든 CloudBread의 서비스 환경을 배포 가능  
[데이터 센터 위치](https://azure.microsoft.com/en-us/regions/)
[CloudBread ARM 프로젝트 Repo](https://github.com/CloudBreadProject/CloudBread-ARM)









