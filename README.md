# 황유주 소개 페이지

국민대학교 경영정보학부 26학번 **황유주(Hwang Yuju)** 의 개인 소개 페이지입니다.
GitHub Pages로 배포됩니다: <https://hyj30726.github.io/>

## 구성

- `index.html` — 소개, 학업과 역량, 성향(ESFJ), 주간 루틴, 겨울방학 계획, 학년별 목표, 퀴즈, FAQ, 방명록, 연락처
- `og-image.svg` — 링크 공유 미리보기용 이미지(1200×630)
- `robots.txt`, `sitemap.xml` — 검색 엔진 크롤링 안내

## SEO / GEO

- `<head>`에 canonical, Open Graph, Twitter Card 메타 포함
- JSON-LD 구조화 데이터(`Person`, `WebSite`, `ProfilePage`, `FAQPage`)로 검색·생성형 AI 엔진이 엔티티로 인식
- 질문형 섹션 헤딩과 FAQ로 AI 답변에 인용되기 쉽게 구성

## 직접 해주면 좋은 후속 작업

1. Google Search Console / Bing 웹마스터에 `sitemap.xml` 제출
2. 공유 미리보기에 PNG가 꼭 필요하면 `og-image.svg`를 1200×630 PNG로 변환해 `og-image.png`로 올리고, `index.html`의 `og:image`/`twitter:image` 경로를 `.png`로 변경
3. 커스텀 도메인을 쓰면 `index.html`·`sitemap.xml`·`robots.txt`의 URL을 새 도메인으로 교체
