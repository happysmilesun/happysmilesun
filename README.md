## 안녕하세요 👋

다우기술에서 웹 서비스를 개발하고 있습니다.
2024년 2월 입사 후 신규 프로젝트 3건을 맡아 분석·설계부터 개발, 운영, 인수인계까지 했습니다.

이미 운영 중인 서비스에 기능을 붙이는 일이 많아서, 기존 정책을 깨지 않으면서 구조를 바꾸는 데 신경을 많이 씁니다.
느린 화면이나 이상한 에러가 생기면 원인을 끝까지 찾아보는 편이고, 고친 뒤에는 결과가 전과 같은지 꼭 확인합니다.

요즘은 AI를 실제 업무에 어떻게 붙일 수 있을지 관심이 많아서, 동기들과 AI 사이드 프로젝트를 하고 있고 업무에서도 AI 코드 리뷰·보안 점검을 도입해 쓰고 있습니다.

![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![JPA](https://img.shields.io/badge/JPA%20·%20Querydsl-59666C?style=flat-square&logo=hibernate&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=flat-square)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js%202%2F3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![GCP](https://img.shields.io/badge/GCP%20·%20GKE-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Claude API](https://img.shields.io/badge/Claude%20API-D97757?style=flat-square&logo=anthropic&logoColor=white)

---

## 📌 한눈에 보기

| | |
|---|---|
| **직장** | 다우기술 웹 애플리케이션 개발(풀스택) 사원 · 2024.02 ~ 현재 (2년 9개월, 정규직) |
| **프로젝트** | 신규 프로젝트 3건을 분석·설계 → 개발 → 운영 → 인수인계까지 수행<br>차세대 그룹웨어 백오피스/고객포탈 → 임직원 복지몰 애드웰 → 모바일 쿠폰 서비스 애드콘<br>애드콘 주문내역 조회 성능 **약 16배** 개선 (첫 조회 3.2초 → 0.2초) |
| **인턴** | 금융권 2회 — KB국민은행 개발 인턴, KBDS 어플리케이션 운영팀 인턴 |
| **AI** | 동기들과 진행한 AI 사이드 프로젝트 **DO-AUI**(LLM tool use 오케스트레이터) 아이디어 제안·설계·프로토타입<br>AI 이중 보안 점검 체계 · PR AI 리뷰 자동화 도입 |
| **자격** | 정보처리기사, SQLD |

---

## 💼 Work — 다우기술 (2024.02 ~ 현재)

### 차세대 백오피스 / 고객포탈 `2024.02 ~ 2025.07`
그룹웨어 다우오피스 3.0 → 4.0 전면 개편에 따른 백오피스·고객포탈 신규 구축 (100명+ 참여, 약 2만 고객사 대상)
- 상품·할인 관리 전담, 백오피스 전 영역 도메인 분석(도메인 경계 10개+·Aggregate)·ERD·아키텍처 설계
- **메일/SMS 통합 알림 재설계 + 42종 개발** — AFTER_COMMIT 이벤트 + @Async 독립 파이프라인, 롤백 건 알림 0건
- **컨텐츠(광고) 서버 분리** — 전수 매칭 스케줄러 제거, RabbitMQ 프로비저닝으로 반영 최대 10분 → 즉시
- 야간 자동 카드 결제 배치 트랜잭션 경계 정리, nginx 프록시 구간 chunked 불일치로 인한 5xx 원인 규명

`Spring Boot` `JPA` `Querydsl` `RabbitMQ` `Spring AOP` `Spring Cloud Gateway` `GCS` `GKE` `Vue.js`

### 임직원 복지몰 애드웰 `2025.07 ~ 2026.07`
HR 담당자가 복지성 선물을 알림톡으로 대량 발송하는 B2B 복지몰 신사업
- 주문 V2 정책(즉시/예약/기념일 발송, 주문 타입별 금액 계산·충전금/PG 분배·환급 산식) 구현
- **전시·마케팅 공통 엔진** — ContentType 기반 엔진 + 타입별 Validator, 새 전시 기능은 타입 정의만으로 추가
- 넥스트키 락 범위를 인덱스 컬럼 순서로 한정, 데드락 재시도 AOP
- Redis **시간대별 키 캐시**로 전시 시작·종료 배치 0개

`Spring Boot` `MyBatis` `MariaDB` `Redis` `Vue 3` `Pinia` `CoreUI`

### 애드콘 배송 실물상품 도입 · 반응형 전환 `2026.08 ~ 현재`
모바일 쿠폰·상품권 B2C/B2B 서비스에 배송 상품 도입, PC/모바일 화면 반응형 전환
- 기존 ERD(107개 테이블·1,042개 컬럼) 분석 후 재설계, 레거시 Controller의 REST API 전환 설계·팀 가이드
- 전시·메인·상품목록·검색·주문내역·어드민 주문관리 전반 개발, 수신자별 안분 기준 환급 계산
- **조회 성능 개선** — 주문내역 첫 조회 3.2초 → 0.2초(약 16배), 검색바 추천 쿼리 297ms → 66ms

`JSP` `jQuery` `Spring Boot` `MyBatis` `MariaDB` `REST API`

👉 **[상세 수행 내역 보기 (문제 → 해결 → 효과)](docs/work.md)**

---

## 🤖 AI

| 프로젝트 | 내용 |
|---|---|
| **DO-AUI** | 그룹웨어 AI 커스텀 대시보드 PoC (동기들과 진행한 AI 사이드 프로젝트). 채팅 요청 → Claude tool use(ReAct)로 API 카드 지목 → 서버가 대신 실행 → 선언형 UI(A2UI) 설계도 검증·저장 → 재조회 시 AI 호출 0회. 사내 API 카드 175장 + 외부 커넥터 3종, 설계도 검증 규칙 144개 |
| **AI 보안 점검 · PR 리뷰** | 소스 분석 + 화면 유즈케이스 이중 보안 점검 체계 설계, 체크리스트·프롬프트 표준화로 타 서비스 확산, PR AI 리뷰 자동화 도입 |
| **연수** | Build with Gemini Seoul 2026 (Google Cloud) 핸즈온 참석 및 결과보고 |

👉 **[AI 경험 상세 보기](docs/ai.md)**

---

## 🛠 Skills

| 수준 | 기술 |
|---|---|
| **실무 주력**<br><sub>분석·설계·구현·운영·장애 대응</sub> | Java, Spring Boot, Spring MVC · JPA, Querydsl · MyBatis · MariaDB · REST API(FeignClient, HttpExchange, RestClient, Spring Cloud Gateway) · Vue.js 2/3, Pinia, CoreUI, JSP, jQuery |
| **실무 활용**<br><sub>설계 참여·기능 단위 구현</sub> | RabbitMQ · Redis · GCP(GKE, GCS) · LLM 애플리케이션(Claude API tool use, JSON Schema, SSE, A2UI) |
| **경험**<br><sub>학부·인턴</sub> | Python(크롤링, Mecab NLP), C, Android, Go, React, NEXCORE |
| **협업** | Git, Bitbucket, Redmine, Jira, Figma, Notion, Slack |

👉 **[보유 기술 수준 상세 보기](docs/skills.md)**

---

## 📜 Experience

| 기간 | 내용 |
|---|---|
| 2024.02.13 ~ | **다우기술** 웹어플리케이션 개발 (Full-Stack) |
| 2023.12.27 ~ 2024.02.13 | **KB데이타시스템** 어플리케이션 개발 인턴 (Back-End) |
| 2023.07.24 ~ 2023.10.13 | **KB국민은행** IT 플랫폼 개발 인턴 (Full-Stack) |
| 2022.10.31 ~ 2022.11.03 | LG CNS 아키텍처 담당 'IT 아키텍처 전문가 양성 특강' 수료 |
| 2022.09 ~ 2022.12 | 대학교 연합동아리 UMC 3기 교내 지부 Spring Boot 파트장 |
| 2022.03 ~ 2022.08 | 대학교 연합동아리 UMC 2기 교내 지부 Spring Boot B팀 리더 |
| 2022.01 ~ 2022.02 | 이미지연구실 학부연구생 |
| 2022.01.14 ~ 2022.01.28 | 교내 공학교육 혁신센터 "2021년 파이썬을 활용한 AI 딥러닝" 심화과정 수료 |
| 2021.01.11 ~ 2021.01.22 | 삼성 SDS 동계 대학생 알고리즘 특강 수료 |

👉 **[인턴 · 대외활동 · 학부 프로젝트 상세 보기](docs/activities.md)**

---

## 🏅 Certificates
- 정보처리기사
- SQLD
