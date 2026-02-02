# 🚀취업 로켓

<p align="center">
  <img src="../image/logo.png">
  <br>
  전체 프로젝트 기간 : 2024-11-15 ~ 2025-02-13 <br>
  
</p>

<p align=center>
  <a href="#">팀 노션</a>
  &nbsp; | &nbsp; 
  <a href="#">API 명세서</a>
  &nbsp; | &nbsp;
  <a href="https://shins99.notion.site/13a7b22f725181a8b443cb71a0869d08?pvs=4">요구사항 정의서</a>   &nbsp; | &nbsp;
  <a href="https://www.figma.com/design/TzQQwcO49HL32VKGTRQVKI/%EC%B7%A8%EC%97%85%EB%A1%9C%EC%BC%93%3A%ED%99%94%EB%A9%B4%EC%84%A4%EA%B3%84%EC%84%9C?node-id=0-1&node-type=canvas">figma</a> 
  <br />
  <a href="#">그라운드 룰</a>
  &nbsp; | &nbsp; 
  <a href="#">트러블 슈팅</a>
</p>

## 📢 취업 로켓 사용해보기

## ⚙️ 기술스택

 <div align= "center">
    <div style="text-align: center">
    <h3 style="border-bottom: 1px  color: #282d33;"> FrontEnd </h3>
        <div style="margin: ; text-align: left;" "text-align: left;"> 
          <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=Figma&logoColor=white">
          <img src="https://img.shields.io/badge/react-17219A?style=for-the-badge&logo=react&logoColor=white">
          <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=Node.js&logoColor=white">
          <img src="https://img.shields.io/badge/Tailwind CSS-06B6D4?style=for-the-badge&logo=Tailwind CSS&logoColor=white">
          <img src="https://img.shields.io/badge/vite-73563B?style=for-the-badge&logo=vite&logoColor=white">
          <img src="https://img.shields.io/badge/reactquery-FF4154?style=for-the-badge&logo=reactquery&logoColor=white">
          <img src="https://img.shields.io/badge/Zustand-47211C?style=for-the-badge&logo=Zustand&logoColor=white">
        </div>
        </div>
        <h3 style="border-bottom: 1px solid #d8dee4; color: #282d33;"> BackEnd </h3>
          <div style="margin: ; text-align: center;">
              <img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white">
              <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white">
              <img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=for-the-badge&logo=Spring Boot&logoColor=white">
              <img src="https://img.shields.io/badge/Spring Security-2AC89F?style=for-the-badge&logo=Spring Security&logoColor=white">
              <img src="https://img.shields.io/badge/JPA-17219A?style=for-the-badge&logo=JPA&logoColor=white">
              <img src="https://img.shields.io/badge/QueryDSL-8A084B?style=for-the-badge&logo=QueryDSL&logoColor=white">
              <img src="https://img.shields.io/badge/mongodb-1DDB16?style=for-the-badge&logo=mongodb&logoColor=white">
        </div>

<h3 style="border-bottom: 1px solid #d8dee4; color: #282d33;"> Infra </h3>
    <div style="margin: ; text-align: left;" "text-align: left;">
          <img src="https://img.shields.io/badge/Amazon S3-02569B?style=for-the-badge&logo=Amazon S3&logoColor=white">
          <img src="https://img.shields.io/badge/Amazon AWS-232F3E?style=for-the-badge&logo=Amazon AWS&logoColor=white">
          <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white">
          <img src="https://img.shields.io/badge/GitHub Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white">
          <img src="https://img.shields.io/badge/Nginx-04B431?style=for-the-badge&logo=Nginx&logoColor=white">
    </div>

  <h3 style="border-bottom: 1px  color: #282d33;"> 협업 </h3>
    <div style="margin: ; text-align: left;" "text-align: left;">
      <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white">
      <img src="https://img.shields.io/badge/Git-94B431?style=for-the-badge&logo=Git&logoColor=white">
      <img src="https://img.shields.io/badge/slack-916?style=for-the-badge&logo=slack&logoColor=white">
    </div>
</div>

## 🏛️ 시스템 아키텍처

<p align="center">

</p>

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                                  Client                                      │
│                        (React + Vite + Tailwind CSS)                        │
└─────────────────────────────────┬───────────────────────────────────────────┘
                                  │
                                  ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                              Nginx (Reverse Proxy)                           │
└─────────────────────────────────┬───────────────────────────────────────────┘
                                  │
                                  ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                         Spring Boot Application                              │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐        │
│  │   OAuth2    │  │  WebSocket  │  │   REST API  │  │     SSE     │        │
│  │   (Kakao)   │  │   (STOMP)   │  │             │  │   (Alarm)   │        │
│  └─────────────┘  └─────────────┘  └─────────────┘  └─────────────┘        │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐        │
│  │  Schedule   │  │   Board     │  │  Question   │  │    User     │        │
│  └─────────────┘  └─────────────┘  └─────────────┘  └─────────────┘        │
└─────────────────────────────────┬───────────────────────────────────────────┘
                                  │
                    ┌─────────────┴─────────────┐
                    ▼                           ▼
        ┌───────────────────┐       ┌───────────────────┐
        │       MySQL       │       │      MongoDB      │
        │   (Primary DB)    │       │  (Document Store) │
        └───────────────────┘       └───────────────────┘
                    │
                    ▼
        ┌───────────────────┐
        │    Amazon S3      │
        │  (File Storage)   │
        └───────────────────┘
```

## 🗂️ Directory 구조도

### BE

```
job-rocket-backend/
├── src/
│   ├── main/
│   │   ├── java/rocket/jobrocketbackend/
│   │   │   ├── JobRocketBackendApplication.java    # 메인 애플리케이션
│   │   │   ├── alarm/                              # 알림 관리 (SSE)
│   │   │   │   ├── controller/
│   │   │   │   ├── service/
│   │   │   │   ├── entity/
│   │   │   │   └── repository/
│   │   │   ├── answer/                             # 면접 답변 관리
│   │   │   ├── board/                              # 게시판 (공지/자유/질문/후기)
│   │   │   │   ├── controller/
│   │   │   │   ├── service/
│   │   │   │   ├── entity/
│   │   │   │   ├── repository/
│   │   │   │   └── dto/
│   │   │   ├── common/                             # 공통 유틸리티
│   │   │   │   ├── entity/
│   │   │   │   ├── dto/
│   │   │   │   └── exception/
│   │   │   ├── config/                             # 설정 클래스
│   │   │   │   ├── SecurityConfig.java
│   │   │   │   ├── WebSocketConfig.java
│   │   │   │   └── RestTemplateConfig.java
│   │   │   ├── introduce/                          # 자기소개서 관리
│   │   │   ├── note/                               # 쪽지 기능
│   │   │   ├── oauth/                              # OAuth 인증 (Kakao)
│   │   │   ├── profile/                            # 사용자 프로필
│   │   │   ├── question/                           # 면접 질문 관리
│   │   │   ├── schedule/                           # 일정 관리
│   │   │   └── user/                               # 사용자 관리
│   │   └── resources/
│   │       └── application.properties
│   └── test/                                       # 테스트 코드
├── build.gradle                                    # Gradle 빌드 설정
└── Dockerfile                                      # Docker 이미지 설정
```

### FE

```
job-rocket-frontend/
├── src/
│   ├── api/                          # API 요청 핸들러
│   │   ├── alarm/                    # 알림 API
│   │   ├── board/                    # 게시판 API
│   │   ├── introduce/                # 자기소개서 API
│   │   ├── note/                     # 쪽지 API
│   │   ├── profile/                  # 프로필 API
│   │   ├── question/                 # 면접 질문 API
│   │   ├── schedule/                 # 일정 API
│   │   └── user/                     # 사용자 API
│   ├── components/                   # 재사용 가능한 컴포넌트
│   │   ├── alarm/                    # 알림 컴포넌트
│   │   ├── board/                    # 게시판 컴포넌트
│   │   │   ├── main/
│   │   │   ├── notice/               # 공지사항
│   │   │   ├── free/                 # 자유게시판
│   │   │   ├── question/             # 질문게시판
│   │   │   └── review/               # 후기게시판
│   │   ├── career/                   # 이력서 관리
│   │   │   ├── careerCommon/
│   │   │   └── pdf/                  # PDF 생성
│   │   ├── common/                   # 공통 컴포넌트 (헤더, 레이아웃)
│   │   ├── note/                     # 쪽지 컴포넌트
│   │   ├── oauth/                    # OAuth 로그인
│   │   ├── profile/                  # 프로필 컴포넌트
│   │   ├── question/                 # 면접 질문 컴포넌트
│   │   │   ├── cs/                   # CS 기반 질문
│   │   │   ├── introduce/            # 자소서 기반 질문
│   │   │   ├── personal/             # 인성 질문
│   │   │   ├── review/               # 면접 복기
│   │   │   └── script/               # 나의 스크립트
│   │   ├── schedule/                 # 일정 관리 컴포넌트
│   │   │   ├── calendar/             # 캘린더
│   │   │   ├── history/              # 히스토리
│   │   │   ├── schedule/             # 일정 CRUD
│   │   │   └── statistics/           # 통계
│   │   └── talentPool/               # 인재풀
│   ├── context/                      # React Context
│   │   └── auth/                     # 인증 상태 관리
│   ├── pages/                        # 페이지 컴포넌트
│   │   ├── Board.jsx                 # 게시판 페이지
│   │   ├── Career.jsx                # 이력서 페이지
│   │   ├── Login.jsx                 # 로그인 페이지
│   │   ├── Profile.jsx               # 프로필 페이지
│   │   ├── Question.jsx              # 면접 질문 페이지
│   │   ├── Schedule.jsx              # 일정 관리 페이지
│   │   ├── Site.jsx                  # 취준 도움 사이트
│   │   ├── TalentPool.jsx            # 인재풀 페이지
│   │   └── Retrospect.jsx            # 회고 페이지
│   ├── store/                        # Zustand 상태 관리
│   ├── App.jsx                       # 루트 컴포넌트
│   └── main.jsx                      # Vite 진입점
├── public/                           # 정적 자원
├── vite.config.js                    # Vite 설정
├── tailwind.config.js                # Tailwind 설정
├── package.json                      # NPM 의존성
└── Dockerfile                        # Docker 이미지 설정
```
## 🚀 핵심 기능

### 회원

#### 로그인

![로그인](../image/회원/로그인.png)
![카카오 권한 허용](../image/회원/카카오권한허용.png)

#### 내정보

![내정보](../image/회원/내정보.png)

#### 쪽지

### 일정관리

#### 일정 목록

![일정목록](../image/일정관리/일정목록.png)

#### 일정 생성

![일정생성](../image/일정관리/일정생성.png)

#### 일정 수정

![수정,삭제](../image/일정관리/수정,삭제.png)
![수정](../image/일정관리/수정.png)

#### 일정 삭제

![수정,삭제](../image/일정관리/수정,삭제.png)
![삭제](../image/일정관리/삭제.png)

#### 통계

![통계](../image/일정관리/통계/통계.png)

#### 히스토리

![히스토리](../image/일정관리/히스토리/히스토리.png)

### 게시판

#### 자유 게시판

#### 질문 게시판

#### 후기 게시판

### 면접 질문

#### 인성 질문

![image](https://github.com/user-attachments/assets/6048bd7c-5ad7-4922-9d44-1185897e2abd)

#### cs 기반 면접질문

![image](https://github.com/user-attachments/assets/065716be-a7ba-4ee6-b53c-10dd21a6895c)

#### 면접 복기

![image](https://github.com/user-attachments/assets/b3f7ec5d-c563-49ff-93bd-c0efb18c6d8c)
![image](https://github.com/user-attachments/assets/aa6f2118-33db-4363-ad56-562d9b590d84)
![image](https://github.com/user-attachments/assets/c1861ce4-2f17-4d92-8f05-94cdca233895)

#### 자소서 및 이력서 기반 면접 질문

![image](https://github.com/user-attachments/assets/2253a74d-1929-41b0-8d06-40f2a517bedd)
![image](https://github.com/user-attachments/assets/fee16a19-9410-4fff-bdc1-ede66a65162e)
![image](https://github.com/user-attachments/assets/832d350b-92a9-459a-b8e8-fc3c0744ed01)

#### 나의 스크립트

![image](https://github.com/user-attachments/assets/c2d23e16-7215-4351-aca8-ec96e0f453f1)
![image](https://github.com/user-attachments/assets/bb51abf9-ec70-427c-8d0e-232015cac65c)

### 취준 도움 사이트 링크 모음

![image](https://github.com/user-attachments/assets/5243702c-bf61-43c1-bbfa-5fd8bf69d67b)

### 푸쉬알람

![알림 화면](../image/푸쉬알림/알림%20전체%20화면.png)

## 팀원 소개

|                신동구                |                     안채원                     |                   정기석                   |                 장호영                 |
| :----------------------------------: | :--------------------------------------------: | :----------------------------------------: | :------------------------------------: |
|     <img src="#" width="100" />      |          <img src="#" width="100" />           |         <img src="#" width="100">          |       <img src="#" width="100">        |
|            **Full-Stack**            |                 **Full-Stack**                 |               **Full-Stack**               |             **Full-Stack**             |
| [@shsh99](https://github.com/shsh99) | [@woneveryday](https://github.com/woneveryday) | [@wjdrltjr5](https://github.com/wjdrltjr5) | [@jang643](https://github.com/jang643) |
