# 주민 X 창업자 코크리에이션 크라우드 펀딩 플랫폼

<img src="https://github.com/user-attachments/assets/2adf8823-df2c-4d73-ab0c-c8a8c88c6e22" />

# Tech Stack

<table>
  <thead>
    <tr>
      <th>Frontend</th>
      <th>Backend</th>
      <th>Design</th>
      <th>Collaboration</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="top">
        <ul>
          <li>Application Type: Web, PWA</li>
          <li>Language: JavaScript</li>
          <li>Framework: React, CRA</li>
          <li>Style: styled-components, Chakra UI</li>
          <li>State Management: Zustand</li>
          <li>Data Fetch: Axios</li>
          <li>Data Cache: TanStack Query</li>
          <li>Cloud Infrastructure: Netlify</li>
        </ul>
      </td>
      <td valign="top">
        <ul>
          <li>Language: <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white" /></li>
          <li>Framework: <img src="https://img.shields.io/badge/django-092E20?style=for-the-badge&logo=django&logoColor=white" />, <img src="https://img.shields.io/badge/Django REST Framework-red?style=for-the-badge&logo=djangoRESTFramework&logoColor=white" /></li>
          <li>Database: <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" /></li>
          <li>Cache: <img src="https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white" /></li>
          <li>Authentication: <img src="https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=jwt&logoColor=white" /></li>
          <li>Cloud Infrastructure: <img src="https://img.shields.io/badge/AWS-orange?style=for-the-badge&logo=aws&logoColor=white" /></li>
          <li>CI/CD: <img src="https://img.shields.io/badge/Github Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" /></li>
        </ul>
      </td>
      <td valign="top">
        <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white" /><br />
      </td>
      <td valign="top">
        <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white" /><br />
        <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white" /><br />
        <img src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" /><br />
      </td>
    </tr>
  </tbody>
</table>

# Architecture Diagram
<img width="2284" height="1366" alt="아키텍처 다이어그램" src="https://github.com/user-attachments/assets/7471d28b-0169-4e23-8328-f78fa6c95861" />

# Directory Structure

<table>
  <thead>
    <tr>
      <th>Frontend Repository</th>
      <th>Backend Repository</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="top">
<pre><code>frontend/
│
├── .github/                           # GitHub 파일
│   ├── ISSUE_TEMPLATE/                # 이슈 템플릿
│   └── PULL_REQUEST_TEMPLATE.md       # PR 템플릿
│
├── public/                            # 정적 파일
│   ├── favicon.ico                    # 파비콘
│   ├── index.html                     # 진입점
│   ├── menifest.json                  # PWA 메타데이터
│   ├── robots.txt                     # 봇 접근제어
│   └── service-worker.js              # 서비스워커
│
├── src/                               # 소스 코드
│   ├── apis/                          # API 호출 관련 코드
│   │   ├── instance.js                # axios 인스턴스
│   │   ├── interceptor.js             # axios 인터셉터
│   │   └── ...                        # TanStack Query Hook (도메인별 파일 분리)
│   │
│   ├── assets/                        # 이미지 및 기타 리소스
│   │   ├── icons/                     # 아이콘 이미지
│   │   └── ...                        # 그외
│   │
│   ├── components/                    # UI 컴포넌트
│   │   ├── common/                    # 공통 컴포넌트
│   │   └── 도메인명/                   # 도메인별 컴포넌트
│   │
│   ├── constants/                     # 상수
│   │   ├── enum.js                    # ENUM
│   │   ├── env.js                     # 환경변수 import
│   │   └── route.js                   # 라우트 경로
│   │
│   ├── pages/                         # 페이지 컴포넌트
│   │   └── .../                       # 라우트 경로에 따른 폴더 분리
│   │
│   ├── service-workers/                       # 서비스 워커
│   │   ├── registerServiceWorker.js           # 서비스 워커 등록
│   │   ├── requestNotificationPermission.js   # 알림 권한 요청
│   │   └── subscribePush.js                   # 푸시 알림 구독
│   │
│   ├── stores/                        # 전역 상태
│   │   ├── example.js                 # 전역 상태 Hook 예시
│   │   └── ...                        # 전역 상태 Hook
│   │
│   ├── styles/                        # 스타일
│   │   ├── provider.js                # Chakra UI Provider
│   │   └── theme.js                   # 디자인 토큰 정의
│   │
│   ├── Router.jsx                     # 라우팅
│   └── index.jsx                      # 전역 설정
│
├── .env.example                       # 환경변수 목록
├── .gitignore                         # Git 제외 설정
├── .prettierrc.json                   # Prettier 설정
├── README.md                          # 레포지토리 리드미
├── netlify.toml                       # Netlify 설정
├── package-lock.json                  # 상세한 의존성 정보
└── package.json                       # 프로젝트 기본 정보 및 간략한 의존성 정보</code></pre>
      </td>
      <td valign="top">
<pre><code>backend/
│
├── .github/                       # GitHub 관리
│   ├── ISSUE_TEMPLATE/            # 이슈 템플릿
│   └── PULL_REQUEST_TEMPLATE.md   # PR 템플릿
│
├── configs/                       # config 관리
│   ├── settings/                  # Django 설정 관리
│   │   ├── __init__.py            # 어떤 환경인지 파악하고 어떤 설정을 적용할지 결정
│   │   ├── base.py                # 공통 Django 설정
│   │   ├── development.py         # 개발환경 Django 설정
│   │   └── production.py          # 배포환경 Django 설정
│   ├── __init__.py                # 이 폴더가 패키지임을 표시
│   ├── asgi.py                    # ASGI 설정
│   ├── urls.py                    # URL 설정
│   └── wsgi.py                    # WSGI 설정
│
├── <앱>/                          # Django App
│   ├── migrations/                # 데이터베이스 마이그레이션
│   ├── __init__.py                # 이 폴더가 패키지임을 표시
│   ├── admin.py                   # Admin 사이트 설정
│   ├── apps.py                    # App 설정
│   ├── models.py                  # Model 정의
│   ├── serializers.py             # Serializer 정의
│   ├── services.py                # 비즈니스 로직
│   ├── tests.py                   # 테스트 코드
│   ├── types.py                   # 커스텀 타입
│   ├── urls.py                    # App URL 설정
│   └── views.py                   # View 정의
│
├── utils/                         # 공통 유틸리티
│   ├── decorators/                # 커스텀 데코레이터
│   │   ├── service.py             # 서비스 전용 데코레이터
│   │   └── view.py                # 뷰 전용 데코레이터
│   ├── __init__.py                # 이 폴더가 패키지임을 표시
│   ├── choices.py                 # 커스텀 Choices
│   ├── constants.py               # 상수
│   ├── helpers.py                 # 공통 헬퍼 함수
│   └── serializer_fields.py       # 커스텀 시리얼라이저 필드
│
├── env_example/                   # 환경변수 목록
│   ├── .env.base                  # 공통 환경변수
│   ├── .env.development           # 개발환경 환경변수
│   └── .env.production            # 배포환경 환경변수
│
├── .gitignore                     # Git 제외 설정
├── manage.py                      # 명령어 실행 도구
├── README.md                      # 레포지토리 리드미
└── requirements.txt               # 의존성 목록</code></pre>
      </td>
    </tr>
  </tbody>
</table>

# Entity Relationship Diagram

<img src="https://github.com/user-attachments/assets/57283b1b-374e-4493-a3da-65b0354ef126" />

