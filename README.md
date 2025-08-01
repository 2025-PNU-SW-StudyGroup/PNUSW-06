<div align="center">
<img src="images/logo.png" width="80" alt="logo"/>
</div>

# <div align="center">이거무라</br>- AI 기반 맞춤형 식당 추천 서비스</div>
### 이동윤재중 소개
| 김해중 | 김동윤 | 권윤재 | 박준이 |
|:-------:|:-------:|:-------:|:-------:|
|<img width="100px" alt="김해중" src="https://avatars.githubusercontent.com/u/128127416?v=4" /> | <img width="100px" alt="김동윤" src="https://avatars.githubusercontent.com/u/104823367?v=4" /> | <img width="100px" alt="권윤재" src="https://avatars.githubusercontent.com/u/97164187?v=4" /> | <img width="100px" alt="박준이" src="https://avatars.githubusercontent.com/u/57588269?v=4" /> |
| hjkim2124@<br/>pusan.ac.kr | dongyoon0201@<br/>naver.com | jae3344@<br/>pusan.ac.kr | zun_e@<br/>kakao.com |
| - 방문 기록 및 식당 평가 개발 <br/> - 백엔드 코드 통합 | 친구 시스템 및 단체 추천 개발 | AI 식당 추천 시스템 개발 | - 로그인/회원가입 개발 <br/> - 인프라 구축 및 배포 |
#

### 1. 프로젝트 소개
#### 1.1. 개발배경 및 필요성
학교 근처에서 끼니를 해결해야 하는 일이 잦은 학생들은 대부분 익숙한 몇몇 식당만 반복해서 방문하게 됩니다. "오늘 뭐 먹지?"라는 고민을 해소하기 위한 서비스의 필요성을 느꼈고, 여기에 AI API 활용 경험을 접목해 실질적인 서비스를 구현하고자 본 프로젝트를 기획하게 되었습니다.
<br/>

#### 1.2. 개발목표
본 프로젝트의 개발 목표는 학교 근처에서 식사를 해결해야 하는 학생들이 매일 겪는 "오늘 뭐 먹지?"라는 고민을 덜어줄 수 있는 맞춤형 식당 추천 서비스를 제공하는 것입니다. 특히 반복적으로 이용하는 몇몇 식당만 떠올리는 기존의 패턴에서 벗어나, AI 기반 추천 시스템을 통해 다양한 선택지를 제시하고 새로운 식당을 발견할 수 있는 기회를 제공하고자 합니다. 이 과정에서 Google의 Gemini API를 활용하여 실제 서비스에 AI API를 적용해보는 경험을 쌓으려 합니다. 이를 통해 실질적인 기술 역량을 향상시키고, AI 추천 서비스 개발 역량을 키우고자 합니다.
<br/>

#### 1.3. 주요 기능
 1. AI 기반 식당 추천 시스템을 통해 사용자의 취향에 맞는 식당을 추천합니다.
 2. 식당 평가 시스템을 도입해 사용자가 추천받은 식당에 대해 직접 평가하고 피드백을 남기면, 해당 정보를 반영해 추천 정확도를 지속적으로 개선해 나갑니다.
 3. 개인뿐만 아니라 여러 명이 함께 식사할 경우에도 인원과 구성원의 선호를 고려한 집단 추천 시스템을 제공하여, 소모임이나 동아리 활동 등 다양한 상황에서도 유용하게 사용할 수 있도록 설계할 예정입니다
<br/>

#### 1.4. 세부내용
- 개인 및 집단 맞춤형 식당 추천
- 사용자 피드백(별점/한줄평)을 통한 추천 모델 개선
- 위치 기반 UI 및 정보 보안 고려
- 웹 기반 서비스로 개발 (Spring Boot + Next.js + PostgreSQL)
- Gemini API를 통한 AI 응답 처리
<br/>

#### 1.5. 기존 서비스(상품) 대비 차별성
기존 식당 추천 서비스는 인기 식당이나 위치 중심으로 추천합니다. 반면, 이거무라는 사용자의 알러지, 비선호 음식, 최근 방문 이력 등을 기반으로 사용자별로 최적화된 식당을 추천합니다. 즉, 단순 거리 중심이 아닌 **개인화**에 초점을 맞추고 있습니다.
<br/>

#### 1.6. 사회적 가치 도입 계획
- 부산대학교 인근 식당과의 제휴를 통해 **지역 상권 활성화**
- 자취생/기숙사생 등의 **식사 접근성 향상**
- 추천 데이터 기반 **선호도 분석 → 서비스 고도화**
- 향후 타 대학 및 지역으로 **서비스 확장 가능성**
<br/>


### 2.상세설계
#### 2.1. 시스템 구성도
<div align="center">
<img src="images/EatThis_SystemDiagram.png" alt="system_diagram"/>
</div>
<br/>

#### 2.3. 사용기술
- Frontend
  - Next.js, TypeScript, Tailwind CSS :　CSR/SSR 하이브리드 렌더링 기반 UI 구현
  - Zustand : 전역 상태 관리
  - Lottie, Custom Font : 애니메이션 효과 및 사용자 경험 향상
- Backend
  - Java 17, Spring Boot, Gradle : REST API 서버 구현, 의존성 관리
  - Spring Security, JWT : 사용자 인증 및 권한 관리
  - JPA (Hibernate), PostgreSQL : ORM 기반 데이터 저장 및 쿼리 처리
  - Swagger / SpringDoc : API 문서 자동화
- DB
  - PostgreSQL : 관계형 데이터베이스
- AI
  - Google Gemini API : AI 기반 식당 추천 로직 실행
- Infra
  - Docker, Docker Compose : 전체 서비스 컨테이너화 및 실행
  - Nginx (리버스 프록시, 정적파일 제공) : 웹 요청 라우팅 및 보안
- 협업 도구
  - GitHub, Notion, Figma : 형상관리, 문서 협업, UI 설계
<br/>


### 3. 개발결과
#### 3.1. 전체시스템 흐름도
##### 3.1.1 유저 플로우 차트
  > 로그인 <br/>
  <img width="400px" alt="로그인 유저 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/LOGIN_userFlowChart.svg" />
  
  > 친구 추가 <br/>
  <img width="400px" alt="친구 추가 유저 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/FRIEND_userFlowChart.svg" />
  
  > 식당 추천 <br/>
  <img width="400px" alt="식당 추천 유저 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/RECOMMEND_userFlowChart.svg" />
  
  > 방문 기록 <br/>
  <img width="400px" alt="방문 기록 유저 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/VISIT_userFlowChart.svg" />

##### 3.1.2 테스크 플로우 차트
  > 로그인 <br/>
  <img width="400px" alt="로그인 테스크 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/LOGIN_taskFlowChart.svg" />
  
  > 친구 추가 <br/>
  <img width="400px" alt="친구 추가 테스크 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/FRIEND_taskFlowChart.svg" />
  
  > 식당 추천 <br/>
  <img width="400px" alt="식당 추천 테스크 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/RECOMMEND_taskFlowChart.svg" />
  
  > 방문 기록 <br/>
  <img width="400px" alt="방문 기록 테스크 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/VISIT_taskFlowChart.svg" />

##### 3.1.3 시스템 플로우 차트
  > 로그인 <br/>
  <img width="400px" alt="로그인 시스템 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/LOGIN_systemFlowChart.svg" />
  
  > 친구 추가 <br/>
  <img width="400px" alt="친구 추가 시스템 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/FRIEND_systemFlowChart.svg" />
  
  > 식당 추천 <br/>
  <img width="400px" alt="식당 추천 시스템 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/RECOMMEND_systemFlowChart.svg" />
  
  > 방문 기록 <br/>
  <img width="400px" alt="방문 기록 시스템 플로우 차트" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/VISIT_systemFlowChart.svg" />
  
##### 3.1.4 IA(Information Architecture)
  <img width="600px" alt="IA" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/informationArchitecture.svg" />

<br/>

#### 3.2. 기능설명

##### 3.2.1 랜딩페이지
<img width="1108" height="988" alt="image" src="https://github.com/user-attachments/assets/93eb0a4f-3954-413f-909a-743c430570c6" />
<img width="647" height="877" alt="image" src="https://github.com/user-attachments/assets/255390c0-31f2-4b40-85af-8f94e75d050b" />


##### 3.2.2 로그인 화면
<img width="804" height="986" alt="image" src="https://github.com/user-attachments/assets/30949e9a-d6e1-4794-b8d0-efc55b37b065" />

##### 3.2.3 회원 가입 화면
<img width="589" height="900" alt="image" src="https://github.com/user-attachments/assets/433a61dc-04b4-46fa-8731-7ba50be6d65a" />

##### 3.2.4 메인 화면
<img width="791" height="885" alt="image" src="https://github.com/user-attachments/assets/ea4a133d-da8d-4f78-8876-7cdf0a94b611" />

##### 3.2.5 AI 추천 결과
<img width="599" height="866" alt="image" src="https://github.com/user-attachments/assets/66c2507f-1f04-49bd-966c-60438505235d" />

##### 3.2.6 같이 먹기 화면
<img width="654" height="920" alt="image" src="https://github.com/user-attachments/assets/15b187bc-4374-4b10-9e70-d54ed462456a" />

##### 3.2.7 친구 추가 화면
<img width="643" height="349" alt="image" src="https://github.com/user-attachments/assets/0a392c67-8014-4728-9795-772a51947bd7" />

##### 3.2.8 방문기록 화면
<img width="546" height="659" alt="image" src="https://github.com/user-attachments/assets/d3863677-0837-49bf-87f1-4c91b4a3f94a" />



#### 3.3. 기능명세서

##### 3.3.1 로그인/회원가입 화면

|라벨|이름|상세|
|:---:|:----------------------------:|:---|
| L1	| 이메일 입력	| - 유효한 이메일 형식인지 검증 <br/>- 중복되는 이메일인지 검증 |
| L3 |	로그인 버튼	| - 입력 정보 유효성 검사 후 로그인 요청 <br/>- 실패 시 에러 메시지 표시 |
| L4	| 회원가입 링크 |	- 클릭 시 회원가입 화면으로 전환 |
| L5 |	이름 입력 |	- 2~10자 한글, 영어 가능 <br/>- 필수 입력 항목 |
| L6 |	프로필 사진 업로드 |	- JPG, PNG 형식만 허용 <br/>- 최대 10MB 크기 제한 |
| L7	| 알러지 정보 선택	| - 다중 선택 가능 <br/>- 계란, 우유, 견과류, 해산물 등 제공 |
| L8 |	비밀번호 확인	| - 입력 시 텍스트 보이지 않도록 •로 표현 <br/>- 비밀번호와 동일한지 검증 |
| L9 |	회원가입 완료	| - 비어있는 필수 입력칸이 없는지 검증 <br/>- 조건 만족 시 회원가입 성공 |

##### 3.3.2 AI 추천 화면

|라벨|이름|상세|
|:---:|:----------------------------:|:---|
| A1 | 그룹 선택 버튼 | - 혼자 먹기 / 친구와 함께 선택 <br/>- 선택에 따라 다음 단계 활성화 |
| A3 | 선택된 멤버 표시 | - 선택된 친구들의 프로필 표시 <br/>- 개별 제거 가능 |
| A4 | AI 추천 요청 버튼 | - 선택 완료 후 활성화 <br/>- 클릭 시 추천 프로세스 시작 |
| A5 | 로딩 애니메이션 | - AI 분석 중 로딩 표시 <br/>- 예상 시간 안내 (5-10초) |
| A6 | 추천 결과 카드 | - 식당명, 메뉴, 위치 정보 표시 <br/>- 이미지 썸네일 포함 |
| A7 | 식당 상세보기 버튼 | - 클릭 시 식당 상세 정보 화면 이동 |
| A8 | 지도 보기 버튼 | - 식당 위치를 지도에서 확인 |
| A9 | 방문 의사 선택 | - 관심있음/없음/나중에 선택 <br/>- 선택 결과 방문기록에 저장 |
| A10 | 다시 추천받기 | - 현재 결과에 만족하지 않을 때 재추천 |

##### 3.3.3 친구 관리 화면

|라벨|이름|상세|
|:---:|:----------------------------:|:---|
| F1 | 친구 목록 | - 등록된 친구들의 리스트 표시 <br/>- 프로필 사진, 이름, 상태 포함 |
| F3 | 친구 추가 버튼 | - 검색 결과에서 친구 추가 요청 <br/>- 중복 확인 및 본인 제외 |
| F4 | 검색 결과 리스트 | - 검색된 사용자 목록 표시 <br/>- 이미 친구인 경우 표시 |
| F5 | 친구 요청 보낸 목록 | - 보낸 친구 요청 상태 확인 <br/>- 요청 취소 가능 |
| F6 | 친구 요청 받은 목록 | - 받은 친구 요청 리스트 <br/>- 수락/거절 선택 가능 |
| F7 | 친구 삭제 버튼 | - 길게 누르면 삭제 옵션 표시 <br/>- 확인 다이얼로그 후 삭제 |
| F8 | 그룹 생성 버튼 | - 추천용 그룹 미리 생성 <br/>- 그룹명과 멤버 설정 |

##### 3.3.4 마이페이지 화면

|라벨|이름|상세|
|:---:|:----------------------------:|:---|
| M1 | 프로필 정보 영역 | - 프로필 사진, 이름, 이메일 표시 <br/>- 수정 버튼으로 편집 가능 |
| M3 | 선호 식당 관리 | - 좋아하는 식당 리스트 <br/>- 방문기록에서 추가 가능 |
| M4 | 방문 기록 탭 | - 전체 방문 기록 리스트 <br/>- 날짜순 정렬, 필터링 가능 |
| M5 | 방문 기록 아이템 | - 식당명, 방문일, 평가 상태 표시 <br/>- 클릭 시 상세 정보 |
| M6 | 평가하기 버튼 | - 미평가 방문기록에 표시 <br/>- 별점과 코멘트 입력 |
| M7 | 통계 정보 | - 총 방문 횟수, 선호 카테고리 등 <br/>- 시각적 차트로 표시 |
| M8 | 설정 메뉴 | - 알림 설정, 계정 관리 등 <br/>- 로그아웃, 회원탈퇴 옵션 |

##### 3.3.5 식당 상세 정보 화면

|라벨|이름|상세|
|:---:|:----------------------------:|:---|
| D1 | 식당 이미지 | - 대표 이미지 표시 <br/>- 이미지 없을 경우 기본 이미지 |
| D3 | 지도 위치 표시 | - 식당 위치 지도 표시 <br/>- 길찾기 앱 연동 가능 |
| D4 | 영업 정보 | - 영업시간, 전화번호, 주소 <br/>- 클릭 시 전화 걸기/복사 |
| D5 | 내 평가 영역 | - 기존 평가 표시/수정 <br/>- 별점, 코멘트 입력 |
| D6 | 친구들 평가 | - 같은 그룹 친구들의 평가 <br/>- 평가 없을 경우 안내 메시지 |
| D7 | 즐겨찾기 버튼 | - 선호 식당에 추가/제거 <br/>- 하트 아이콘으로 상태 표시 |
| D8 | 공유하기 버튼 | - 식당 정보를 외부 앱으로 공유 <br/>- 링크 복사, SNS 공유 등 |


#### 3.4. 디렉토리 구조
```
📦 EatThis
├── 📁 EatThisBack          # 백엔드(Spring Boot)
│   ├── Dockerfile
│   ├── build.gradle
│   ├── settings.gradle
│   ├── pom.xml
│   ├── gradlew / gradlew.bat
│   ├── 📁 src
│   │   └── main/java/com/ydyjj/eatthisback
│   │       ├── EatThisBackApplication.java
│   │       ├── 📁 common                # 공통 응답 형식
│   │       ├── 📁 config                # 설정 (보안, Swagger 등)
│   │       ├── 📁 controller            # API 컨트롤러
│   │       ├── 📁 dto                   # 데이터 전송 객체
│   │       ├── 📁 entity                # JPA 엔티티
│   │       ├── 📁 exception             # 전역 예외 처리
│   │       ├── 📁 repository            # DB 리포지토리
│   │       ├── 📁 security              # JWT 및 인증 로직
│   │       └── 📁 service
│   │           └── 📁 impl             # 서비스 구현체
│   └── 📁 resources
│       └── application.properties

├── 📁 EatThisFront         # 프론트엔드(Next.js)
│   ├── Dockerfile
│   ├── package.json / lock
│   ├── next.config.ts / js
│   ├── 📁 app               # 페이지별 라우팅
│   │   ├── login, signup, find, friends, main, visits, result 등
│   ├── 📁 components        # UI 컴포넌트
│   ├── 📁 hooks             # 커스텀 훅
│   ├── 📁 lib               # API 함수, 유틸
│   ├── 📁 public            # 정적 파일 및 이미지
│   ├── 📁 store             # 상태 관리
│   └── tailwind.config.ts  # Tailwind 설정

├── 📁 EatThisInfra         # 인프라 구성(Docker, DB, Nginx)
│   ├── docker-compose.yml
│   ├── 📁 db
│   │   └── init.sql
│   └── 📁 nginx
│       └── nginx.conf
```

<br/>

### 4. 사용 방법

[![Visit Dev Badge Maker](https://img.shields.io/badge/Visit-Eat%20This%20PNU-FFA726?style=for-the-badge&logo=github&logoColor=white)](https://eatthispnu.com/)

<br/>


### 5. 소개 및 시연영상
유튜브 링크 입니다. <br/>
[<img width="700px" alt="소개 및 시연영상" src="https://github.com/2025-PNU-SW-StudyGroup/PNUSW-06/blob/main/images/PNUSW-06_demo_video_thumbnail.png" />](https://youtu.be/Z67Zp1dLph0)

<br/>


### 6. 해커톤 및 SW 학습 공동체 참여 후기
- 김해중
  > 이번 SW 학습 공동체 활동을 위해 모인 팀원들과 함께 BeeMaker 대회에 참여해보았지만 아쉽게 떨어졌습니다. 처음에는 두 가지 주제의 프로젝트를 병행하다보니 대회용 프로젝트의 몰입도와 기획 완성도가 떨어졌던 것 같습니다. 대회 문제를 빠르게 해결하고나니 학습공동체 활동용 프로젝트에 더 집중할 수 있었습니다. 프론트엔드와 백엔드 구분 없이 모두가 각자 담당한 기능을 구현하고, 각 기능을 통합하고, 프로젝트를 완성하면서 풀스택 개발자로서의 역량도 기르고 소통과 협업의 능력을 키우는 값진 12주 간의 경험이 되었습니다. 팀원 모두가 활동에 열심히 참여해주고 마지막에는 배포까지 성공적으로 마무리하며 큰 성취감을 느꼈습니다. 
- 김동윤
  > BeeMaker 대회에 참여하고자 하였지만, 여러가지 사유로 아쉽게 탈락하였습니다. 탈락을 계기로 팀원간의 결속력을 다질 수 있었고, 더 나은 프로젝트 발전의 밑거름이 되었다고 생각합니다. 팀원 4명 모두 맡은바를 충실히 이행하였습니다. 저는 친구 추가 및 단체 추천을 설계하고 구현하였으며,   다른 팀원들이 개발한 파트에 대해 소통 하고 이해하며 더 나은 완성도를 가지게 되었습니다. 성공적인 결과물 도출로 인한 성취감 느낄 수 있던 활동이었습니다.
- 권윤재
  > BeeMaker 대회를 준비하며 열심히 도전했지만 아쉽게도 탈락하게 되었습니다. 그러나 학습 공동체 활동이 함께 진행되었기에 프로젝트가 중단되지 않고 끝까지 이어질 수 있었습니다. 저는 AI 추천 시스템을 직접 설계하고 구현했으며, 팀원들 모두가 각자의 역할을 책임감 있게 수행했습니다. 기능을 통합하고 소통하며 협업하는 과정을 통해 실력은 물론, 팀워크와 책임감도 함께 키울 수 있었던 값진 시간이었습니다. 프로젝트를 끝까지 잘 마무리하고 배포까지 완료할 수 있어 정말 뿌듯했습니다.
- 박준이
  > 팀 구성원들과 기술 스택 경계를 허물고 풀스택 방식의 애자일 개발 환경을 조성했습니다. 인프라 설계부터 배포 자동화까지 DevOps 파이프라인을 구축하며, 동시에 스크럼 마스터 역할로 프로젝트 일정을 관리했습니다.
각자 맡은 서비스 모듈을 개발하고 마이크로서비스 통합 과정에서 발생한 기술적 이슈들을 해결하며 시스템 아키텍처 설계 경험을 쌓았습니다. 최종적으로 프로덕션 환경 배포를 성공시키며 팀 전체가 엔드투엔드 개발 프로세스를 완주하는 뜻깊은 성과를 거둬 몹시 만족스럽습니다.​​​​​​​​​​​​​​​​
<br/>
