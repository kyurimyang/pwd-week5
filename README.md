# Ajou Campus Foodmap

아주대학교 주변 맛집을 소개하고 제보받는 커뮤니티 서비스입니다. (PWD 2026 2학기 5주차 실습)

- GitHub: https://github.com/kyurimyang/pwd-week5
- Vercel: (배포 후 URL 추가)

## 주요 기능

- 맛집 목록 보기와 카테고리별 필터링
- 맛집 상세 페이지
- 좋아요 (LocalStorage에 저장)
- 인기 맛집 TOP 5 (평점순)
- 맛집 제보 (LocalStorage에 저장, 이 브라우저에만 보관)
- 반응형 디자인

## 기술 스택

React 19, TypeScript(strict), Vite, React Router, Emotion, React Hook Form, React Query, Vercel

## 실행 방법

Node.js 24.x가 필요합니다.

```bash
npm ci
npm run dev        # 개발 서버 (http://localhost:5173)
npm run typecheck  # 타입 검사
npm run lint       # 린트
npm run build      # 타입 검사 후 dist 빌드
```

## 폴더 구조

```
src/
├── components/  # 재사용 컴포넌트
├── pages/       # 페이지 컴포넌트
├── services/    # 데이터 접근(api.ts), LocalStorage 읽기(storage.ts), 검증(validation.ts)
├── styles/      # 전역 스타일
└── types/       # 공통 타입
```

## 참고

- 백엔드 없이 동작합니다. 맛집은 코드에 포함된 가상 데이터이고, 좋아요와 제보는 브라우저 LocalStorage에 저장됩니다.
- 저장된 데이터는 같은 브라우저, 같은 주소에서만 유지되며 다른 사용자와 공유되지 않습니다.
- `vercel.json`은 상세 페이지 등에서 새로고침해도 404가 나지 않도록 모든 주소를 `index.html`로 보냅니다.
