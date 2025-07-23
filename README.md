# LLM Classroom

학생들이 LLM 사용법과 활용을 배울 수 있는 온라인 에듀테크 도구

## 프로젝트 목적

LLM Classroom은 학생들이 대화형 AI와 효과적으로 소통하는 방법을 배우고, 교사가 학습 과정을 체계적으로 관리할 수 있는 교육용 플랫폼입니다.

## 주요 기능

### 학생 기능
- **개별 LLM 환경 제공**: 각 학생별로 독립적인 LLM 대화 환경 제공
- **AI 피드백 시스템**: 학생의 LLM 대화 방식을 분석하여 개선점 제안
- **커리큘럼 기반 문제 해결**: 지정된 커리큘럼에 따라 LLM과 함께 문제 해결
- **가이드형 학습**: LLM이 학생을 커리큘럼에 따라 체계적으로 안내

### 교사 기능
- **학생 대화 모니터링**: 실시간 학생-LLM 대화 내용 확인
- **대시보드**: 학생별 학습 현황 및 진도 요약 확인
- **커리큘럼 관리**: 학습 과정 설계 및 조정
- **학습 분석**: 학생별 LLM 활용 패턴 및 성과 분석

## 기술 스택

- **Backend**: FastAPI
- **Frontend**: React/Vue.js
- **Database**: PostgreSQL
- **LLM Integration**: OpenAI API, Anthropic Claude API
- **Authentication**: JWT
- **Deployment**: Docker

## 설치 및 실행

```bash
# 프로젝트 클론
git clone <repository-url>
cd LLM-Classroom

# 가상환경 생성 및 활성화
python -m venv venv
source venv/bin/activate  # macOS/Linux
# venv\Scripts\activate  # Windows

# 의존성 설치
pip install -r requirements.txt

# 환경변수 설정
cp .env.example .env
# .env 파일에서 API 키 및 데이터베이스 설정

# 데이터베이스 초기화
python init_db.py

# 서버 실행
python main.py
```

## 프로젝트 구조

```
LLM-Classroom/
├── app/
│   ├── models/          # 데이터베이스 모델
│   ├── api/             # API 라우터
│   ├── services/        # 비즈니스 로직
│   └── utils/           # 유틸리티 함수
├── frontend/            # 프론트엔드 코드
├── tests/               # 테스트 코드
├── requirements.txt     # Python 의존성
└── main.py             # 애플리케이션 진입점
```

## 기여

이 프로젝트에 기여하고 싶으시다면 Pull Request를 보내주세요.

## 라이센스

이 프로젝트는 MIT 라이센스 하에 배포됩니다.