# 북싹 v0.15 — iPhone 홈 화면 앱 설치용 파일

이 폴더는 HTML 게임을 무료 정적 호스팅에 올려 iPhone 홈 화면에서 앱처럼 실행하도록 준비한 패키지입니다.

## 무료 공개 배포: GitHub Pages
1. GitHub에 로그인하고 새 **Public** 저장소(repository)를 만듭니다. 예: `booksprout-app`
2. 이 폴더 안의 파일과 `icons` 폴더를 압축 해제한 뒤 저장소 최상위(root)에 업로드합니다. ZIP 파일 자체가 아니라 ZIP을 푼 파일을 올립니다.
3. 저장소의 **Settings → Pages**로 이동합니다.
4. **Build and deployment → Source**에서 **Deploy from a branch**를 선택합니다.
5. Branch를 `main`, 폴더를 `/(root)`로 선택하고 **Save**를 누릅니다.
6. Pages가 배포하면 `https://<GitHub사용자명>.github.io/booksprout-app/` 주소가 표시됩니다. 배포에 몇 분 걸릴 수 있습니다.
7. iPhone에서 **Safari**로 그 주소를 엽니다. 공유 버튼 → **홈 화면에 추가(Add to Home Screen)** → **웹 앱으로 열기(Open as Web App)**를 켠 뒤 **추가**를 누릅니다.

주의: GitHub Free의 Pages는 공개 저장소를 사용하므로 이 게임 코드는 인터넷에 공개됩니다. 게임에 개인 정보나 비밀 정보를 입력하지 마세요.

## 구성
- `index.html`: 북싹 게임 전체 (배경·토끼 이미지를 HTML 안에 포함)
- `manifest.webmanifest`: 앱 이름, 아이콘 및 홈 화면 표시 설정
- `sw.js`: 앱 셸 캐시(지원되는 환경에서 재방문/오프라인 진입 보조)
- `icons/`: 홈 화면 앱 아이콘

게임 데이터는 브라우저의 localStorage에 저장됩니다. Safari의 웹사이트 데이터 삭제나 사이트 주소 변경 시 기록이 초기화될 수 있으므로, 해당 사이트 데이터를 삭제하지 마세요.
