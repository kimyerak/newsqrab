# 📱 Flutter News Shortform App

## 📝 프로젝트 개요
Flutter 기반의 뉴스 숏폼 생성 앱으로, **생성형 AI**를 활용하여 최신 뉴스를 짧고 강렬한 영상 형식으로 제공합니다.
이 앱은 백엔드(NestJS)와 연결되어 뉴스 스크랩, 기사 요약, OpenAI 연동 등을 처리합니다.

## 🚀 프론트 구현 화면
- **🏠 홈 화면 (`home.dart`)**
  - 하단 네비게이션 바를 통해 여러 화면을 탐색 가능
  - 앱 로고 및 알림 버튼이 포함된 커스텀 `AppBar` 제공

- **🔥 팔로잉 (`following.dart`)**
  - 사용자가 팔로우한 뉴스 또는 콘텐츠 제공

- **🌍 탐색 (`explore.dart`)**
  - 트렌딩 뉴스 및 AI가 추천하는 뉴스 탐색 가능

- **📌 스크랩 (`scrap.dart`)**
  - 사용자가 저장한 뉴스 및 콘텐츠 목록 제공

- **🎥 릴스 (`reels.dart`)**
  - 생성형 AI를 통해 자동 생성된 뉴스 숏폼 비디오 제공

- **🎞️ 마이 클립 (`myclip.dart`)**
  - 사용자가 직접 생성하거나 저장한 클립 관리 가능

- **🔔 알림 시스템**
  - 앱 내 `AppBar`에서 알림 버튼을 눌러 최근 알림 확인 가능




## 🚀 백엔드 주요 기능
- **사용자 관리**: 회원가입, 로그인, 프로필 관리
- **뉴스 숏폼 생성**: OpenAI 기반으로 뉴스 요약 및 숏폼 콘텐츠 생성
- **스크랩 기능**: 사용자가 관심 있는 뉴스를 저장 및 관리
- **S3 업로드**: 생성된 숏폼을 AWS S3에 업로드하여 저장
- **백그라운드 작업**: 뉴스 크롤링 및 숏폼 자동 생성 (NestJS Schedule 활용)

## 🏗️ 기술 스택
- **Frontend**: Flutter (Dart)
- **Backend**: NestJS (TypeScript, Mongoose, MongoDB)
- **AI Service**: OpenAI API (GPT 기반 요약 생성)
- **Cloud Storage**: AWS S3
- **Task Scheduling**: NestJS Schedule Module

## 🔧 프로젝트 설정 및 실행 방법

### 1️⃣ 환경 설정
```bash
flutter pub get # 의존성 설치
```

### 2️⃣ 앱 실행
```bash
flutter run
```

### 3️⃣ 백엔드 서버 실행 (NestJS)
```bash
npm install # 의존성 설치
npm run start # 개발 서버 실행
```

## 🔗 API 연동 방식
Flutter 앱은 **NestJS 백엔드 API**와 통신하여 데이터를 주고받습니다.

### 📌 기본 API 엔드포인트
- **사용자 관리**: `/user/login`, `/user/register`
- **뉴스 조회**: `/article/latest`, `/article/:id`
- **숏폼 생성**: `/reels/generate`
- **스크랩**: `/scrap/add`, `/scrap/list`
- **파일 업로드**: `/s3/upload`

## 💡 향후 개발 계획
- **중립적인 뉴스 요약**: RAG로 언론사별 특성 투가
- **할루시네이션, 가짜뉴스 필터링**: 타 뉴스 크롤링

---

이 문서는 지속적으로 업데이트될 예정입니다.
궁금한 점이나 제안이 있다면 언제든지 PR 또는 이슈를 등록해주세요! 🙌

