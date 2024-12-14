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



## Technology Stack
- Frontend: React
- Backend: Express
- Database: PostgreSQL

## Installation Guideline

## Project Deliverables:

- [요구사항 분석 명세서](https://github.com/sogong24/market/tree/main/artifacts/srs)
- Architecture 및 Design Documents
    - [Software Architecture](https://github.com/sogong24/market/blob/main/artifacts/high-level-architecure)
    - [Software Design](https://github.com/sogong24/market/tree/main/artifacts/uml-design)
    - [UI Design](https://github.com/sogong24/market/tree/main/artifacts/ui-design)
- [Coding Standard](https://github.com/sogong24/market/tree/main/artifacts/coding-standard)
- Source Code
    - [Frontend](https://github.com/sogong24/front)
    - [Backend](https://github.com/sogong24/backend)
- [테스트 케이스 및 결과](https://github.com/sogong24/market/tree/main/artifacts/test-cases)

## Repository Structure
- market: 프로젝트 개괄
    - /artifacts: 프로젝트 진행에 사용한 요소들 
    - /classroom: 교수님과 소통용
    - /proposal: 초기 계획안
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

## Project Team Members

### Frontend

- 2020920015 김찬우
- 2020920026 박주현
- 2020920035 오유찬

### Backend

- 2020920007 김민형
- 2021920002 강현우
- 2021920061 최승우