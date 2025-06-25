# 🎯 Vibe Coding W2-2: AI 에이전트 기반 채팅 시스템

> **Vibe Coding Week 2-2 프로젝트**: LangGraph를 활용한 AI 에이전트 기반 대화형 시스템

## 📋 프로젝트 개요

이 프로젝트는 **FastAPI**와 **Streamlit**을 기반으로 한 AI 에이전트 채팅 시스템입니다. **LangGraph**를 활용하여 메모리 기능을 포함한 대화형 AI를 구현하며, **TDD(Test-Driven Development)** 방법론을 적용하여 개발되었습니다.

## ✨ 주요 기능

- 🤖 **AI 에이전트 대화**: LangGraph 기반 AI 에이전트와의 자연스러운 대화
- 🧠 **메모리 기능**: 대화 컨텍스트를 기억하는 스마트 메모리 시스템  
- 🎨 **현대적 UI**: Streamlit 기반의 직관적이고 아름다운 사용자 인터페이스
- 🔄 **실시간 스트리밍**: 응답이 실시간으로 스트리밍되는 대화 경험
- 📊 **포괄적 테스트**: TDD 방식으로 구현된 완전한 테스트 커버리지

## 🏗️ 시스템 아키텍처

```
┌─────────────────┐    HTTP/WebSocket    ┌─────────────────┐
│   Frontend      │ ◄──────────────────► │   Backend       │
│   (Streamlit)   │                      │   (FastAPI)     │
└─────────────────┘                      └─────────────────┘
                                                   │
                                                   ▼
                                         ┌─────────────────┐
                                         │   AI Agent      │
                                         │   (LangGraph)   │
                                         └─────────────────┘
```

## 📁 프로젝트 구조

```
vibe_coding_w2-2/
├── 📁 backend/                 # FastAPI 백엔드
│   ├── 📁 app/
│   │   ├── 📁 models/         # 데이터 모델
│   │   ├── 📁 routers/        # API 라우터
│   │   ├── agent.py           # AI 에이전트 로직
│   │   ├── config.py          # 설정 관리
│   │   └── main.py            # FastAPI 애플리케이션
│   ├── 📁 tests/              # 백엔드 테스트
│   └── requirements.txt       # 백엔드 의존성
├── 📁 frontend/               # Streamlit 프론트엔드
│   ├── app.py                 # 메인 애플리케이션
│   └── requirements.txt       # 프론트엔드 의존성
├── 📁 .github/                # GitHub 자동화
│   ├── 📁 workflows/          # GitHub Actions
│   ├── 📁 ISSUE_TEMPLATE/     # 이슈 템플릿
│   └── 📁 PULL_REQUEST_TEMPLATE/ # PR 템플릿
├── 📁 docs/                   # 프로젝트 문서
└── 📁 .cursor/                # 개발 가이드라인
```

## 🚀 빠른 시작

### 📋 사전 요구사항

- Python 3.9+
- pip
- Git

### 🔧 설치 및 실행

1. **저장소 클론**
```bash
git clone https://github.com/wndudwns0028/vibe_coding_w2-2.git
cd vibe_coding_w2-2
```

2. **백엔드 설정 및 실행**
```bash
cd backend
pip install -r requirements.txt
python run.py
```

3. **프론트엔드 설정 및 실행** (새 터미널)
```bash
cd frontend
pip install -r requirements.txt
streamlit run app.py
```

4. **접속**
- 🎨 **프론트엔드**: http://localhost:8501
- 🔧 **백엔드 API**: http://localhost:8000
- 📚 **API 문서**: http://localhost:8000/docs

## 🧪 테스트 실행

### 백엔드 테스트
```bash
cd backend
python -m pytest tests/ -v
```

### 테스트 커버리지 확인
```bash
cd backend
python -m pytest tests/ --cov=app --cov-report=html
```

## 🔧 기술 스택

### 🖥️ Backend
- **FastAPI**: 현대적이고 빠른 웹 프레임워크
- **LangGraph**: AI 에이전트 구현
- **LangChain**: AI 모델 통합
- **Pydantic**: 데이터 검증 및 설정 관리
- **Pytest**: 테스트 프레임워크

### 🎨 Frontend  
- **Streamlit**: 빠른 웹 앱 개발
- **Requests**: HTTP 클라이언트

### 🔄 DevOps & Automation
- **GitHub Actions**: CI/CD 자동화
- **이슈/PR 템플릿**: 체계적인 프로젝트 관리
- **자동 라벨링**: 스마트한 이슈/PR 분류
- **코드 리뷰 자동화**: 품질 관리

## 🎯 주요 특징

### 🤖 AI 에이전트
- **LangGraph 활용**: 복잡한 대화 플로우 관리
- **메모리 시스템**: 대화 컨텍스트 유지
- **스트리밍 응답**: 실시간 대화 경험

### 🧪 테스트 주도 개발 (TDD)
- **포괄적 테스트**: 모든 핵심 기능에 대한 테스트
- **Mock 활용**: 외부 의존성 격리
- **지속적 통합**: 자동화된 테스트 실행

### 🔄 GitHub 자동화
- **자동 테스트**: Push/PR 시 자동 테스트 실행
- **스마트 라벨링**: 내용 기반 자동 라벨 할당
- **자동 리뷰**: 코드 품질 자동 검사
- **담당자 할당**: 이슈/PR 자동 할당

## 📖 API 문서

백엔드 서버 실행 후 다음 URL에서 자세한 API 문서를 확인할 수 있습니다:
- **Swagger UI**: http://localhost:8000/docs
- **ReDoc**: http://localhost:8000/redoc

## 🤝 기여하기

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 라이센스

이 프로젝트는 MIT 라이센스 하에 배포됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## 📞 문의

프로젝트에 대한 질문이나 제안사항이 있으시면 이슈를 생성해주세요!

---

⭐ **이 프로젝트가 도움이 되셨다면 별표를 눌러주세요!** ⭐ 