# Speak-Up Cards

English/Korean flashcards and a practice checklist that help kids find the right words in class, games, and tricky moments with other kids (72 phrases in 5 tabs, plus a step-by-step Freeze Tag explainer).

아이가 수업, 게임, 친구 관계에서 바로 꺼내 쓸 수 있는 짧은 영어 표현과 한국어 뜻을 연습하는 플래시카드 + 체크리스트 앱입니다.

- 서버, API, 빌드 과정이 없습니다. `index.html`이 앱 본체이고, `icons/`와 `manifest.webmanifest`는 홈 화면 아이콘과 실행 화면(스플래시)용 파일입니다.
- 체크한 진행 상황은 각 기기의 브라우저(localStorage)에만 저장됩니다.
- 스피커 버튼은 브라우저의 음성 읽기(Web Speech API)를 사용합니다. 기기에 따라 목소리가 다릅니다.

## GitHub Pages로 열기

1. 이 저장소를 GitHub에 올립니다.
2. **Settings → Pages → Build and deployment**에서 Source를 `Deploy from a branch`, Branch를 `main` / `/ (root)`로 선택합니다.
3. 잠시 후 `https://<계정>.github.io/<저장소 이름>/` 주소로 열립니다.

## 표현 수정하기

`index.html` 안의 `const TABS = [...]` 목록에 카드 데이터가 있습니다. 카드 하나는 다음 형태입니다.

```js
{sit:"상황 (English)", sitKo:"상황 (한국어)", say:"English phrase", ko:"한국어 뜻", alt:"Other way", altKo:"다른 표현 한국어"}
```

새 카드는 각 탭 목록의 **맨 뒤**에 추가해야 이전에 체크한 진행 상황이 유지됩니다.

## 홈 화면에 추가하기

- **아이폰/아이패드:** Safari에서 열고 공유 버튼 → **홈 화면에 추가**.
- **안드로이드:** Chrome에서 열고 메뉴 → **홈 화면에 추가** (또는 앱 설치).

아이콘을 바꾸고 싶으면 `icons/` 안의 PNG 파일을 같은 이름으로 교체하세요.
