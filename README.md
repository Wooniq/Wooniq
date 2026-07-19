<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2B3A67,100:4F8EF7&height=180&section=header&text=Han%20JiWoon&fontSize=50&fontColor=ffffff&fontAlignY=30&desc=Backend%20Engineer&descAlignY=48&descSize=18&animation=fadeIn" width="100%"/>
안녕하세요, 백엔드 엔지니어 한지운입니다 👩🏻‍💻

**101%의 성능 향상보다, 1%의 오차를 남기지 않는 데 집중합니다.**

</div>
<br>

</div>

<br>

## About

**분산 시스템**과 **AI 파이프라인**을 결합해, 남들이 시도하지 않았던 데이터 흐름도 설계해 냅니다.

- Outbox Pattern 적용을 통한 MSA 환경 데이터 정합성 및 이벤트 유실 리스크 최소화
- CQRS 및 Debezium CDC 기반 PostgreSQL-MongoDB 이기종 데이터 실시간 동기화 구조 구현
- GraphDB-LLM을 연계한 GraphRAG 기반 문서 질의응답 구조 설계 및 논문 등재
- Kubernetes · Jenkins · ArgoCD 기반 GitOps 배포 자동화 및 온프레미스 운영 환경 구축

<br>

## Education & Certification

- Hansung University, Computer Engineering, GPA 3.76/4.5 (2022.03 ~ 2026.08)
- 정보처리기사 (2025.09)
- TOEIC Speaking IM3 (2026.03)

<br>

## Projects

<details>
<summary><b>Wanderpool — MSA 기반 On-Premise 카풀 예약 서비스, 2026.04 ~ 2026.06</b></summary>
<br>

Private GitLab, Harbor, Jenkins, ArgoCD 기반 온프레미스 환경에서 구축한 MSA 기반 카풀 예약 서비스입니다. gRPC, Outbox Pattern, Istio를 적용해 서비스 간 통신과 데이터 정합성을 함께 고려했습니다.

**주요 성과**
- 4개 마이크로서비스와 Kong API Gateway 기반의 MSA 환경을 구축했습니다.
- GitOps 배포 파이프라인을 구축하고 Kubernetes 자동 배포 환경을 구현했습니다.
- Kong API Gateway로 외부 요청 라우팅과 JWT 검증 흐름을 중앙화했습니다.
- Istio Service Mesh로 서비스 간 호출 지연을 1~4ms 수준으로 관찰하고 트래픽 가시성을 확보했습니다.

**핵심 기여**
- Outbox Pattern을 적용해 상태 변경과 외부 서비스 호출 간 데이터 불일치 가능성을 완화했습니다.
- gRPC와 Protobuf를 도입해 서비스 간 통신 계약을 명확히 하고 내부 호출 구조를 표준화했습니다.
- Request ID와 재시도 정책을 적용해 중복 환불 위험을 줄이고 실패 요청의 추적 가능성을 확보했습니다.
- 인증 검증 책임을 API Gateway로 분리해 개별 서비스의 인증 처리 부담을 완화했습니다.

</details>

<details>
<summary><b>Watt-Up — 전기차 충전소 예약 플랫폼, 2026.02 ~ 2026.03</b></summary>
<br>

CQRS와 Debezium CDC를 적용해 조회와 예약 워크로드를 분리한 전기차 충전소 예약 플랫폼입니다. Kafka 기반 CDC 파이프라인으로 PostgreSQL-MongoDB 간 실시간 조회 모델 동기화를 구현했습니다.

**주요 성과**
- 12,000여 건의 충전소 데이터를 활용한 예약 플랫폼을 구축했습니다.
- CQRS 패턴을 적용해 조회 트래픽과 예약 생성 요청을 분리했습니다.
- Debezium CDC와 MongoDB 동기화 모듈 기반 실시간 데이터 동기화 파이프라인을 구축했습니다.

**핵심 기여**
- Debezium CDC로 PostgreSQL 변경 데이터를 Kafka 이벤트로 전파하는 데이터 파이프라인을 구현했습니다.
- PostgreSQL과 MongoDB 간 이기종 데이터베이스 동기화로 CQRS 아키텍처를 구현했습니다.
- Kafka 기반 이벤트 처리 구조를 설계해 서비스 간 결합도를 낮추고 확장성을 확보했습니다.
- Jenkins, Docker Hub를 활용한 CI/CD 파이프라인을 구축했습니다.

</details>

<details>
<summary><b>OTA 사전 검증 프로젝트 — 현대오토에버 클라우드 개인 프로젝트, 2026.02 ~ 2026.04</b></summary>
<br>

커넥티드카 백엔드가 차량 소프트웨어 신뢰성에 직접 관여한다는 문제의식에서 출발한 OTA(Over-the-Air) 업데이트 사전 검증 시스템입니다. 차량에서 수집된 ECU 인벤토리 데이터를 정규화하고, 업데이트 패키지의 배포 가능 여부를 판단하는 검증 로직을 구현했습니다.

**주요 성과**
- ECU 인벤토리 데이터 정규화 및 업데이트 패키지 버전·의존성 규칙 기반 검증 로직을 구현했습니다.
- Kafka 기반 비동기 파이프라인으로 차량 상태, 검증 결과, 실패 사유를 이력화하는 체계를 구축했습니다.
- 차량 소프트웨어 신뢰성이 차량 내부 로직뿐 아니라 백엔드의 검증 설계에도 좌우된다는 인사이트를 도출했습니다.

**핵심 기여**
- 차량에서 수집된 ECU 인벤토리 데이터를 정규화하는 로직을 구현했습니다.
- 업데이트 패키지의 버전과 의존성 규칙을 비교해 배포 가능 여부를 판단하는 검증 로직을 구현했습니다.
- Kafka 기반 비동기 파이프라인으로 차량 상태 데이터와 검증 결과, 실패 사유를 이력화했습니다.

</details>

<details>
<summary><b>기업 화상회의 AI 어시스턴트 — Backend, 2025.03 ~ 2025.05</b></summary>
<br>

GraphDB와 Gemini LLM을 연동해 기업 화상회의 중 실시간으로 회의 내용을 기록하고 질의응답까지 지원하는 AI 어시스턴트 시스템입니다.

**주요 성과**
- GraphDB와 Gemini LLM을 연동한 AI 기반 회의 어시스턴트 시스템을 개발했습니다.
- 자동 회의록 생성, 할 일 추출, 캘린더 연동, 화면 공유 모듈을 구현했습니다.
- GraphRAG 기반 지식 그래프와 실시간 컴포넌트를 AWS 환경에 분산 구축했습니다.

**핵심 기여**
- 회의 중 발화 내용을 기반으로 실시간 QA가 가능한 구조를 설계했습니다.
- GraphRAG 기반 지식 그래프로 회의 맥락과 근거를 연결한 질의응답 흐름을 구현했습니다.

</details>

<details>
<summary><b>GraphRAG 기반 EPUB 리더기, 2024.08 ~ 2025.02</b></summary>
<br>

EPUB 문서를 GraphDB에 지식 그래프로 구조화하고 LLM 질의응답과 연결한 문서 기반 AI 리더기입니다. 기존 키워드 검색이 문서 간 관계와 추론 질문을 처리하지 못하는 한계를 보완하기 위해 GraphRAG 구조를 설계했습니다.

**주요 성과**
- 500페이지 도서와 30여 개 학칙 파일 기반 문서 질의응답 기능을 구현했습니다.
- 문서 기반 질의응답 정확도 95%를 확인했습니다.
- GraphML 렌더링 구조 개선으로 시각화 시간을 20초대에서 4초대로 단축했습니다.
- KCI 논문 등재 및 SW중심대학 연합 SW FESTIVAL 3위를 수상했습니다.

**핵심 기여**
- EPUB 데이터 추출 및 문서 구조 분석 파이프라인을 구현했습니다.
- 문서를 노드와 관계로 변환해 GraphDB에 적재하는 지식 그래프 구조를 설계했습니다.
- GraphDB 검색 결과를 LLM 질의응답과 연결해 근거 기반 답변 흐름을 구현했습니다.
- GraphML을 브라우저에서 직접 렌더링하도록 개선해 그래프 시각화 성능을 개선했습니다.

</details>

<br>

## Experience

<details>
<summary><b>SSAFY 16기 (Java Track) — Backend, 2026.07 ~ 현재</b></summary>
<br>

- 알고리즘·코딩 테스트 훈련을 통해 문제 해결 능력을 강화하고 있습니다.
- Java, Spring Boot, REST API, 관계형 데이터베이스 기반 백엔드 애플리케이션을 개발하고 있습니다.
- 애자일 협업 방식으로 팀 프로젝트를 수행하고 있습니다.

</details>

<details>
<summary><b>현대오토에버 모빌리티 SW 스쿨 (Cloud Track 3기), 2025.12 ~ 2026.06</b></summary>
<br>

- MSA 기반 모빌리티 서비스를 Spring Boot로 설계·구현했습니다.
- Kubernetes 배포 환경과 GitOps 파이프라인을 직접 구축했습니다.
- gRPC 통신과 이벤트 기반 아키텍처로 서비스 간 연동을 설계했습니다.
- **모범상 및 우수 프로젝트상 2회 수상** (WanderPool, Watt-Up)

</details>

<details>
<summary><b>학부 연구생 — GraphRAG 기반 EPUB 리더 연구, 2024.08 ~ 2025.02</b></summary>
<br>

- 지식 그래프 모델링 기반의 GraphRAG 질의응답 시스템을 개발했습니다.
- 문서 내 개체 간 관계를 추출·관리하는 데이터 파이프라인을 설계했습니다.
- Neo4j 기반 시각화로 결과를 설명 가능한 형태로 제공했습니다.
- 연구 결과를 KCI 등재 학술지에 게재했습니다.

</details>

<details>
<summary><b>컴퓨터공학과 조교, 2025.09 ~ 2025.12</b></summary>
<br>

- HTML, CSS, JavaScript 기반 웹 프로그래밍 실습을 지원했습니다.
- 팀 프로젝트 중 발생하는 구현 이슈의 디버깅을 도왔습니다.
- 과제 평가 및 학생 개발 역량 향상을 지원했습니다.

</details>

<details>
<summary><b>멋쟁이사자처럼 한성대 (Backend Track), 2024.03 ~ 2024.12</b></summary>
<br>

- Spring Boot와 REST API 설계 원칙 기반 백엔드 서비스를 개발했습니다.
- 데이터베이스 스키마를 설계하고 CRUD 기능을 구현했습니다.
- Git 기반 협업 워크플로우로 팀 프로젝트를 수행했습니다.

</details>

<details>
<summary><b>HSD 셔틀버스 앱 서버 유지보수, 2024.06 ~ 2024.12</b></summary>
<br>

- 교내 셔틀버스 앱의 백엔드 서비스를 유지보수하고 기능을 개선했습니다.
- API 연동, 서버 모니터링, 운영 이슈 대응을 담당했습니다.
- 예외 처리 개선과 불필요한 서버 연산 제거로 서비스 안정성을 높였습니다.

</details>

<br>

## Publications

- EPUB 리더기의 GraphRAG 활용에 관한 연구 · [PDF](https://github.com/user-attachments/files/17943916/EPUB.GraphRAG.pdf)
- GraphRAG를 활용하여 뛰어난 검색과 추론 기능을 가진 EPUB 리더 (KCI 등재) · [PDF](https://github.com/user-attachments/files/18278657/GraphRAG.EPUB.pdf) · [KCI Link](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART003160624)

<br>

## Awards

- 2026.06 현대오토에버 모빌리티 SW 스쿨 3기 모범상 · 우수 프로젝트상 2회
- 2025.05 한성발전공헌상
- 2025.02 한성대학교 C&C Festival 대상
- 2024.11 SW중심대학 연합 SW FESTIVAL 장려상
- 2024.09 한성대학교 공학경진대회 은상
- 2024.05 한성대학교 교내 해커톤 최우수상

<br>

## Skills

**Languages & Backend**

<p>
<img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=java&logoColor=white">
<img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white">
<img src="https://img.shields.io/badge/Spring-6DB33F?style=flat-square&logo=spring&logoColor=white">
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white">
<img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white">
<img src="https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white">
<img src="https://img.shields.io/badge/gRPC-0F9D58?style=flat-square&logo=google&logoColor=white">
<img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white">
</p>

**Databases**

<p>
<img src="https://img.shields.io/badge/MySQL-00f?style=flat-square&logo=mysql&logoColor=white">
<img src="https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white">
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white">
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white">
<img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white">
<img src="https://img.shields.io/badge/Neo4j-00CC96?style=flat-square&logo=neo4j&logoColor=white">
<img src="https://img.shields.io/badge/ArangoDB-007ACC?style=flat-square&logo=arangodb&logoColor=white">
</p>

**Cloud / Infra & DevOps**

<p>
<img src="https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white">
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white">
<img src="https://img.shields.io/badge/Docker-0db7ed?style=flat-square&logo=docker&logoColor=white">
<img src="https://img.shields.io/badge/Istio-466BB0?style=flat-square&logo=istio&logoColor=white">
<img src="https://img.shields.io/badge/Kong-003459?style=flat-square&logo=kong&logoColor=white">
<img src="https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white">
<img src="https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white">
<img src="https://img.shields.io/badge/GitLab-FC6D26?style=flat-square&logo=gitlab&logoColor=white">
<img src="https://img.shields.io/badge/Harbor-60B932?style=flat-square&logo=harbor&logoColor=white">
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black">
</p>

**Monitoring & Tools**

<p>
<img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white">
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white">
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white">
<img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white">
<img src="https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=figma&logoColor=white">
</p>

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=agn705)](https://solved.ac/agn705/)

<br>

## GitHub Stats

<p>
<img src="https://github-stats-extended.vercel.app/api?username=Wooniq&show_icons=true&theme=default&hide_border=true&bg_color=ffffff&icon_color=000000&text_color=333333&title_color=007ACC&count_private=true" width="56%">
<img src="https://github-stats-extended.vercel.app/api/top-langs/?username=Wooniq&layout=donut&show_icons=true&theme=default&hide_border=true&bg_color=ffffff&icon_color=000000&text_color=333333&title_color=007ACC&count_private=true&exclude_repo=Face-Transfer-Application&hide=html,css" width="38%">
</p>

<br>

## Interests

클라우드 네이티브 시스템, 대규모 데이터 · RAG/GraphRAG 아키텍처, 그리고 모빌리티/커넥티드 서비스를 위한 지능형 플랫폼에 관심이 있습니다.
