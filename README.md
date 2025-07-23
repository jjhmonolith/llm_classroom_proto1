# LLM Classroom

중학생을 위한 AI 교육 플랫폼 - 학생들이 LLM과 효과적으로 소통하는 방법을 배우는 온라인 에듀테크 도구

## 🎯 프로젝트 목적

LLM Classroom은 중학생들이 대화형 AI와 효과적으로 소통하는 방법을 배우고, 실시간 AI 튜터의 피드백을 통해 학습 효과를 극대화할 수 있는 교육용 플랫폼입니다.

## ✨ 주요 기능

### 🎓 학생 기능
- **주제별 LLM 대화**: 선택한 학습 주제에 맞는 AI와의 대화 환경
- **실시간 AI 튜터 피드백**: 학생의 질문 방식과 대화 패턴을 분석하여 개선점 제안
- **가이드형 시작 질문**: AI가 생성하는 개인화된 학습 가이드와 시작 질문 예시
- **마크다운 렌더링**: 풍부한 텍스트 표현으로 더 나은 학습 경험
- **클릭형 질문 전송**: 추천 질문을 클릭하여 즉시 대화 시작

### 🔧 AI 시스템
- **듀얼 AI 구조**: 채팅 AI와 튜터 AI의 분리된 역할
- **주제 관리**: 학습 주제에서 벗어나는 대화를 감지하고 리다이렉션
- **동적 프롬프트**: 각 주제별 맞춤형 AI 프롬프트 생성
- **GPT-4o-mini 모델**: 모든 AI 상호작용에 최신 모델 사용

## 🛠 기술 스택

- **Backend**: FastAPI
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **AI Integration**: OpenAI GPT-4o-mini API
- **Deployment**: Docker, AWS EC2, Nginx
- **Version Control**: Git, GitHub

## 🚀 설치 및 실행

### 로컬 환경
```bash
# 프로젝트 클론
git clone https://github.com/jjhmonolith/llm_classroom_proto1.git
cd llm_classroom_proto1

# 가상환경 생성 및 활성화
python -m venv venv
source venv/bin/activate  # macOS/Linux

# 의존성 설치
pip install -r requirements.txt

# 환경변수 설정
cp .env.example .env
# .env 파일에서 OPENAI_API_KEY 설정

# 서버 실행
python main.py
```

### Docker 실행
```bash
# Docker 이미지 빌드
docker build -t llm-classroom .

# 컨테이너 실행
docker run -p 8000:8000 --env-file .env llm-classroom
```

### AWS 배포
상세한 AWS 배포 가이드는 [AWS_DEPLOYMENT_GUIDE.md](AWS_DEPLOYMENT_GUIDE.md)를 참고하세요.

## 📁 프로젝트 구조

```
llm_classroom_proto1/
├── app/
│   ├── api/                 # API 라우터
│   │   ├── chat.py         # 채팅 API
│   │   └── initial.py      # 초기 설정 API
│   ├── services/           # 비즈니스 로직
│   │   ├── openai_service.py    # OpenAI API 통합
│   │   ├── topic_service.py     # 주제 관리 서비스
│   │   └── tutor_service.py     # AI 튜터 서비스
│   ├── models/             # 데이터 모델
│   └── utils/              # 유틸리티 함수
├── frontend/               # 프론트엔드 파일
│   ├── index.html         # 메인 채팅 페이지
│   └── topic-selection.html # 주제 선택 페이지
├── requirements.txt        # Python 의존성
├── main.py                # 애플리케이션 진입점
├── Dockerfile             # Docker 설정
├── deploy.sh              # 배포 스크립트
├── .env.example           # 환경변수 템플릿
├── AWS_DEPLOYMENT_GUIDE.md # AWS 배포 가이드
└── TECHNICAL_DOCUMENTATION.md # 기술 문서
```

## 📖 문서

- **[기술 문서](TECHNICAL_DOCUMENTATION.md)**: 시스템 아키텍처, AI 프롬프트, API 명세
- **[AWS 배포 가이드](AWS_DEPLOYMENT_GUIDE.md)**: 단계별 AWS 배포 방법
- **[환경 설정](.env.example)**: 환경변수 설정 가이드

## 🎮 사용 방법

1. **주제 선택**: 학습하고 싶은 주제를 선택합니다
2. **AI 가이드 확인**: 우측 튜터 피드백 영역에서 학습 가이드를 확인합니다
3. **질문 시작**: 추천 질문을 클릭하거나 직접 질문을 입력합니다
4. **피드백 활용**: AI 튜터의 실시간 피드백을 통해 질문 방식을 개선합니다

## 🔒 보안 및 프라이버시

- OpenAI API 키는 환경변수로 안전하게 관리
- 학생 대화 내용은 세션 기반으로만 저장
- HTTPS 지원 (Let's Encrypt SSL 인증서)

## 📊 성능 특징

- **응답 속도**: GPT-4o-mini의 빠른 응답 시간
- **확장성**: Docker 컨테이너 기반 배포로 쉬운 확장
- **안정성**: Nginx 리버스 프록시와 systemd 서비스 관리

## 🤝 기여 방법

1. Fork 이 리포지토리
2. Feature 브랜치 생성 (`git checkout -b feature/amazing-feature`)
3. 변경사항 커밋 (`git commit -m 'Add amazing feature'`)
4. 브랜치에 Push (`git push origin feature/amazing-feature`)
5. Pull Request 생성

## 📄 라이센스

이 프로젝트는 MIT 라이센스 하에 배포됩니다.

## 🆔 버전

**v1.0** - 2024년 초기 릴리즈
- 듀얼 AI 시스템 구현
- 실시간 튜터 피드백
- AWS 배포 지원
- 마크다운 렌더링
