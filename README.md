# 👋 안녕하세요, 민병욱입니다!

> **사용자의 흐름을 따라가며, 작은 기능도 큰 서비스 속에서 의미 있게 만드는 개발자**

[![GitHub](https://img.shields.io/badge/GitHub-byungwook--dev-181717?style=flat-square&logo=github)](https://github.com/byungwook-dev)
![Visitor](https://komarev.com/ghpvc/?username=byungwook-dev&style=flat-square&color=orange)

---

## 🧑‍💻 About Me

- 🎓 명지대학교 문헌정보학과 졸업 (2026.02)
- 🪖 육군 병장 만기제대 (2020.05 ~ 2021.11)
- 🌏 영어 OPIc IH (Intermediate High)
- 📍 서울 거주 / 풀스택 개발자 지향

백엔드(Spring Boot, Node.js)부터 프론트엔드(React), AI 연동(LangChain, Claude API), 클라우드 배포(Docker, Kubernetes, AWS)까지 서비스 전체 흐름을 직접 설계하고 구현합니다.

---

## 🛠️ Tech Stack

### Backend
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=flat-square)

### Frontend
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38BDF8?style=flat-square&logo=tailwindcss&logoColor=white)
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-005F0F?style=flat-square&logo=thymeleaf&logoColor=white)

### Database
![Oracle](https://img.shields.io/badge/Oracle_DB-F80000?style=flat-square&logo=oracle&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

### AI / NLP
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Claude API](https://img.shields.io/badge/Claude_API-CC785C?style=flat-square)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)

### DevOps / Cloud
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

---

## 🚀 Projects

### 1. 🏆 TeamBuilder AI — AI 기반 지능형 팀/반 자동 배정 시스템
> 제1회 K.I.T. 바이브코딩 공모전 출품작

**Tech:** `Next.js 16` `TypeScript` `Claude Sonnet 4 API` `Docker` `AWS EC2` `GitHub Actions`

교육기관에서 수작업으로 진행하던 팀/반 배정을 AI로 자동화한 시스템입니다.  
6단계 하이브리드 최적화 알고리즘과 Claude API를 병렬 실행하여 균형 점수가 더 높은 결과를 자동 선택합니다.

**담당 역할:** 기획 총괄 + AWS 배포 자동화 (CI/CD 파이프라인 구축)

| 지표 | 개선 전 | 개선 후 | 효과 |
|------|--------|--------|------|
| EBS 용량 | 7.6GB | 30GB | **약 4배 확장** |
| 배포 성공률 | 60% | 100% | **실패율 0%** |
| 배포 시간 | 15~20분 | 3~5분 | **75% 단축** |
| 장애 대응 시간 | 수 분 | 수 초 | **90% 이상 단축** |
| 팀 균형 점수 | — | **95.4점** | 팀 간 성적 차이 0.1점 |

**핵심 구현 내용**
- AWS EC2 인스턴스 생성 및 EBS 볼륨 확장 (7.6GB → 30GB)
- GitHub Actions 기반 CI/CD: Docker Hub push → EC2 pull → 컨테이너 교체 자동화
- `--no-cache` 옵션 적용 및 Secrets 관리로 보안 강화
- 운영 검증 절차 정립 (`docker ps`, `docker logs`, `printenv`)

---

### 2. 🎭 ShowU — 예술 플랫폼
**Tech:** `React` `Express` `Node.js` `MongoDB`

공연 티켓 예매와 공간 대여 기능을 제공하는 예술 특화 플랫폼입니다.

**담당 역할:** 예매/결제 시스템 설계 및 구현

**핵심 구현 내용**
- 좌석·시간·날짜 **중복 예약 방지 로직** 설계 (동시성 제어)
- **토스페이먼츠 결제 연동** — 실결제 API 연동 및 결제 검증 흐름 구현
- React 기반 좌석 선택 UI 및 실시간 예약 현황 반영

---

### 3. 🏃 Connection — 스포츠 커뮤니티 플랫폼
**Tech:** `Spring Boot` `Thymeleaf` `MyBatis` `Oracle DB`

20~30대 스포츠 동호회를 위한 커뮤니티 플랫폼으로, 풀스택으로 직접 설계·구현했습니다.

**담당 역할:** 주요 기능 전담 구현

**핵심 구현 내용**
- 메인 화면, 장소 찾기, 신청서, **댓글 CRUD**, 마이페이지 등 핵심 기능 전담
- Spring Boot + MyBatis + Oracle DB 기반 서버-DB 연동 설계
- Thymeleaf 서버사이드 렌더링으로 커뮤니티 전체 흐름 구현

---

### 4. 🤖 AI 자연어처리 챗봇 프로젝트
**Tech:** `Python` `LangChain` `Streamlit` `Hugging Face` `GPT`

NLP 전 과정을 실습하며 다양한 AI 기능을 구현한 프로젝트입니다.

**핵심 구현 내용**
- 텍스트 전처리 → 토큰화 → 모델 적용 전 과정 실습
- **RAG(Retrieval-Augmented Generation)** 구조 적용 문서 요약 기능
- 유튜브 자막 기반 **영상 요약** 및 **학습용 퀴즈 자동 생성** 기능
- 외부 API 없이 로컬 환경에서 단독 실행 가능한 챗봇 구현 (의존도 최소화)

---

### 5. ☁️ 운영·배포 프로젝트
**Tech:** `Docker` `Kubernetes` `AWS`

개인 프로젝트를 실제 클라우드 환경에 배포·운영하며 DevOps 역량을 쌓았습니다.

**핵심 구현 내용**
- 애플리케이션 **컨테이너화** 및 Kubernetes **오케스트레이션**
- AWS 클라우드 빌드·배포 및 서비스 운영
- CI/CD 파이프라인 구축으로 배포 자동화

---

## 📜 Certifications

| 자격증 | 발급 기관 | 취득일 |
|--------|----------|--------|
| 정보처리기사 | 과학기술정보통신부 | 2025.12.28 |
| SQLD (SQL 개발자) | 한국데이터산업진흥원 | 2025.12.12 |
| Microsoft Certified: Azure AI Fundamentals | Microsoft | 2024.09.21 |
| Microsoft Certified: Azure Data Fundamentals | Microsoft | 2024.09.21 |

---

## 📚 Education & Training

| 과정 | 기관 | 기간 | 시간 |
|------|------|------|------|
| 멀티클라우드2 (AWS) | 코리아IT아카데미 | 2025.09 | 59.5h |
| 멀티클라우드1 (Docker, Kubernetes) | 코리아IT아카데미 | 2025.08 | 59.5h |
| AI활용 자연어처리 챗봇 프로젝트 1~6 | 코리아IT아카데미 | 2025.01 ~ 07 | 180h |
| 프론트엔드 1~6 | 코리아IT아카데미 | 2024.07 ~ 2025.01 | 180h |
| 웹개발 4~6 | 코리아IT아카데미 | 2024.02 ~ 05 | 162h |
| 웹개발 2~4 | 코리아IT아카데미 | 2023.07 ~ 10 | 162h |
| 명지대학교 문헌정보학과 | 명지대학교 | 2019 ~ 2026 | — |

---
