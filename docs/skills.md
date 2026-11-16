[← README로 돌아가기](../README.md)

# 🛠 보유 기술 수준

## 실무 주력
> 분석·설계·구현·운영·장애 대응까지 수행

### Java, Spring Boot, Spring MVC `3개 프로젝트 · 2년 9개월`
- **트랜잭션 경계 설계** — `@Transactional`, `@TransactionalEventListener(AFTER_COMMIT / AFTER_ROLLBACK)`
- **Spring AOP 커스텀 어노테이션 설계** — 프로비저닝 공통 흐름, 데드락 재시도, 서버 간 예외 변환
- **이벤트·비동기** — `@Async`, 전용 스레드풀(기본 5 · 최대 10 · 대기열 1만), 배치·스케줄러
- **설계 패턴 적용** — 전략, 템플릿 메서드, 레지스트리, 타입별 빈 구성(`@Configuration` · `@Qualifier`)

### JPA·Querydsl `약 1년 6개월` / MyBatis `약 1년 4개월`
- 프로젝트마다 다른 영속성 스택에 적응
- 동적 쿼리·CTE·윈도 함수, sqlSession 직접 호출 → Mapper 인터페이스 전환

### RDB (MariaDB)
- **ERD 설계** — 도메인 경계 10개 이상 정의 / 107개 테이블·1,042개 컬럼 분석 후 재설계
- **동시성** — 인덱스 컬럼 순서 설계로 락 범위 한정, `SELECT … FOR UPDATE`, 넥스트키 락 이해, 데드락 재시도
- **튜닝** — 실행계획 기반 튜닝(첫 조회 3.2초 → 0.2초, 쿼리 297ms → 66ms), 쿼리 캐시 동작 분석

### REST API 설계·연동
- FeignClient, HttpExchange, RestClient, Spring Cloud Gateway
- 레거시 Controller의 REST API 전환 설계·가이드, 쿠폰/배송 공용 REST API 통합, 외부 쇼핑몰 BO REST 연동

### 프론트엔드
- Vue.js 2/3(Pinia, CoreUI), JSP·jQuery — 화면 개발, 반응형 전환, 상태 저장소 설계

---

## 실무 활용
> 설계에 참여하고 기능 단위로 구현

| 기술 | 내용 |
|---|---|
| **RabbitMQ** | fanout 이벤트 발행 보장(이력 테이블·revisionId 멱등·재발행), 성공/실패 회신 큐, 리스너 에러 핸들러 |
| **Redis** | 시간대별 키 캐시, TTL·evict 정책 설계 |
| **GCP** | GKE(Kubernetes) 배포 환경에서의 개발·장애 분석(ingress → gateway → 서비스 요청 경로), GCS(임시/퍼블릭 버킷 이동, 보상 트랜잭션) |
| **LLM 애플리케이션** | Claude API tool use(ReAct 루프), JSON Schema 검증, SSE 스트리밍, A2UI(선언형 UI 프로토콜) — PoC 설계·프로토타입 구현 |
| **AI 활용** | AI PR 리뷰, AI 보안 점검 프롬프트 표준화 |
| **네트워크** | nginx 프록시 구간의 HTTP chunked/Content-Length 불일치로 인한 5xx 원인 규명 |

---

## 경험
> 학부·인턴 수준

- Python(크롤링, Mecab 형태소 분석 기반 NLP), C, Android, Go, React, NEXCORE(금융 프레임워크)

---

## 협업 도구
- Git, Bitbucket(PR 기반 협업), Redmine, Jira, Figma, Notion, Slack

## 자격
- 정보처리기사
- SQLD

---

[← AI 경험](ai.md) · [README로 돌아가기](../README.md) · [인턴·활동 →](activities.md)
