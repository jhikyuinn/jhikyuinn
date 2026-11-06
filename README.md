# 지규인

**백엔드 · AI Agent 엔지니어**

Spring Boot · Kafka · Kubernetes · MCP · n8n

직접 만들어 보면서 배우고, 한 문제를 끝까지 파고드는 편입니다. 학부 때부터 서비스를 직접 만들어 왔고, 석사에서는 "트랜잭션을 어떤 순서로 처리할 것인가"라는 문제 하나를 구현과 실험, 논문으로 이어서 파고들었습니다.

| 성공 처리량 (AWS 1,000 TPS) | 장애 복구 시간 | TTA 공인시험 합의 시간 | CI/CD 구축 | AI Agent 논문 |
|:---:|:---:|:---:|:---:|:---:|
| **1.31~2.98배** | **11.8초 → 5.4초** | **3.73초** (목표 8초) | 인턴 경험 | **SCI · KCI** 게재 |

---

## 만든 것

| 프로젝트 | 한 줄 소개 | 기술 | 상태 |
|---|---|---|---|
| Fairslot | 지연과 무관하게 자원을 공정하게 나누는 티켓팅 백엔드. 전체를 Java로 직접 작성하고 CI/CD·클라우드 배포 연습으로 확장 | Java, Spring Boot, PostgreSQL, Redis, Kafka | 진행 중 |
| 일본어 학습 자동화 | 뉴스를 모으면 에이전트가 모르는 단어만 Notion 단어장에 추가 | n8n, MCP, AI Agent | 매일 사용 중 |
| AI Agent Transaction Sequencer | 서비스 의도를 읽고 트랜잭션 순서를 정하는 에이전트 | CrewAI, Go | **IEEE Access · KCI** |
| [Serializer Extended](https://github.com/jhikyuinn/Serializer-extended) | 충돌 트랜잭션을 저장 전에 처리하는 정렬 서비스 | Go, Kafka, BFT | 처리량 **1.31~2.98배** |
| [FootPrint](https://github.com/jhikyuinn/FootPrint) | 대화 기록 변조를 확인하는 메신저 (혼자 개발) | React Native, GunDB | 학과 **최우수 논문상** |
| 사내 인프라 CI/CD | 모비젠 인턴으로 파이프라인 구축 | Docker, Kubernetes, Jenkins | 2025.06 – 08 |

## 깊게 파고든 문제

석사 과정 동안 하나의 문제를 단계별로 이어서 풀었습니다.

**1. 같은 데이터를 건드리는 트랜잭션이 몰리면 왜 실패하고, 순서를 바꾸면 줄일 수 있는가** ([Serializer](https://github.com/jhikyuinn/Serializer))
- 분산 원장(Hyperledger Fabric)은 충돌하는 트랜잭션이 한 블록에 몰리면 뒤쪽이 실패해 처리량이 떨어집니다.
- 처리 전에 트랜잭션 사이의 의존 관계를 분석해 재정렬하는 Orderer를 만들었고, 처리량이 **약 12%** 향상됐습니다. ICTC 발표, 특허 출원, SW 저작권으로 이어졌습니다.

**2. 연구용 구현이 실제 부하와 장애 상황에서도 버티는가** ([Serializer Extended](https://github.com/jhikyuinn/Serializer-extended))
- 정렬을 Kafka 기반 별도 서비스로 분리하고, 버려진 기록은 BFT 합의망에 남겨 유실을 막았습니다.
- AWS 1,000 TPS에서 기존 대비 성공 처리량 **1.31~2.98배**, 장애 복구 시간 **11.8초에서 5.4초**.

**3. 서비스마다 중요한 순서가 다르다면, 규칙 대신 서비스 의도를 읽게 할 수 있는가**
- CrewAI 에이전트가 서비스 의도에 맞춰 순서를 정하는 시퀀서를 설계했고, IEEE Access와 KCI에 게재했습니다.

**4. 노드가 멀리 떨어질수록 늘어나는 합의 지연을 어떻게 줄이는가** (국가 R&D)
- 메시지 전달 경로와 합의 단계를 줄이는 프로토콜을 설계하고 AWS 20노드를 여러 리전에 두고 검증했습니다. TTA 공인시험에서 목표 8초 대비 **3.73초**.

## 기술

| 분야 | 사용 기술 |
|---|---|
| 백엔드 · DB | `Spring Boot` `FastAPI` `PostgreSQL` `Redis` |
| AI Agent | `CrewAI` `MCP` `n8n` |
| 분산 시스템 · 인프라 | `Kafka` `Hyperledger Fabric` `Docker` `Kubernetes` `Jenkins` `AWS` |
| 언어 | `Java` `Go` `Python` `JavaScript` |

## 경력

| 기간 | 소속 | 한 일 |
|---|---|---|
| 2025.06 – 2025.08 | 모비젠 아키텍처팀 인턴 | Docker, Kubernetes, Jenkins로 사내 인프라 CI/CD 구축 |
| 2023.09 – 2026.02 | 국가 R&D 과제 연구원 | 합의 경로 최적화 프로토콜 개발, 분산 환경 실시간 서비스 과제 병행 |
| 2023.09 – 2024.02 | 인천대학교 DWEB 인턴 | 분산 네트워크 성능 개선 |
| 2023.01 – 2023.07 | 포항공과대학교 MCNL 인턴 | 분산 네트워크 성능 개선 |
| 2022.03 – 2022.12 | 동국대학교 INLAB 학부연구생 | 분산 시스템 연구 |

## 학력

| 학위 | 학교 · 연구실 | 기간 | 비고 |
|---|---|---|---|
| 석사 | 인천대학교 컴퓨터공학과 · Distributed Systems and Web Engineering Lab | 2024.03 – 2026.03 | 지도교수 박기석, GPA 4.25/4.5 |
| 학사 | 동국대학교 경주캠퍼스 컴퓨터공학과 | 2019.03 – 2023.02 | |

## 논문 · 특허

### 국제
| 구분 | 제목 | 학회·저널 | 연도 | 저자 |
|---|---|---|---|---|
| 저널 (SCI) | AI Agent-Based Blockchain Transaction Sequencer for Intent-Aware Transaction Ordering | *IEEE Access* | 2026 | 1저자 |
| 학회 | TD-ORDERER: Transaction Dependency Orderer | *ICTC* | 2025 | 1저자 |

### 국내
| 구분 | 제목 | 학회·저널 | 연도 | 저자 |
|---|---|---|---|---|
| 저널 (KCI) | 허가형 블록체인을 위한 서비스 인지형 AI 에이전트 기반 트랜잭션 순서 결정 기법 | *컴퓨팅의 실제 논문지* 32(5) | 2026 | 1저자 |
| 학회 | MLOps 환경의 AI 모델 및 데이터 신뢰성 보장을 위한 블록체인 기술 | *KSC* | 2025 | 2저자 |
| 학회 | 트랜잭션 재정렬을 통한 하이퍼레저 패브릭의 처리량 향상 | *KSC* | 2024 | 1저자 |

### 학위논문 · 특허 · SW 저작권
| 구분 | 제목 | 기관 | 연도 |
|---|---|---|---|
| 석사 학위논문 | A Study on Transaction Reordering Techniques in the Hyperledger Fabric Platform for Enhancing Blockchain Service Satisfaction | 인천대학교 | 2026 |
| 특허 출원 | 블록체인 상의 트랜잭션 처리 방법 및 장치 (10-2024-0136914) | 특허청 | 2024 |
| SW 저작권 | 서비스 맞춤형 지능형 트랜잭션 정렬 시스템 | 한국저작권위원회 | 2025 |
| SW 저작권 | 블록체인 기반 트랜잭션 의존성 분석 및 우선순위 정렬 시스템 | 한국저작권위원회 | 2024 |

## 수상 · 자격 · 활동

| 구분 | 내용 | 시기 |
|---|---|---|
| 수상 | LINC 3.0 캡스톤 디자인 경진대회 대상 (동국대학교 총장) | 2022.12 |
| 수상 | 컴퓨터공학과 최우수 논문상 | 2022.12 |
| 자격 | AWS Certified Cloud Practitioner, OPIc IH | 2024.12, 2025.11 |
| 조교 | 인천 블록체인 칼리지 (인천테크노파크) | 2025.07–08, 2025.11–12 |
| 조교 | 웹 프로그래밍, 블록체인 수업 (인천대학교) | 석사 재학 중 |
| 교육 | 커넥티드카 네트워크 교육 수료 (현대엔지비) | 2026.04–06 |

[hnn991206@gmail.com](mailto:hnn991206@gmail.com) · [LinkedIn](https://www.linkedin.com/in/%EA%B7%9C%EC%9D%B8%EC%A7%80-184180367/)
