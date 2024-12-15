## Project Title

시대 마켓

## Project Scope

서울시립대학교 컴퓨터과학부 2024년 소프트웨어공학 프로젝트로, Software Development Life-Cycle을 기반으로 객체지향 소프트웨어공학 방법론을 적용하여 수업 중 직접 작성한 필기를 다른 학생들과 공유할 수 있는 플랫폼 개발

## Project Duration

2024년 2학기

## Highlighted Features

- 필기 업로드/다운로드: 사용자는 PDF 형식의 강의 필기를 업로드할 수 있으며, 포인트를 사용해 필기를 다운로드 받을 수 있음
- 검색 필터링: 과목명, 교수명, 학년/학기별로 필기를 검색 및 필터링할 수 있어 필요한 자료를 손쉽게 찾을 수 있음
- 포인트 기반 시스템: 필기 업로드 시 포인트를 획득하고, 다운로드 시 포인트를 사용하도록 하여 적극적인 참여를 유도
- 평가 시스템: 다운로드한 필기에 대해 좋아요/싫어요로 평가할 수 있어, 양질의 콘텐츠가 유지되도록 함

[Demo video](https://github.com/sogong24/market/blob/main/reports/demo.mp4)

## Project Constraints

- 웹 브라우저 기반: Chrome 지원
- 디자인 및 UI:  다양한 화면 크기(데스크톱, 태블릿, 모바일)에서 최적화된 사용자 경험을 제공
- 언어: JavaScript
- 프레임 워크: React, Node.js
- 배포 및 운영: 이 프로젝트는 배포되지 않으며, 내부 테스트 및 개발 용도로만 사용
- 필기 범위: 컴퓨터과학부에서 진행하는 전공과목으로 제한

## High-level Architecture

![image](https://drive.google.com/uc?export=view&id=16e7AyQfUc2vmwBfWT914vwiSi1gy8joW)

## Technology Stack
- Frontend: React
- Backend: Express
- Database: PostgreSQL

## Installation Guideline

### Frontend

1. Run `npm install create-react-app frontend`
2. Run `npm install react-router-dom`
3. Run `npm install -D tailwindcss postcss autoprefixer`
4. Run `npx tailwindcss init -p`
5. Add path to tailwind.config.js
   ```
   /** @type {import('tailwindcss').Config} */
    module.exports = {
      content: [
        "./src/**/*.{js,jsx,ts,tsx}",
      ],
      theme: {
        extend: {},
      },
      plugins: [],
    }
    ```
6. Add tailwind directives to CSS file (src/index.css)
   ```
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```
8. Run `npm install react-icons`
9. Go to the project repository
10. Run `npm start`
### Backend

1. Install and run [Docker Desktop](https://www.docker.com)
2. Go to the project repository
3. Run `npm install`
4. Run `docker-compose up --build`

## Project Deliverables

- [요구사항 분석 명세서](https://github.com/sogong24/market/blob/main/artifacts/srs/srs-v1.2.pdf)
- Architecture 및 Design Documents
    - [Software Architecture](https://github.com/sogong24/market/blob/main/artifacts/high-level-architecture/high-level-architecture-v1.1.pdf)
    - Software Design
        - [Static Class Diagram](https://github.com/sogong24/market/blob/main/artifacts/uml-design/static-class-diagram.uxf)
        - [Sequence Diagram](https://github.com/sogong24/market/blob/main/artifacts/uml-design/sequence-diagram.uxf)
    - UI Design
        - [Figma](https://github.com/sogong24/market/blob/main/artifacts/ui-design/ui-design.fig)
        - [PNG](https://github.com/sogong24/market/blob/main/artifacts/ui-design/ui-design.png)
    - [Coding Standard](https://github.com/sogong24/market/blob/main/artifacts/coding-standard/coding-standard-v1.1.pdf)
- Source Code
    - [Frontend](https://github.com/sogong24/front)
         - main : 배포 준비가 된 안정적인 코드를 저장하는 기본 브랜치. 업데이트 주기: Pull Request를 통해서만 업데이트되며, 주요 기능이 완료된 후 병합.
         - mypage : 사용자 개인 페이지 개발 작업. 사용자 정보 표시 기능. React 상태 관리 최적화 작업 포함.
         - temp-minbros : 임시 브랜치로, 새로운 기능 또는 실험적인 코드를 테스트하기 위한 공간. 기존 코드와 병합 전 최종 점검용.
         - temp : 기능 구현 전, 테스트와 디버깅 작업을 진행하기 위한 브랜치. 디버깅 로그 추가 및 API 요청 최적화 작업 포함.
         - post-create : 게시물 작성 관련 기능 개발. 글쓰기 페이지 구현.
         - login : 로그인 및 인증 관련 기능 개발.
    - [Backend](https://github.com/sogong24/backend)
        - initial-test: 개발 초기 각 개발 환경에서 잘 동작하는지 확인하는 테스트
        - connect-front: 프론트엔드와의 연동
        - login-signin: 로그인 및 회원가입 기능 구현
        - upload-note: 필기 업로드 기능 구현
        - download-note: 필기 다운로드 기능 구현
        - handle-notes: 필기 업로드 / 다운로드 기능을 제외한 나머지 기능 구현
        - use-password-hash: 로그인 및 회원가입에서 비밀번호에 해시 함수 추가
        - temp: 임시로 필요한 작업 수행
- [테스트 케이스 및 결과](https://github.com/sogong24/market/blob/main/artifacts/test-cases/test-cases-v1.4.xlsx)
- [API Documentation](https://github.com/sogong24/market/blob/main/artifacts/api-documentation/api-documentation-v1.1.pdf)

## Repository Structure
- market: 프로젝트 개괄
    - /artifacts: 프로젝트 진행에 사용한 요소들 
    - /classroom: 교수님과 소통용
    - /proposal: 초기 계획안
    - /reports: 프레젠테이션 및 데모
    - README: 최종 보고서

- backend: 백엔드
    - /config: db설정
    - /controllers: 각각 유저, 노트, 강좌에 대한 함수 처리 로직
    - /docker/api: 도커 설정
    - /middleware: auth 설정
    - /models: 각 유저, 노트, 강좌 객체의 구성 요소들 정의
    - /routes: front에서 보낼 명령을 처리할 라우터
    - /scripts: 강좌 데이터
    - /tests: 테스트 코드
    - /uploads: 물리적 필기 파일이 저장될 경로

- frontend: 프론트엔드
   - /api: API 통신 로직 및 데이터 처리를 담당하는 디렉토리
   - /components: 재사용 가능한 UI 컴포넌트를 저장하는 디렉토리
        - /common: 공통된 layout 설정
        - /postCreate: 노트 기능이 적용된 페이지의 layout 설정
        - /search: 검색 기능이 적용된 페이지의 공통된 layout 설정 
   - /hooks: React의 Custom Hooks를 정의하는 디렉토리
   - /pages: 페이지 단위의 컴포넌트를 저장하는 디렉토리. 예를 들어, 로그인 페이지, 마이페이지, 게시물 작성 페이지 등이 여기에 포함

## Project Team Members

### Frontend

- 2020920015 김찬우
- 2020920026 박주현
- 2020920035 오유찬

### Backend

- 2020920007 김민형
- 2021920002 강현우
- 2021920061 최승우
