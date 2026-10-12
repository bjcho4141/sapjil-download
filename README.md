# 벤자민의 삽질코딩 — 설치 파일 (테스트 버전)

AI 없이 **맨손으로** 개발을 배우는 퀘스트 게임 「벤자민의 삽질코딩 — 바이브코딩 시대에서 살아남기」의 설치 파일을 받는 곳이에요.
게임 개발은 비공개 레포에서 하고, 여기에는 [Releases](../../releases)에 설치 파일만 올려요.

## 윈도우 10 / 11

**① PowerShell**을 열고(시작 → `powershell`) 붙여 넣고 Enter — Node.js, Git(Git Bash 포함), VS Code를 설치해요.

```powershell
winget install -e --id OpenJS.NodeJS.LTS --accept-source-agreements --accept-package-agreements; winget install -e --id Git.Git --accept-source-agreements --accept-package-agreements; winget install -e --id Microsoft.VisualStudioCode --accept-source-agreements --accept-package-agreements
```

**② Git Bash**를 새로 열고(시작 → `git bash`) 붙여 넣고 Enter — 게임을 설치하고 바탕화면에 「삽질코딩」 아이콘을 만들어요.

```bash
npm install -g https://github.com/bjcho4141/sapjil-download/releases/latest/download/sapjil.tgz && node "$(npm root -g)/sapjil/dist/cli.js" init ~/sapjil-play
```

> Git Bash에서는 `Ctrl+V` 대신 **마우스 오른쪽 클릭 → Paste** 또는 `Shift+Insert`로 붙여 넣어요.

**③ 바탕화면 「삽질코딩」 아이콘을 더블클릭** — 게임 화면과 **VS Code**(내 작업 폴더 + 아래 작업 기록 터미널)가 같이 열려요. VS Code가 "신뢰하시나요?"라고 물으면 [예], 터미널이 안 보이면 ``Ctrl + ` ``. 끌 때는 게임 화면 오른쪽 위 **[⏻ 끄기]**.

## 맥

Node.js 22.12 이상(`brew install node` 또는 [nodejs.org](https://nodejs.org/ko/download))과 [VS Code](https://code.visualstudio.com)가 있어야 해요. 터미널에 붙여 넣고 Enter:

```bash
npm install -g https://github.com/bjcho4141/sapjil-download/releases/latest/download/sapjil.tgz && sapjil init ~/sapjil-play
```

Dock에 생긴 「삽질코딩」 아이콘을 누르면 게임 화면과 VS Code가 같이 열려요.

## 업데이트

`&&` 앞의 `npm install -g …` 부분만 다시 실행하면 최신 버전으로 바뀌어요. 게임 폴더(`~/sapjil-play`)와 진행 상황은 그대로예요.

## 막히면

화면을 캡처해서(윈도우 `Win+Shift+S`, 맥 `⌘+Shift+4`) 알려 주세요. 테스트 버전이라 그게 제일 큰 도움이에요.
