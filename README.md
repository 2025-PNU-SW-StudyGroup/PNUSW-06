#
<div align="center">
<img src="images/logo.png" width="80" alt="logo"/>
</div>

# <div align="center">이거무라</br>- AI 기반 맞춤형 식당 추천 서비스</div>
### 이동윤재중 소개
| 김해중 | 김동윤 | 권윤재 | 박준이 |
|:-------:|:-------:|:-------:|:-------:|
|<img width="100px" alt="김해중" src="https://avatars.githubusercontent.com/u/128127416?v=4" /> | <img width="100px" alt="김동윤" src="https://avatars.githubusercontent.com/u/104823367?v=4" /> | <img width="100px" alt="권윤재" src="https://avatars.githubusercontent.com/u/97164187?v=4" /> | <img width="100px" alt="박준이" src="https://avatars.githubusercontent.com/u/57588269?v=4" /> |
| hjkim2124@<br/>pusan.ac.kr | dongyoon0201@<br/>naver.com | jae3344@<br/>pusan.ac.kr | zun_e@<br/>kakao.com |
| 프론트앤드 개발 | 백앤드 개발 | AI 추천 시스템 개발 | 프로젝트 총괄 |
#

### 1. 프로젝트 소개
#### 1.1. 개발배경 및 필요성
학교 근처에서 끼니를 해결해야 하는 일이 잦은 학생들은 대부분 익숙한 몇몇 식당만 반복해서 방문하게 됩니다. "오늘 뭐 먹지?"라는 고민을 해소하기 위한 서비스의 필요성을 느꼈고, 여기에 AI API 활용 경험을 접목해 실질적인 서비스를 구현하고자 본 프로젝트를 기획하게 되었습니다.
<br/>

#### 1.2. 개발목표 및 주요내용
Google Gemini API를 활용한 AI 추천 시스템을 통해, 사용자의 취향, 선호도, 알러지, 최근 방문 이력 등을 반영하여 개인 맞춤형 식당을 추천합니다. 더불어 친구들과의 파티 기능을 통해 그룹 구성원의 식사 선호도를 종합 분석한 집단 추천도 함께 제공합니다. 사용자의 피드백은 추천 정확도 개선에도 반영됩니다.
<br/>

#### 1.3. 세부내용
- 개인 및 집단 맞춤형 식당 추천
- 사용자 피드백(별점/한줄평)을 통한 추천 모델 개선
- 위치 기반 UI 및 정보 보안 고려
- 웹 기반 서비스로 개발 (Spring Boot + Next.js + PostgreSQL)
- Gemini API를 통한 AI 응답 처리
<br/>

#### 1.4. 기존 서비스(상품) 대비 차별성
기존 식당 추천 서비스는 인기 식당이나 위치 중심으로 추천합니다. 반면, 이거무라는 사용자의 알러지, 비선호 음식, 최근 방문 이력 등을 기반으로 사용자별로 최적화된 식당을 추천합니다. 즉, 단순 거리 중심이 아닌 **개인화**에 초점을 맞추고 있습니다.
<br/>

#### 1.5. 사회적가지 도입 계획
- 부산대학교 인근 식당과의 제휴를 통해 **지역 상권 활성화**
- 자취생/기숙사생 등의 **식사 접근성 향상**
- 추천 데이터 기반 **선호도 분석 → 서비스 고도화**
- 향후 타 대학 및 지역으로 **서비스 확장 가능성**
<br/>


### 2.상세설계
#### 2.1. 시스템 구성도
추후 이미지 업로드 예정
<br/>

#### 2.3. 사용기술
| 항목       | 기술 스택              |
|------------|------------------------|
| **Backend** | Java Spring Boot       |
| **Frontend** | Next.js (React 기반)  |
| **DB**      | PostgreSQL             |
| **AI**      | Google Gemini API      |
| **Infra**   | Docker, GitHub         |
| **협업도구**| Notion, Figma          |
<br/>


### 3. 개발결과
**추후 수정하겠습니다.**
</br></br>
[코딩역량강화플랫폼 Online Judge](http://10.125.121.115:8080/)를 예시로 작성하였습니다.
#### 3.1. 전체시스템 흐름도
- 유저 플로우 차트
  > 코딩 역량강화 플랫폼의 회원가입 부분만 작성했습니다. <br/>
  > 사용자의 행동 흐름을 도식화하여 보여줍니다.
  <img width="400px" alt="유저 플로우 차트" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/c8de7c98-efd8-4f64-a39a-720faabccd78" />

- 테스크 플로우 차트
  > 코딩 역량강화 플랫폼의 로그인 부분만 작성했습니다. <br/>
  > 주요 테스크의 프로세스를 도식화하여 보여줍니다.
  <img width="400px" alt="테스크 플로우 차트" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/b83502a9-032d-4453-8687-428d54643610" />

- 시스템 플로우 차트
  > 코딩 역량강화 플랫폼의 로그인 부분만 작성했습니다. <br/>
  > 테스크의 흐름에 따른 데이터 처리를 도식화하여 보여줍니다.
  <img width="600px" alt="시스템 플로우 차트" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/1bfb66f0-446c-4450-8a81-a78bfe5ac9ce" />

  
- IA(Information Architecture)
  > 정보나 시스템의 구조를 도식화하여 보여줍니다. <br/>
  <img width="600px" alt="IA" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/07d842fe-fb73-4079-97a3-58b2495ff331" />

<br/>

#### 3.2. 기능설명
##### ` 메인 페이지 `
- 상단 배너
  - 3초에 마다 자동으로 내용이 넘어갑니다. <br/>
    ![상단 배너](https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/4640389f-dcaf-4b78-916e-188c8e9c6ee7)

- 공지사항
  - 최근 5개의 공지사항을 보여줍니다.
  - 발행된지 일주일이 안 된 공지사항은 new라는 mark표시를 해줍니다.
  - 공지사항 글을 클릭하면 해당 공지사항 게시글로 이동합니다.
  - 상단의 더보기 버튼을 클릭하면 공지사항 페이지로 이동합니다.<br/>
    <img width="600px" alt="공지사항" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/7c425946-ff06-4b32-8b18-4119cc86e308">

- 이번 주 보너스 문제
  - 이번 주의 보너스 점수를 주는 문제를 보여줍니다.
  - 문제를 클릭하면, 해당 문제의 게시글로 이동합니다. <br/>
    <img width="600px" alt="이번 주 보너스 문제" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/5c603984-8cf6-4524-84a6-5410bb6a8cbf">

- 실시간 랭킹
  - 상위 랭킹 10명의 유저를 보여줍니다.
  - 상단의 더보기 버튼을 클릭하면 전체 랭킹 페이지로 이동합니다.<br/>
    <img width="200px" alt="실시간 랭킹" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/8492e285-5423-4c00-bc46-400cbe733d35">
<br/>

##### ` 문제 페이지 `
- 문제 목록
  - 사용자가 설정한 한 번에 보여줄 문제 갯수 만큼 한 화면에 문제를 띄워줍니다.
  - 검색창에서 문제의 제목 및 번호로 문제를 검색할 수 있습니다.
  - 난이도, 영역, 카테고리 별로 문제를 볼 수 있습니다.
  - 상단의 shuffle 이모지를 클릭하면 랜덤으로 선택된 문제 푸는 페이지로 이동합니다.
  - 목록에서 문제를 클릭하면 해당 문제를 푸는 페이지로 이동합니다.
    ![문제 목록](https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/95afd0db-b5a7-4628-ac9c-164513a9e51b)
<br/>


#### 3.3. 기능명세서
<img width="200px" alt="실시간 랭킹" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/97ad3fea-f90a-437a-b611-3fb8cd24070e" />

|라벨|이름|상세|
|:---:|:----------------------------:|:---|
| S1  | 부산대학교 웹메일              | - 부산대 웹메일 형식인지 검증 <br/>- 중복되는 이메일인지 검증 |
| S2  | 부산대학교 웹메일 인증 코드 전송| - 클릭 시 인증 코드 메일로 전송 |
| S3  | 메일 인증 코드                 | - 인증 요청 버튼 클릭 후 활성화 <br/>- 유효시간 5분|
| S4  | 메일 인증 코드 확인            | - 인증코드 검증 |
| S5  | 닉네임                        | - 4 ~ 12자 영어, 숫자, '_' 가능 |
| S6  | 단과대학 선택                  | -부산대학교 단과대학 리스트 보여주기 |
| S7  | 학과 선택                     | - 단과대학 안의 학과 리스트 보여주기 |
| S8  | 비밀번호                      | - 입력 시 텍스트 보이지 않도록 •로 표현해주기 <br/>- 6자 이상 20자 이하, 영어와 숫자 조합 필수 |
| S9  | 비밀번호 확인                  | - 입력 시 텍스트 보이지 않도록 •로 표현해주기 <br/>- 비밀번호와 동일한 지 검증 |
| S10 | 회원가입 완료                  | - 비어 있는 입력 칸이 없는지 검증 <br/>-메일 인증 완료했는지 확인 <br/>-조건을 만족하면 회원가입 성공|
| S11 | 로그인                        | - 클릭 시 로그인 모달로 전환 |

<br/>

#### 3.4. 디렉토리 구조
```
├── build/                      # webpack 설정 파일
├── config/                     # 프로젝트 설정 파일
├── deplay/                     # 배포 설정 파일
├── src/                        # 소스 코드
│   ├── assets/                 # 이미지, 폰트 등의 정적 파일
│   ├── pages/                  # 화면에 나타나는 페이지
│   │   ├── page1/              # 페이지1
│   │   ├── page2/              # 페이지2
│   │   ├── components/         # 여러 페이지에서 공통적으로 사용되는 컴포넌트
│   ├── router/                 # 라우터
│   ├── store/                  # global state store
│   ├── styles/                 # 스타일
│   ├── utils/                  # 유틸리티
├── static/                     # 정적 파일
```
<br/>


### 4. 설치 및 사용 방법
**필요 패키지**
- 위의 사용 기술 참고

```bash
$ git clone https://github.com/test/test.git
$ cd test/frontend
$ npm i
$ export NODE_ENV="development" # windows: set NODE_ENV=development
$ npm run build:dll
$ export TARGET="http://localhost:8000"  # windows: set NODE_ENV=http://localhost:8000
$ npm run dev
```
<br/>


### 5. 소개 및 시연영상
[<img width="700px" alt="소개 및 시연영상" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/162132cd-9af5-4154-9b9a-41c96cf5e8fd" />](https://www.youtube.com/watch?v=EfEgTrm5_u4)

<br/>

### 6. 팀 소개
| MEMBER1 | MEMBER2 | MEMBER3 |
|:-------:|:-------:|:-------:|
|<img width="100px" alt="MEMBER1" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/f5b5df2a-e174-437d-86b2-a5a23d9ee75d" /> | <img width="100px" alt="MEMBER2" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/fe4e8910-4565-4f3f-9bd1-f135e74cb39d" /> | <img width="100px" alt="MEMBER3" src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/675d8471-19b9-4abc-bf8a-be426989b318" /> |
| member1@pusan.ac.kr | member2@gmail.com | member3@naver.com |
| 프론트앤드 개발 | 인프라 구축 <br/> 백앤드 개발 | DB 설계 <br/> 백앤드 개발 |


<br/>


### 7. 해커톤 참여 후기
- MEMBER1
  > 작성하세요.
- MEMBER2
  > 작성하세요.
- MEMBER3
  > 작성하세요.
<br/>
