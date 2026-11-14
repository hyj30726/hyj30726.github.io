# 황유주 소개 페이지와 마음의 작은 섬

국민대학교 경영정보학부 26학번 황유주(Hwang Yuju)의 개인 소개 페이지입니다.
GitHub Pages 주소: <https://hyj30726.github.io/>

## 파일

- `index.html` — 소개, 학업·역량, 프로젝트 링크, 주간 루틴, 목표, FAQ 공개 질문, Firestore 방명록·공감, 실시간 짝맞추기 TOP 3, 연락처
- `island.html` — 직접 입력을 포함한 마음 체크와 브라우저 기록, 안심 목록, 읽기 쉬운 TXT 백업, Firebase 로그인·익명 게시판·비공개 일기, 쉬어가기 도구와 도움 연락처
- `island-logo.svg` — 마음의 작은 섬 페이지 로고
- `og-image.svg` — 공유 이미지의 편집 가능한 원본
- `og-image.png` — Open Graph와 X 카드에서 사용하는 1200×630 미리보기 이미지
- `robots.txt`, `sitemap.xml` — 크롤러 안내와 공개 URL 목록

## Firebase 공유 기능

섬 페이지의 공개 게시판과 비공개 일기, 소개 페이지의 공개 질문은 Firebase를 사용합니다. 소개 페이지의 질문은 `profileQuestions` 경로에 저장되며, 방명록·공감·게임 순위는 해당 기능의 Firestore 규칙이 별도로 허용되어야 합니다. 방명록과 질문, 닉네임은 공개됩니다. 질문은 이메일을 받지 않습니다.

Firebase Authentication에서 이메일/비밀번호와 익명 로그인을 사용 설정하고, 승인된 도메인에 `hyj30726.github.io`를 추가하세요. Firestore 규칙 원본은 `firestore.rules`이며, Firebase Console의 Firestore Database → Rules에서 게시하거나 Firebase CLI로 배포할 수 있습니다.

```sh
firebase deploy --only firestore:rules --project ureka-28d23
```

Rules 변경은 GitHub Pages 배포와 별개로 Firebase에 게시해야 합니다.

## 검색 접근성

- 페이지 제목, 설명, canonical URL, Open Graph, X 카드 메타데이터를 제공합니다.
- JSON-LD의 `Person`, `WebSite`, `ProfilePage` 정보는 화면에 보이는 자기소개와 맞춥니다.
- FAQ는 방문자가 읽을 수 있는 HTML로도 표시합니다. 구조화 데이터가 검색 결과의 특별한 표시를 보장하지는 않습니다.
- 생성형 검색을 위한 별도 마크업이나 반복 키워드는 추가하지 않습니다. 정확하고 구체적인 자기소개와 크롤러가 읽을 수 있는 기본 구조를 우선합니다.

## 게시 후 설정

사이트 소유자 계정으로 Google Search Console과 Bing Webmaster Tools에 사이트를 등록하고, `https://hyj30726.github.io/sitemap.xml`을 제출할 수 있습니다. 제출은 검색 노출이나 즉시 색인을 보장하지 않습니다.