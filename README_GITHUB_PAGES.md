# BIFF 2026 시간표 — GitHub Pages / iPhone PWA

이 폴더의 파일을 **그대로 GitHub 저장소의 루트(root)** 에 업로드하면 됩니다.

## 포함 파일

- `index.html` — 메인 웹앱
- `404.html` — GitHub Pages fallback
- `manifest.webmanifest` — 홈 화면 / PWA 정보
- `service-worker.js` — 오프라인 캐시
- `.nojekyll` — GitHub Pages에서 Jekyll 처리 방지
- `icons/` — PWA 및 iPhone 홈 화면 아이콘

## 가장 쉬운 배포 방법 — GitHub 웹사이트에서 업로드

1. GitHub에 로그인합니다.
2. 우측 상단 `+` → **New repository**를 선택합니다.
3. 예: 저장소 이름을 `biff-2026-schedule`로 만듭니다.
4. GitHub Free를 사용한다면 Pages를 간단히 쓰기 위해 **Public** 저장소를 권장합니다.
5. 생성한 저장소에서 **Add file → Upload files**를 누릅니다.
6. 이 폴더 안의 파일/폴더를 모두 업로드합니다.
   - 중요한 점: `index.html`이 저장소 최상위에 있어야 합니다.
7. 아래 `Commit changes`를 눌러 업로드를 완료합니다.
8. 저장소 **Settings → Pages**로 이동합니다.
9. **Build and deployment → Source → Deploy from a branch**
10. Branch: `main`, Folder: `/(root)` 선택 후 **Save**
11. 잠시 기다린 뒤 같은 Pages 화면의 **Visit site**를 누릅니다.

주소는 보통 다음 형태입니다.

`https://<GitHub아이디>.github.io/biff-2026-schedule/`

## Git 명령어로 올리는 방법

Git이 설치된 PC에서 이 폴더를 연 뒤:

```bash
git init
git add .
git commit -m "BIFF 2026 schedule PWA"
git branch -M main
git remote add origin https://github.com/<GitHub아이디>/<저장소이름>.git
git push -u origin main
```

그 다음 GitHub 저장소의:

**Settings → Pages → Deploy from a branch → main / (root) → Save**

를 선택합니다.

이미 저장소가 있다면 이후 업데이트는:

```bash
git add .
git commit -m "Update BIFF schedule"
git push
```

만 하면 됩니다.

## iPhone에서 앱처럼 사용

1. GitHub Pages 주소를 **Safari**에서 엽니다.
2. Safari 하단/상단의 **공유 버튼**을 누릅니다.
3. **홈 화면에 추가**를 선택합니다.
4. 이름을 확인하고 **추가**를 누릅니다.
5. 홈 화면의 `BIFF 2026` 아이콘으로 실행합니다.

첫 접속은 인터넷이 필요합니다. 한 번 정상 접속하면 서비스 워커가 앱 파일을 캐시하므로 이후에는 오프라인에서도 기본 화면을 열 수 있습니다.

## 주의

- 카카오톡으로 `.html` 파일 자체를 보내서 미리보기로 여는 방식이 아니라, **GitHub Pages의 HTTPS 주소를 공유**하세요.
- Excel 내보내기와 일정 저장은 브라우저에서 동작합니다.
- GitHub Pages에 공개하면 사이트 내용은 인터넷에 공개됩니다.
