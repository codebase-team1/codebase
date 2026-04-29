# 코드베이스 (CODE:BASE) 공식 홈페이지

> 스마트팩토리 구축 & 플랫폼 개발 전문기업 — AI 머신비전 · 스마트HACCP · MES · 자동화 로봇을 단일 플랫폼으로

🌐 **사이트**: https://www.code-base.co.kr
📩 **문의**: codebase_team@code-base.co.kr
📞 **전화**: 010-9741-5525
📍 **주소**: 대구광역시 수성구 알파시티1로42길 11, 태왕알파시티수성 913호

---

## 📂 파일 구조

```
.
├── index.html                       # 메인 페이지 (Hero · 솔루션 · 산업 · 플랫폼 · 기술 · CTA)
├── contact.html                     # 문의 양식 페이지 (EmailJS 자동 발송)
├── privacy.html                     # 개인정보처리방침
├── terms.html                       # 이용약관
├── logo.png                         # 통합 로고 (모든 페이지 공유)
├── favicon.svg                      # 벡터 favicon (현대 브라우저 우선)
├── favicon-96x96.png                # 브라우저 탭 아이콘 (PNG)
├── favicon.ico                      # 구형 브라우저 호환
├── apple-touch-icon.png             # iOS 홈 화면 아이콘 (180x180)
├── web-app-manifest-192x192.png     # PWA 아이콘
├── web-app-manifest-512x512.png     # PWA 아이콘 (대형)
├── site.webmanifest                 # PWA 매니페스트
├── og-image.png                     # SNS 공유 미리보기 (1200x630) ※ 별도 생성 필요
├── README.md                        # 이 문서
└── .gitignore                       # Git 무시 파일 목록
```

---

## ✨ 주요 기능

- **단일 페이지 스크롤형 메인**: Hero → 솔루션 4종 → 산업군 → 차별점 비교 → 플랫폼 → 요금제 → 기술 → CTA → 푸터
- **반응형 디자인**: 데스크톱(1024px+) · 태블릿(768px) · 모바일(480px) 분기 처리
- **모바일 햄버거 메뉴**: 드로어 형태로 펼침/닫힘
- **부드러운 앵커 스크롤 + Scrollspy**: 현재 위치 자동 강조
- **문의 폼 자동 메일 발송**: EmailJS 연동, 24시간 이내 회신
- **URL 파라미터 매핑**: `?type=demo` 등으로 문의 유형 자동 선택

---

## 🛠 사용 기술

순수 정적 사이트 — 빌드 도구·프레임워크 없음. 브라우저에서 바로 동작합니다.

| 영역 | 기술 |
|---|---|
| 마크업 | HTML5 (시멘틱) |
| 스타일 | CSS3 (CSS Variables, Grid, Flexbox) |
| 스크립트 | Vanilla JavaScript (ES6+) |
| 폰트 | Google Fonts: Barlow Condensed · Noto Sans KR · JetBrains Mono |
| 메일 발송 | [EmailJS v4](https://www.emailjs.com/) (브라우저 직접 호출) |
| 호스팅 | GitHub Pages |

---

## 🚀 로컬 실행

별도 빌드 없이 브라우저로 바로 열면 됩니다:

```bash
# Windows
start index.html

# Mac
open index.html

# Linux
xdg-open index.html
```

또는 VS Code의 **Live Server** 확장을 사용하시면 파일 변경 시 자동 새로고침됩니다.

---

## 🌐 배포 (GitHub Pages)

1. 이 저장소를 GitHub에 Push
2. **Settings → Pages** 메뉴
3. Source: `Deploy from a branch` → Branch: `main` / `(root)`
4. Custom domain: `www.code-base.co.kr` 입력 → **Enforce HTTPS** 체크
5. 가비아 DNS 설정에 CNAME / A 레코드 추가
6. `index.html`이 자동으로 진입점으로 인식됩니다 — 별도 설정 불필요

---

## 📧 문의 폼 EmailJS 설정

`contact.html` 의 다음 상수를 발급받은 키로 교체:

```js
const EMAILJS_PUBLIC_KEY  = '...';
const EMAILJS_SERVICE_ID  = '...';
const EMAILJS_TEMPLATE_ID = '...';
const SHEETS_URL          = 'YOUR_APPS_SCRIPT_URL'; // 선택사항: Google Sheets 자동 저장
```

EmailJS 대시보드 → **Account** → **Allowed Origins** 에 다음 도메인 추가 필수:
- `https://www.code-base.co.kr`
- 로컬 테스트 시: `http://localhost`, `null`

---

## 🔐 보안 노트

- **Public Key는 노출되어도 안전** — Allowed Origins로 도메인 제한
- **Private Key는 절대 코드/저장소에 포함하지 말 것**
- 민감 정보(Service Account Key 등)는 [.gitignore](./.gitignore)로 차단

---

## 📜 약관·정책

- [개인정보처리방침](./privacy.html)
- [이용약관](./terms.html)

> 두 문서는 표준 양식 기반 초안입니다. 실제 시행 전 법무 검토 권장.

---

## © 라이선스

© 2026 코드베이스(CodeBase) All rights reserved.
