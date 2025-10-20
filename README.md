# Tommo 🐻

> 함께하는 가계부 관리 서비스

Tommo는 가족이나 친구들과 함께 가계부를 관리할 수 있는 웹 애플리케이션입니다. 투표 기능을 통해 소비 결정을 민주적으로 내리고, 실시간으로 가계부를 공유할 수 있습니다.

## 🧩 문제 정의

- 부부 또는 가족이 각자 지출을 관리할 경우 **전체 재정 상황을 명확히 알기 어려움**
- 단순 메신저나 구두 합의에 의존 시 **분쟁 가능성** 증가
- 카드/계좌이체 사용 시 현금과 달리 지출 체감이 약해, 본인조차 **정확한 소비 내역을 파악하기 어려움**
- 실제 조사 결과, 20·30세대의 63%가 "한 달 지출 내역을 정확히 모른다"고 응답

## ✨ 주요 기능

### 🏠 가계부 관리
- **그룹 가계부**: 여러 명이 함께 가계부를 관리
- **수입/지출 기록**: 카테고리별 수입과 지출 내역 기록
- **캘린더 뷰**: 월별 가계부 현황을 캘린더로 확인
- **통계 분석**: 지출 패턴과 카테고리별 분석
- **고급 기능**: 정기 결제, 할부 결제 지원

### 🗳️ 투표 시스템
- **소비 투표**: 큰 금액의 소비에 대해 그룹원들과 투표
- **실시간 결과**: 투표 진행 상황과 결과를 실시간으로 확인
- **투표 관리**: 투표 생성, 수정, 삭제 기능

### 📊 통계 및 분석
- **차트 시각화**: 지출 패턴을 다양한 차트로 분석
- **카테고리별 분석**: 수입/지출 카테고리별 상세 통계
- **월별 리포트**: 월별 가계부 현황 리포트
- **엑셀 내보내기**: 데이터를 엑셀 파일로 다운로드

### 👥 그룹 관리
- **그룹 생성**: 새로운 가계부 그룹 생성
- **멤버 초대**: 이메일을 통한 그룹 멤버 초대
- **권한 관리**: 그룹 관리자 권한 설정

### 💬 소셜 기능
- **댓글 시스템**: 지출 내역에 댓글 작성 및 소통
- **반응 기능**: 이모지로 지출 내역에 반응
- **알림 시스템**: 새로운 지출, 댓글, 투표 결과 알림

## 🛠️ 기술 스택

### ⚙️ 빌드/번들링
- **Vite** - React + TypeScript 개발 환경 빠르게 구축

### 📦 데이터 관리
- **Supabase** - 오픈소스 Firebase 대체제
- **PostgreSQL** 기반 (DB + 인증 + 스토리지 제공)
- **Auth(로그인/회원가입), Realtime(실시간), Storage(파일 업로드)** 지원

### 🖥️ 라우팅
- **React Router (v7)** - 페이지 라우팅 관리

### 🎨 UI & 스타일
- **Tailwind CSS** - Utility-first CSS 프레임워크
- **clsx** - 조건부 className 처리 도우미
- **tailwind-merge** - Tailwind className 충돌 시 자동 정리
- **Framer Motion** - 애니메이션/전환 효과 라이브러리

### 📝 상태 관리
- **Zustand** - 가벼운 상태 관리 라이브러리
- **전역 상태 관리용** (사용자 정보, 토큰, UI 상태 등)

### 🖥️ 폼 & 데이터 처리
- **xlsx (SheetJS)** - 엑셀 파일 읽기/내보내기 라이브러리

### 📊 시각화
- **Recharts** - 차트/그래프 라이브러리
- **원형 그래프, 막대 그래프, 라인 차트** 등 지원

### 🔧 개발 편의 도구
- **ESLint** - 코드 품질 검사
- **Prettier** - 코드 포매터
- **TypeScript** - 정적 타입 시스템

## 🚀 시작하기

### 필수 요구사항
- Node.js 18+ 
- npm 또는 yarn

### 설치 및 실행

1. **저장소 클론**
   ```bash
   git clone https://github.com/your-username/towmoo.git
   cd towmoo
   ```

2. **의존성 설치**
   ```bash
   npm install
   ```

3. **환경 변수 설정**
   ```bash
   # .env.local 파일 생성
   VITE_SUPABASE_URL=your_supabase_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. **개발 서버 실행**
   ```bash
   npm run dev
   ```

5. **브라우저에서 확인**
   ```
   http://localhost:5173
   ```

### 빌드 및 배포

```bash
# 프로덕션 빌드
npm run build

# 빌드 미리보기
npm run preview

# 린트 검사
npm run lint
```

## 📁 프로젝트 구조

```
src/
├── app/                    # 앱 진입점 (App.tsx, Router.tsx)
├── features/              # 기능별 모듈 (데이터 관련)
│   ├── accountbook/       # 가계부 기능
│   ├── calendar/          # 캘린더 기능
│   ├── group/             # 그룹 관리
│   ├── vote/              # 투표 기능
│   ├── statistics/        # 통계 기능
│   ├── detail/            # 상세 조회 기능
│   └── accountItem/       # 가계부 아이템 기능
├── pages/                 # 페이지 컴포넌트 (UI만)
│   ├── accountbook/       # 가계부 페이지
│   ├── calendar/          # 캘린더 페이지
│   ├── group/             # 그룹 관리 페이지
│   ├── vote/              # 투표 페이지
│   ├── statistics/        # 통계 페이지
│   ├── item/              # 아이템 관리 페이지
│   └── more/              # 더보기 페이지
├── shared/                # 공통 컴포넌트 및 유틸
│   ├── components/        # 재사용 컴포넌트
│   ├── hooks/             # 커스텀 훅
│   ├── stores/            # 상태 관리 (Zustand)
│   ├── services/          # API 서비스
│   └── utils/             # 유틸리티 함수
└── supabase/              # Supabase 설정
```

## 🎯 주요 페이지

- **홈**: 그룹 목록 및 가계부 현황
- **캘린더**: 월별 가계부 캘린더 뷰
- **통계**: 지출 분석 및 차트
- **투표**: 그룹 투표 관리
- **설정**: 그룹 및 계정 설정

## 🚀 개발 로드맵

### 1차 스프린트: 로그인 + 기본 기록
- [x] 소셜 로그인 (구글, 카카오)
- [x] 기본 가계부 아이템 CRUD
- [x] 카테고리별 분류

### 2차 스프린트: 그룹 공유 + 달력 뷰
- [x] 그룹 생성 및 관리
- [x] 멤버 초대 시스템
- [x] 달력 뷰 구현

### 3차 스프린트: 통계 + 투표
- [x] 통계 차트 구현
- [x] 투표 시스템
- [x] 소셜 기능 (댓글, 반응)

### 4차 스프린트: 리포트/엑셀 다운로드
- [ ] 월별 리포트 생성
- [ ] 엑셀 내보내기 기능
- [ ] 알림 시스템

## 🔤 코딩 컨벤션

### 네이밍 규칙
| 대상 | 컨벤션 | 예시 |
| --- | --- | --- |
| 변수, 함수 | `camelCase` | `userName`, `handleClick` |
| 컴포넌트, 클래스 | `PascalCase` | `UserProfile`, `LoginForm` |
| 타입, 인터페이스 | `PascalCase` | `UserInfo`, `ApiResponse` |
| 상수 | `UPPER_SNAKE_CASE` | `API_URL`, `MAX_RETRY_COUNT` |

### Git 컨벤션
| 태그 | 설명 | 예시 |
| --- | --- | --- |
| `feat` | 새로운 기능 추가 | `feat: 로그인 기능 구현` |
| `fix` | 버그 수정 | `fix: 로그인 에러 처리 추가` |
| `docs` | 문서 수정 | `docs: README 업데이트` |
| `style` | 코드 스타일 변경 | `style: Prettier 적용` |
| `refactor` | 코드 리팩토링 | `refactor: 컴포넌트 분리` |
| `test` | 테스트 코드 추가 | `test: 로그인 테스트 추가` |
| `chore` | 빌드 설정 변경 | `chore: 의존성 업데이트` |

### Prettier 설정
```json
{
  "semi": false,
  "singleQuote": true,
  "singleAttributePerLine": true,
  "bracketSameLine": true,
  "endOfLine": "lf",
  "trailingComma": "none",
  "arrowParens": "avoid"
}
```

### 브랜치 전략
- `main`: 직접 push 금지 → PR을 통해서만 반영
- `feature`: 각자 개발할 때 만드는 브랜치 (예: `feature/login`)

## 👥 팀원

- **박철현** - Frontend Developer
- **정은빈** - Frontend Developer  
- **김정주** - Frontend Developer
- **이성균** - Frontend Developer

**FES-5-Project3-TEAM-5-1**

---

<img width="2048" height="2048" alt="Towmoo Logo" src="https://github.com/user-attachments/assets/0c3ddbb4-c9e0-4bc0-a4ed-c6db4fa8086d" />

