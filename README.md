# 뽀모타임(Pomotime)
**뽀모타임(Pomotime)** 은 뽀모도로 공부법을 기반으로 한 타이머와 일정 관리 기능을 제공하여 사용자가 효율적으로 공부 시간을 관리할 수 있도록 돕는 웹 애플리케이션입니다.

## 🛠️ 사용한 기술 스택
### 디자인
<img src="https://img.shields.io/badge/figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white">

### 프론트엔드
<img src="https://img.shields.io/badge/ejs-B4CA65?style=for-the-badge&logo=ejs&logoColor=black"><img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=black"><img src="https://img.shields.io/badge/css3-1572B6?style=for-the-badge&logo=css3&logoColor=black"><img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
### 백엔드
<img src="https://img.shields.io/badge/nodedotjs-5FA04E?style=for-the-badge&logo=nodedotjs&logoColor=black"><img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=black"><img src="https://img.shields.io/badge/amazons3-569A31?style=for-the-badge&logo=amazons3&logoColor=black">
### 배포
<img src="https://img.shields.io/badge/filezilla-BF0000?style=for-the-badge&logo=filezilla&logoColor=black">

---

## 📅 프로젝트 개요
- 기간: 2024년 10월 30일 ~ 11월 14일 (2주)
- 팀 프로젝트
- 주요 기능:
    - 공부 시간 관리용 타이머 (뽀모도로 타이머 및 일반 타이머)
    - 일정 관리 (달력 기반 일정 추가 및 관리)
    - 로그인 및 회원 관리
    - 사용자 피드 공유 기능
---

## 🔍 프로젝트를 시작하게 된 계기
프로젝트를 시작할 당시 **"어떤 페이지를 만들 것인가?"** 에 대해 고민했습니다.
우리가 직접 사용하고 도움이 될 만한 페이지를 만들면 더욱 의욕적으로 작업할 수 있다는 결론에 도달했습니다.
결과적으로, **공부에 도움을 주는 일정 관리 및 타이머 기능** 개발에 초점을 맞추게 되었습니다.

---

## 💡 뽀모도로 공부법
**뽀모도로 타이머** 란 25분 동안 집중하여 공부하고, 이후 5분간 휴식하는 과정을 하나의 사이클로 잡아 반복하는 공부법입니다.

- 장점:
    - 최대 집중 시간을 활용하여 생산성 향상
    - 피로도를 최소화
- 아이디어:
    - 타이머 기능과 일정 관리 기능을 결합하여 생산성을 극대화할 수 있도록 설계
---

## 🎯 주요 타겟층 및 기대효과
### 타겟층
공부 시간 관리를 원하는 모든 연령층
- 직관적이고 친숙한 UI 디자인으로 누구나 쉽게 사용 가능
### 기대효과
- 설치가 필요 없는 웹 기반 앱으로 사용자 경험 향상
- 꾸준한 학습 관리로 집중력 및 학습 효율 증가

---

## 📋 주요 기능
### 1. 로그인 및 회원 관리
- 회원가입 시 DB에 저장된 정보를 통해 로그인 기능 구현
- 세션을 활용해 비인가 접근 방지
- 추가 기능:
    - 이메일 찾기 (DB 탐색)
    - 비밀번호 재설정 (해시 암호화)
### 2. 피드 페이지
- 사용자 간 정보 공유
- 피드 렌더링 최적화: 무한 스크롤 구현으로 성능 개선
- 이미지 최적화: Amazon S3를 사용해 대용량 이미지 관리
### 3. 일정 관리 페이지
- 달력 기반 일정 관리 기능
- 특정 날짜의 일정을 추가/삭제/편집 가능
- 일정 데이터 구조:
    - 사용자 ID
    - 일정 내용
    - 생성된 날짜
### 4. 타이머 페이지
- **뽀모도로 타이머**: 25분 공부 + 5분 휴식 반복
- **일반 타이머**: 지속적인 집중 시간을 측정
### 5. 마이페이지
- 사용자 일정의 상태 확인 (미완료, 진행 중, 완료)
- 좋아요를 누른 피드 모아보기

---

## 📊 프로젝트 구조
**MVC 패턴**을 기반으로 프로젝트를 설계
```
src/
├── controllers/
├── models/
├── routes/
├── views/
└── public/
```

---

## 🧩 해결한 과제
### 1. 로그인 페이지 보안 강화
- **문제**: URL 변경으로 비인가 사용자가 접근 가능
- **해결**: 세션을 활용한 접근 제어
### 2. 피드 렌더링 최적화
- **문제**: 피드 과다 로드로 성능 저하
- **해결**: 초기 로드 시 3개의 데이터만 불러오고, 무한 스크롤로 추가 데이터 로드
### 3. 달력 렌더링
- **문제**: 날짜 이동 시 다수의 DOM 요소 생성
- **해결**: 초기 로드 시 모든 요소를 생성하고, DOM 조작으로 표시

---

## 💭 작업 후기 및 피드백
이번 프로젝트를 통해 기획, 디자인, 프론트엔드, 백엔드, DB 연결까지의 전 과정을 경험할 수 있었습니다.
특히 **Git 협업**과 제한된 시간 내 효율적인 작업 진행이 중요함을 느꼈습니다.

### 아쉬운 점
- 공부 시간 기록 및 리워드 시스템
- 주간 공부 통계 시각화
- 목표 의식을 강화할 수 있는 추가 기능
### 앞으로의 계획
프로젝트가 끝난 이후에도 기능 업데이트를 통해 더욱 완성도를 높일 예정입니다.
