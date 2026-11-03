# 안녕하세요, 지규인입니다 👋

### 분산 시스템에서 **트랜잭션을 "어떤 순서로" 처리할지** 연구하고 구현해 온 백엔드 · 인프라 엔지니어

Hyperledger Fabric 위에서 **트랜잭션 재정렬로 처리량 높이기** → **트랜잭션 의존성 분석 기반 Orderer(TD-Orderer)** → **서비스 의도를 이해하는 AI 에이전트 기반 트랜잭션 순서 결정**까지,
학부 연구생부터 석사까지 하나의 문제를 단계적으로 발전시켜 왔습니다.
연구에서 끝내지 않고 **특허 · SW 저작권으로 남기고, 실무에서 CI/CD 파이프라인까지 직접 구축**해봤습니다.

- 🔬 **SCI(IEEE Access) · KCI · 국제학회(ICTC)** 포함 논문 6편 · 특허 출원 1건 · SW 저작권 2건
- 🏢 인턴 3회: 포항공대 MCNL · 인천대 DWEB · **모비젠 아키텍처팀(사내 인프라 CI/CD 구축)**
- 🧑‍🏫 블록체인 칼리지 · 웹 프로그래밍 수업 조교
- 🤖 **AI 에이전트** (CrewAI · MCP · n8n)를 연구와 자동화 워크플로에 직접 적용
- 🌱 지금은 **Spring Boot 백엔드**와 **배포 · 운영** (CI/CD, Kubernetes, 모니터링, 장애 대응)을 직접 만들면서 공부하고 있습니다

---

## 🛠 Tech Stack

**Language**
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

**Backend / Database**
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**Distributed System / Blockchain**
![Hyperledger Fabric](https://img.shields.io/badge/Hyperledger%20Fabric-2F3134?style=flat-square&logo=hyperledger&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)

**AI Agent**
![CrewAI](https://img.shields.io/badge/CrewAI-FF5A50?style=flat-square&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square&logo=modelcontextprotocol&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)

**Frontend / Mobile**
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![React Native](https://img.shields.io/badge/React%20Native-20232A?style=flat-square&logo=react&logoColor=61DAFB)

**Infra / DevOps**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)

---

## 🚀 Featured Projects

### 연구

| 프로젝트 | 설명 | 성과 |
|---|---|---|
| **AI Agent Transaction Sequencer** | 서비스 의도(intent)를 인지하는 AI 에이전트가 트랜잭션 순서를 결정하는 허가형 블록체인 시퀀서 (CrewAI · Hyperledger Fabric) | **IEEE Access (SCI)** · KCI 게재 · SW 저작권 등록 |
| **[TD-Orderer](https://github.com/jhikyuinn/Serializer)** | 트랜잭션 의존성 분석으로 충돌을 줄이는 Hyperledger Fabric Orderer | **ICTC** 발표 · 특허 출원 · SW 저작권 등록 |
| [Serializer Extended](https://github.com/jhikyuinn/Serializer-extended) | Fabric 트랜잭션 충돌을 블록에 넣기 전에 Kafka 정렬 서비스에서 풀고, 버린 기록은 BFT 합의망에 남기는 외부 정렬 서비스. 연구 이후 고가용성과 AWS 실험까지 확장 | AWS 1,000 TPS에서 Fabric 대비 성공 처리량 ×1.31~2.98 · 장애 복구 11.8 s → 5.4 s |

### 개인 프로젝트

| 프로젝트 | 설명 | 상태 |
|---|---|---|
| **[FootPrint](https://github.com/jhikyuinn/FootPrint)** | 대화는 P2P DB(GunDB)에, 대화 해시는 Hyperledger Fabric에 기록해 대화 기록이 바뀌지 않았는지 확인하는 메신저. 메시지 서명 검증, 앱 없이 검증 가능한 회의록 내보내기, 메시지가 많은 방의 로딩 측정 · 개선 | 동국대 컴퓨터공학과 **최우수 논문상** (2022) · 2026 개선 중 |
| **Fairslot** | 네트워크 지연과 상관없이 한정된 자원을 공정하게 배분하는 시스템. 첫 시나리오는 티켓팅. 지연 시간별 당첨률 측정, 초과 판매 방지 · 멱등성, Kafka 이벤트, Kubernetes · GitOps · 모니터링까지 직접 운영 (Spring Boot · PostgreSQL · Redis · Kafka) | 🚧 진행 중 (reservation-service) |
| **[오늘의 자격증](https://github.com/jhikyuinn/Todaycertificate)** | 시험일, 과락 위험 과목, 오답을 바탕으로 오늘 풀 기출 문제를 골라 주는 국가자격 필기 학습 앱. 2022년 Express + MySQL 앱을 Spring Boot + PostgreSQL로 다시 만드는 중 | 🚧 진행 중 |
| 일본어 학습 자동화 | n8n이 매일 일본 뉴스를 모으면, AI 에이전트가 낯선 단어를 뽑아 MCP로 연결한 Notion 단어장에 없는 단어만 뜻 · 예문과 함께 추가하고, 기사를 음성으로 바꿔 청해 연습에 사용 | 매일 사용 중 · 개인화 개선 예정 |

---

## 📄 Publications

- **[SCI]** AI Agent-Based Blockchain Transaction Sequencer for Intent-Aware Transaction Ordering, *IEEE Access*, 2026 — 1저자
- **[KCI]** 허가형 블록체인을 위한 서비스 인지형 AI 에이전트 기반 트랜잭션 순서 결정 기법, *정보과학회 컴퓨팅의 실제 논문지* 32권 5호, 2026 — 1저자
- **[Int'l Conf.]** TD-ORDERER: Transaction Dependency Orderer, *ICTC*, 2025 — 1저자
- **[Domestic]** MLOps 환경의 AI 모델 및 데이터 신뢰성 보장을 위한 블록체인 기술, *KSC 2025* — 2저자
- **[Domestic]** 트랜잭션 재정렬을 통한 하이퍼레저 패브릭의 처리량 향상, *KSC 2024* — 1저자
- **[M.S. Thesis]** A Study on Transaction Reordering Techniques in the Hyperledger Fabric Platform for Enhancing Blockchain Service Satisfaction, 2025

## 🧾 Patent & Software Copyright

- **특허 출원** · 블록체인 상의 트랜잭션 처리 방법 및 장치 (10-2024-0136914, 2024.10)
- **SW 저작권** · 서비스 맞춤형 지능형 트랜잭션 정렬 시스템 (2025.12)
- **SW 저작권** · 블록체인 기반 트랜잭션 의존성 분석 및 우선순위 정렬 시스템 (2024.12)

---

## 💼 Experience

| 기간 | 소속 | 내용 |
|---|---|---|
| 2025.06 – 2025.08 | 모비젠 아키텍처팀 인턴 | Docker · Kubernetes · Jenkins로 사내 인프라 CI/CD 구축 |
| 2023.09 – 2026.02 | 국가 R&D 과제 연구원 | 노드 간 메시지 전달 · 합의 최적 경로 프로토콜 (AWS 서울 · 도쿄 20노드, TTA 인증시험 목표 8 s 대비 3.73 s 합의) · 블록체인 기반 Web 3.0 실시간 서비스 |
| 2023.09 – 2024.02 | 인천대학교 DWEB 인턴 | 블록체인 네트워크 개선 |
| 2023.01 – 2023.07 | 포항공과대학교 MCNL 인턴 | 블록체인 네트워크 개선 |
| 2022.03 – 2022.12 | 동국대학교 INLAB 학부연구생 | 블록체인 연구 |

## 🧑‍🏫 Teaching & Activities

- 인천 블록체인 칼리지 조교 — 인천테크노파크 (2025.07–08, 2025.11–12)
- 수업 조교 — 웹 프로그래밍, 블록체인 (인천대학교)
- 카인사이드아웃 · 커넥티드카 네트워크 교육 수료 — 현대엔지비 (2026.04–06)

## 🏆 Awards

- **대상** · LINC 3.0 캡스톤 디자인 경진대회 — 동국대학교 총장 (2022.12)
- **최우수 논문상** · 하이퍼레저 패브릭 블록체인 기반 P2P 채팅 애플리케이션 — 동국대 컴퓨터공학과 (2022.12)

## 🎓 Education & Certifications

- **인천대학교** 컴퓨터공학과 석사 (2024.03 – 2026.02) · GPA 4.25/4.5
- **동국대학교** 경주캠퍼스 컴퓨터공학과 학사 (2019.03 – 2023.02)
- AWS Certified Cloud Practitioner (2024.12) · OPIc IH (2025.11) · 정보처리기사 

---

## 📫 Contact
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:hnn991206@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/%EA%B7%9C%EC%9D%B8%EC%A7%80-184180367/)
