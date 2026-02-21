# PRJ01 — LangChain 활용 지능형 FAQ 챗봇 애플리케이션

> AI/LLM 서비스 개발 과정 (모두의연구소) 5기 | 12주 과정 중 **1~3주차 프로젝트**

## 과정 개요

이 저장소는 **모두의연구소 AI/LLM 서비스 개발 과정 5기** 커리큘럼의 첫 번째 프로젝트(`PRJ01`)입니다.
총 12주, 60회차, 204시간 과정 중 **1~3주차(D+1 ~ D+15)**를 다루며,
LangChain 기초부터 RAG 파이프라인 구축, 프롬프트 엔지니어링, 메모리 관리까지 챗봇 개발의 전 과정을 학습합니다.

최종 목표: **주택청약 FAQ 시스템 챗봇 구현** (문서 전처리 + RAG + Gradio)

---

## 전체 커리큘럼 (12주)

| 주차 | 프로젝트 | 주제 |
|------|---------|------|
| **1~3주차** | **PRJ01** | **LangChain 활용 지능형 FAQ 챗봇** ← 현재 |
| 4~6주차 | PRJ02 | 검색형 RAG 기반 금융 상품 추천 시스템 |
| 7~9주차 | PRJ03 | 법률 문서 기반 검색 에이전트 시스템 |
| 10~12주차 | PRJ04 | 생성형 AI를 활용한 비정형 문서 기반 RAG 서비스 |

---

## PRJ01 학습 내용

### Week 1 — LangChain 기초 (D+1 ~ D+5)

| D+ | 날짜 | 학습 노드 | 노트북 |
|----|------|-----------|--------|
| 1 | 2/3 | OT + 프로젝트 안내 | — |
| 2 | 2/4 | 파이썬 클린코드 | `PRJ01_W1_001_Python_Clean_Code.ipynb` |
| 3 | 2/5 | 환경설정 / LLM 생성 원리 + OpenAI Chat Completion API | `PRJ01_W1_002_OpenAI_Chat_Completion.ipynb` |
| 4 | 2/6 | LangChain 주요 아키텍처 및 컴포넌트 | `PRJ01_W1_003_Langchain_Components.ipynb` |
| 5 | 2/7 | LangChain LCEL 문법 + Gradio 챗봇 구현 | `PRJ01_W1_004_LangSmith_LCEL.ipynb` · `PRJ01_W1_005_Gradio_Chatbot.ipynb` |

### Week 2 — 문서 처리 및 벡터 데이터베이스 (D+6 ~ D+10)

| D+ | 날짜 | 학습 노드 | 노트북 |
|----|------|-----------|--------|
| 6 | 2/10 | NLP 기초 - Tokenization + Embedding (BoW, TF-IDF, Word2Vec) | `PRJ01_W2_001_Tokenizing_Embedding.ipynb` |
| 7 | 2/11 | RAG 기본 개념 / 문서 전처리 | `PRJ01_W2_002_Simple_RAG_Pipeline.ipynb` |
| 8 | 2/12 | 문서 로더 + 텍스트 분할 | `PRJ01_W2_003_Document_Loader.ipynb` · `PRJ01_W2_004_Text_Splitter.ipynb` |
| — | 2/13, 2/19 | **휴강** | — |
| 9 | 2/20 | 임베딩(Embeddings) + 벡터 저장소(Vector Stores) | `PRJ01_W2_005_Embedding_Model.ipynb` · `PRJ01_W2_006_Vectorstore.ipynb` |
| 10 | 2/21 | RAG 체인 구성 + Naïve RAG 구현 | `PRJ01_W2_007_Retriever.ipynb` |

### Week 3 — 프롬프트 엔지니어링 및 메모리 관리 (D+11 ~ D+15)

| D+ | 날짜 | 학습 노드 | 노트북 |
|----|------|-----------|--------|
| 11 | 2/24 | 프롬프트 엔지니어링 - 효과적인 프롬프트 템플릿 설계 | _(예정)_ |
| 12 | 2/25 | 프롬프트 엔지니어링 - Zero-shot, Few-shot | _(예정)_ |
| 13 | 2/26 | 프롬프트 엔지니어링 - Chain-of-Thought (CoT) | _(예정)_ |
| 14 | 2/27 | 대화 이력 관리를 위한 메모리 구현 (Chat History) | _(예정)_ |
| 15 | 2/28 | **주택청약 FAQ 챗봇 최종 구현** (RAG + Gradio) | _(예정)_ |

---

## 기술 스택

| 분류 | 라이브러리 |
|------|-----------|
| LLM API | OpenAI GPT, Google Gemini, Groq, Ollama (로컬) |
| LLM 프레임워크 | LangChain, LCEL |
| 임베딩 | OpenAI Embeddings, HuggingFace (sentence-transformers), Ollama |
| 벡터 DB | FAISS, ChromaDB, Pinecone |
| UI | Gradio 4.x |
| 모니터링 | LangSmith, Langfuse |
| 패키지 관리 | uv |
| 런타임 | Python 3.11, Jupyter Notebook |

---

## 환경 설정

### 1. 의존성 설치

```bash
uv sync
```

### 2. 환경 변수 설정

`drafts/env_sample.md`를 참고하여 프로젝트 루트에 `.env` 파일을 생성합니다.

```env
OPENAI_API_KEY=sk-proj-...
GOOGLE_API_KEY=...
GROQ_API_KEY=...
PINECONE_API_KEY=...
LANGSMITH_API_KEY=lsv2_pt_...
LANGSMITH_PROJECT=faq_bot
LANGFUSE_SECRET_KEY=sk-lf-...
LANGFUSE_PUBLIC_KEY=pk-lf-...
LANGFUSE_HOST=https://cloud.langfuse.com
```

> `.env` 파일은 `.gitignore`에 의해 추적되지 않습니다.

### 3. Jupyter 실행

```bash
uv run jupyter notebook
```

---

## 디렉토리 구조

```
001_chatbot/
├── PRJ01_W1_*.ipynb        # Week 1 실습 노트북 (LangChain 기초)
├── PRJ01_W2_*.ipynb        # Week 2 실습 노트북 (RAG 파이프라인)
│
├── data/                   # 실습용 샘플 데이터
│   ├── *.pdf, *.txt, *.csv, *.json, *.jpg
│   └── ...
│
├── articles/               # RAG 실습용 문서
│   └── notionai.pdf
│
├── homework/               # 과제 제출 노트북
│
├── docs/                   # 프로젝트 문서
│   ├── DEPENDENCIES.md         # 의존성 관리 가이드 (Intel Mac 제약 포함)
│   ├── RAG_Experiments.ipynb   # RAG 실험 노트북
│   └── LLM과정_5기_커리큘럼.pdf
│
├── drafts/                 # 작업 중 파일 & 유틸리티 스크립트
│   ├── env_sample.md       # 환경 변수 템플릿
│   └── *.py
│
├── chroma_db/              # ChromaDB 로컬 데이터 (gitignore, 노트북 실행 시 자동 생성)
├── faiss_*_index/          # FAISS 인덱스 (gitignore, 노트북 실행 시 자동 생성)
│
├── pyproject.toml          # 프로젝트 의존성 (uv)
└── .env                    # API 키 (gitignore)
```

---

## Intel Mac 사용자 주의사항

이 프로젝트는 **Intel Mac (macOS 13 Ventura, x86_64)** 환경을 기준으로 구성되어 있습니다.
일부 ML 라이브러리 버전이 호환성 문제로 고정되어 있습니다.

| 패키지 | 고정 버전 | 사유 |
|--------|-----------|------|
| `torch` | `==2.2.2` | 2.3+ macOS 13 미지원 |
| `sentence-transformers` | `==2.2.2` | torch 2.2.2 의존 |
| `faiss-cpu` | `<1.8` | 1.8+ macOS 14+ 전용 |
| `onnxruntime` | `<1.17` | 1.17+ 메모리 이슈 |

자세한 내용은 [`docs/DEPENDENCIES.md`](docs/DEPENDENCIES.md)를 참조하세요.

---

## 참고 자료

- [LangChain Docs](https://python.langchain.com/)
- [OpenAI API Reference](https://platform.openai.com/docs/)
- [Gradio Documentation](https://www.gradio.app/docs/)
- [LangSmith](https://smith.langchain.com/)
