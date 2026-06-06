# 안녕하세요, 민병욱입니다!

[![GitHub](https://img.shields.io/badge/GitHub-byungwook--dev-181717?style=flat-square&logo=github)](https://github.com/byungwook-dev)
[![Portfolio](https://img.shields.io/badge/Portfolio-Notion-000000?style=flat-square&logo=notion)](https://app.notion.com/p/by-Byungwook-dev-36505e05fc2f80cd831cd45ef9059112)
![Visitor](https://komarev.com/ghpvc/?username=byungwook-dev&style=flat-square&color=orange)

---

## 🧑‍💻 About Me

- 🎓 명지대학교 문헌정보학과 졸업 (2026.02)
- 📚 코리아IT아카데미 수료 (894.5시간, 2022.09 ~ 2025.09)
- 🌏 OPIc IH (Intermediate High)
- 🪖 육군 병장 만기제대 (2020.05 ~ 2021.11)
- 📍 서울 거주

---

백엔드(Node.js, Spring Boot)부터 프론트엔드(React, Next.js), AI 연동(LangChain, Claude API, RAG), 클라우드 배포(Docker, AWS, GitHub Actions)까지 서비스 전체 흐름을 설계하고 구현합니다.

---

## 🛠️ Tech Stack

### Backend
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=flat-square)

### Frontend
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Redux](https://img.shields.io/badge/Redux-764ABC?style=flat-square&logo=redux&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38BDF8?style=flat-square&logo=tailwindcss&logoColor=white)
![Styled Components](https://img.shields.io/badge/Styled_Components-DB7093?style=flat-square&logo=styledcomponents&logoColor=white)

### Database
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle_DB-F80000?style=flat-square&logo=oracle&logoColor=white)

### AI / NLP
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Claude API](https://img.shields.io/badge/Claude_API-CC785C?style=flat-square)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

### DevOps / Cloud
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)

---

## Projects

### 1. ShowU — 예술가와 팬을 연결하는 통합 플랫폼

**Tech:** `React 18.3` `Redux 5.0` `Express 4.21` `Mongoose 8.9` `MongoDB Atlas` `Toss Payments SDK 2.3` `k6 0.55.0`

공연 티켓 예매, 공간 대여, 굿즈/경매 쇼핑, VOD 스트리밍, 커뮤니티를 통합한 예술 특화 플랫폼.
Reservation 도메인 풀스택 + 경매/굿즈 결제 파트 담당.

| 지표 | 개선 전 | 개선 후 |
|------|--------|--------|
| 동시 200명 중복 예약 | 9건 ❌ | 0건 ✅ |
| 결제 금액 위변조 | 통과 ❌ | FORBIDDEN_REQUEST(403) ✅ |
| WriteConflict 에러 코드 | 500 ❌ | 400 ✅ |

- k6 동시 200명 부하테스트로 Race Condition 재현 → MongoDB Unique Index + 트랜잭션으로 중복 예약 0건 달성
- `mongoose.startSession()`으로 Seat/Rental 두 컬렉션 원자적 저장 → 부분 저장 케이스 제거
- Toss Payments 서버사이드 검증(`/v1/payments/confirm`) → Postman 재현: 340,000원→1,000원 조작 시 403 차단

**GitHub**: [front-showu](https://github.com/byungwook-dev/front-showu) · [back-showu](https://github.com/byungwook-dev/back-showu)

---

### 2. PrivateGPT — 완전 로컬 기반 문서 RAG 챗봇

**Tech:** `Python` `LangChain 1.3.1` `Ollama (Mistral)` `FAISS` `CacheBackedEmbeddings` `Streamlit`

외부 API 없이 로컬에서만 동작하는 문서 기반 RAG 챗봇.
5개월 LangChain/RAG/NLP 학습 후 9개 챗봇 프로젝트 중 프라이버시와 성능 최적화에 집중한 대표 프로젝트.

| 지표 | 개선 전 | 개선 후 |
|------|--------|--------|
| 임베딩 처리 시간 | 118.27초 ❌ | 0.09초 ✅ |
| 속도 개선율 | — | 99.9% |

- OpenAI API 대신 Ollama + Mistral 로컬 모델 → 데이터 외부 전송 없는 프라이버시 보장 구조
- `CacheBackedEmbeddings`로 임베딩 캐싱 → 처리 시간 118.27초 → 0.09초 (99.9% 단축)
- `condense_llm`으로 이전 대화 반영한 질문 재구성 → 맥락 단절 문제 해결
- `similarity_score_threshold` 적용 → 관련성 낮은 컨텍스트 제외, 할루시네이션 감소

**GitHub**: [NLP/09_PrivateGPT](https://github.com/byungwook-dev/NLP/tree/main/09_PrivateGPT)

---

### 3. TeamBuilder AI — AI 기반 지능형 팀/반 자동 배정 시스템

**Tech:** `Next.js 16` `TypeScript` `Claude Sonnet 4 API` `Docker` `AWS EC2` `GitHub Actions`

> 제1회 K.I.T. 바이브코딩 공모전 출품작 (506팀 참가)

교육기관의 수작업 팀/반 배정을 AI로 자동화한 웹 서비스.
기획 총괄 + AWS 배포 자동화(CI/CD 파이프라인 구축) 담당.

| 지표 | 개선 전 | 개선 후 |
|------|--------|--------|
| 배포 성공률 | ~70% ❌ | 100% ✅ |
| 평균 배포 시간 | 수동 SSH | 약 2분 ✅ |
| EBS 용량 | 7.6GB | 30GB ✅ |
| 팀 균형 점수 | — | 95.4점 ✅ |

- GitHub Actions 86회 중 26회 실패 → `fetch-depth:0` + `--no-cache` 표준화, 9개 Secrets 관리 → 성공률 100%
- `ANTHROPIC_API_KEY` Dockerfile ARG 제외 → 런타임 전용 주입으로 이미지 레이어 키 노출 방지
- Silent Failure(exit 0인데 구버전 유지) → `docker images`로 누적 이미지 원인 특정, EBS 30GB 무중단 확장
- 6단계 하이브리드 알고리즘 + Claude Sonnet 4 병렬 실행 → 균형 점수 95.4점, 팀 간 성적 차이 0.1점

**배포**: http://3.35.27.169/ · **GitHub**: [byungwook-dev/Sensitive](https://github.com/byungwook-dev/Sensitive)

---

## 📜 Certifications

| 자격증 | 발급 기관 | 취득일 |
|--------|----------|--------|
| 정보처리기사 | 한국산업인력공단 | 2025.12.28 |
| SQLD (SQL 개발자) | 한국데이터산업진흥원 | 2025.12.12 |
| Microsoft Certified: Azure AI Fundamentals | Microsoft | 2024.09.21 |
| Microsoft Certified: Azure Data Fundamentals | Microsoft | 2024.09.21 |

---

## 📚 Education & Training

### 코리아IT아카데미 (총 894.5시간, 2022.09 ~ 2025.09)

| 과정 | 기간 | 시간 |
|------|------|------|
| JAVA 1~2 | 2022.09 ~ 2022.11 | 60h |
| Python | 2023.01 ~ 2023.02 | 32h |
| 웹개발 2~4 (SpringBoot, MyBatis, OracleDB) | 2023.07 ~ 2023.10 | 162h |
| 웹개발 4~6 (React, JS, Node.js, MongoDB) | 2024.02 ~ 2024.05 | 162h |
| 프론트엔드 1~6 | 2024.07 ~ 2025.01 | 180h |
| AI활용 자연어처리 챗봇 1~6 (Python, RAG, HuggingFace) | 2025.01 ~ 2025.07 | 180h |
| 멀티클라우드 1 (Docker, Kubernetes) | 2025.08 | 59.5h |
| 멀티클라우드 2 (AWS) | 2025.09 | 59.5h |

### 대학교

| 학교 | 전공 | 기간 |
|------|------|------|
| 명지대학교 | 문헌정보학과 | 2019 ~ 2026.02 졸업 |
