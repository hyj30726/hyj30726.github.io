# 마음의 작은 섬

마음을 살펴보고 잠시 쉬어가는 웹페이지입니다.

메인 주소 <https://hyj30726.github.io/> 에서 섬, 쉼으로 이동합니다.

## 주요 기능

- 체크인 기록은 사용 중인 브라우저의 `localStorage`에만 저장됩니다.
- 이메일/비밀번호 계정으로 로그인하면 마음일기를 Firebase에 저장하고 다시 볼 수 있습니다. 일기는 작성자 계정만 읽고 삭제할 수 있습니다.
- 익명 게시글과 답글은 Firebase에 공개 저장됩니다. 게시글에 이모지로 공감할 수 있고, 게시판은 실시간으로 갱신됩니다.
- 로그인하지 않아도 공개 게시판을 둘러볼 수 있습니다.

## Firebase 설정

1. Firebase Authentication에서 **이메일/비밀번호**와 **익명** 로그인을 사용 설정합니다.
2. Authentication의 **승인된 도메인**에 `hyj30726.github.io`를 추가합니다. Codespaces 미리보기를 사용할 경우 해당 미리보기 호스트도 추가해야 합니다.
3. Firestore 데이터베이스를 만들고, 프로젝트 루트에서 보안 규칙을 배포합니다.

   ```sh
   firebase deploy --only firestore:rules --project ureka-28d23
   ```

4. `island.html`의 Firebase 웹 앱 설정이 Firebase 콘솔의 웹 앱과 일치하는지 확인합니다.

계정 생성이나 로그인이 안 되면 화면의 오류 안내를 확인하세요. `auth/operation-not-allowed`는 해당 로그인 방식이 꺼져 있다는 뜻이고, `auth/unauthorized-domain`은 현재 접속 주소를 승인된 도메인에 추가해야 한다는 뜻입니다.

게시글과 답글은 공개됩니다. Firestore 규칙은 데이터 접근을 제한하지만 게시물의 유해성 검토나 스팸 방지를 대신하지 않습니다. 체크인 기록은 브라우저에 남고, 마음일기만 Firebase 계정에 저장됩니다. 이 페이지는 전문 상담이나 치료를 대신하지 않습니다.
