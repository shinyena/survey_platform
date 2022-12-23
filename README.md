# 설문조사 기반 데이터 공유 플랫폼
## 개요
### 프로젝트 소개
- 설문조사 플랫폼: 설문 생성, 복제, 삭제 등 기본적인 설문 제작 서비스
- 설문 데이터 허브: 포인트 사용을 통한 전체공개 설문 조사 결과 열람 가능
### 기능 소개
0. 로그인, 회원가입, 회원정보수정, 회원탈퇴
1. 설문 생성, 수정, 삭제
2. 답변 생성, 수정, 삭제
3. 생성한 설문 및 답변한 설문 조회
4. 설문 허브 조회 및 구매
5. 그룹 생성, 수정, 삭제
6. 그룹 허브 조회 및 참여
7. 설문 분석
8. 관리자 기능
### 사용 기술
- Frontend: 
![](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=white)
- Backend: 
![](https://img.shields.io/badge/Java-007396?style=flat-square&logo=java&logoColor=white)
![](https://img.shields.io/badge/SpringBoot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![](https://img.shields.io/badge/ApacheKafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![](https://img.shields.io/badge/KakaoiCloud-FFCD00?style=flat-square&logo=kakao&logoColor=white)
- Database:
![](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
- CI/CD:
![](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![](https://img.shields.io/badge/Argo-EF7B4D?style=flat-square&logo=argo&logoColor=white)
## 구현
### 1. MSA
![](readmeImg/msa.png)

|Service|Description|
|---|---|
|[Eureka Server](https://github.com/solbiko/survey_platform_backend_eurekaserver.git)||
|[Gateway](https://github.com/solbiko/survey_platform_backend_gateway.git)||
|[Frontend](https://github.com/solbiko/survey_platform_frontend_react.git)|9|
|[Auth Service](https://github.com/solbiko/survey_platform_backend_auth.git)|사용자 가입 및 사용자 그룹 서비스|
|[Analysis Service](https://github.com/OYJ-hansung/survey_platform_backend_analysis.git)|설문 분석 서비스|
|[Common Service](https://github.com/solbiko/survey_platform_backend_common.git)||
|[Point Service](https://github.com/stella693/survey_platform_backend_point.git)|사용자 포인트 서비스|
|[Survey Service](https://github.com/solbiko/survey_platform_backend_survey.git)||
### 2. System Architecture
![](readmeImg/sa.png)
### 3. Database
- Analysis DB: 설문 분석 정보 테이블
![](readmeImg/dbimg/analysis_db.png)
- Common DB: 플랫폼 기본 정보 테이블
![](readmeImg/dbimg/common_db.png)
- Point DB: 사용자 포인트 정보 테이블
![](readmeImg/dbimg/point_db.png)
- Survey DB: 설문, 질문, 답변 정보 테이블
![](readmeImg/dbimg/survey_db.png)
- User DB: 사용자, 그룹 정보 테이블
![](readmeImg/dbimg/user_db.png)
