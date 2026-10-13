# 벤자민의 삽질코딩 — 설치 파일 (테스트 버전)

AI 없이 **맨손으로** 개발을 배우는 퀘스트 게임 「벤자민의 삽질코딩 — 바이브코딩 시대에서 살아남기」의 설치 파일을 받는 곳이에요.
게임 개발은 비공개 레포에서 하고, 여기에는 [Releases](../../releases)에 설치 파일만 올려요.

**내 컴퓨터에 맞는 칸만 보면 돼요** → [🪟 윈도우 10 / 11](#-윈도우-10--11) · [🍎 맥](#-맥) · [🔄 업데이트](#-업데이트-새-버전이-나왔을-때) · [🆘 막히면](#-막히면)

---

## 🪟 윈도우 10 / 11

> 시간 약 10분. 명령어 **두 줄**이면 끝나요.

### 1단계 — PowerShell: 필요한 프로그램 3개 설치

시작 메뉴에서 `powershell` 검색 → 열기 → 아래 줄을 붙여 넣고 Enter. **Node.js · Git(Git Bash 포함) · VS Code**를 차례대로 설치해요.

```powershell
winget install -e --id OpenJS.NodeJS.LTS --accept-source-agreements --accept-package-agreements; winget install -e --id Git.Git --accept-source-agreements --accept-package-agreements; winget install -e --id Microsoft.VisualStudioCode --accept-source-agreements --accept-package-agreements
```

- "이 앱이 디바이스를 변경하도록 허용하시겠어요?" 창이 뜨면 **[예]**. 3~6분 걸려요.
- 셋 다 "설치했습니다(Successfully installed)"가 나오면 PowerShell은 닫아도 돼요.

### 2단계 — Git Bash: 게임 설치

시작 메뉴에서 `git bash` 검색 → **새로** 열기 (1단계가 끝난 뒤에 열어야 방금 깐 프로그램을 찾아요) → 아래 줄을 붙여 넣고 Enter.

```bash
npm install -g https://github.com/bjcho4141/sapjil-download/releases/latest/download/sapjil.tgz && node "$(npm root -g)/sapjil/dist/cli.js" init ~/sapjil-play
```

- Git Bash에서는 `Ctrl+V`가 안 돼요. **마우스 오른쪽 클릭 → Paste** (또는 `Shift+Insert`).
- 마지막에 노란 **🏗 공사 시작!**이 보이면 끝. 바탕화면에 「삽질코딩」 아이콘이 생겨요.

### 3단계 — 게임 시작

1. 바탕화면 **「삽질코딩」 아이콘 더블클릭** → 브라우저(게임 화면)와 **VS Code**가 같이 열려요.
2. VS Code 위쪽에 **"제한 모드"** 줄이 보이면 **[관리] → [신뢰]** — **터미널을 열기 전에 먼저!**
3. `Ctrl + J` → 아래에 **🏗 작업 기록 터미널**이 열려요. 미션은 여기서 해요.
   - 한 번 열어 두면 다음부터는 저절로 열려요.
   - 탭 이름이 `powershell`이면(신뢰하기 전에 연 것) 🗑 휴지통으로 닫고 `+`.

**끄기**: 게임 화면 오른쪽 위 **[⏻ 끄기]**. 다시 할 때는 아이콘만 누르면 돼요.

---

## 🍎 맥

> 시간 약 10분.

### 1단계 — 준비물 2개 설치

| 프로그램 | 설치 방법 |
|---|---|
| **Node.js** (22.12 이상) | [nodejs.org](https://nodejs.org/ko/download)에서 "LTS" 설치 파일을 받아 실행. Homebrew가 있으면 `brew install node` |
| **VS Code** | [code.visualstudio.com](https://code.visualstudio.com)에서 받아 **응용 프로그램** 폴더로 옮기기 |

### 2단계 — 터미널: 게임 설치

`⌘ + Space` → `터미널` 검색 → 열기 → 아래 줄을 붙여 넣고 Enter.

```bash
npm install -g https://github.com/bjcho4141/sapjil-download/releases/latest/download/sapjil.tgz && node "$(npm root -g)/sapjil/dist/cli.js" init ~/sapjil-play
```

- `EACCES`(권한) 오류가 나면 앞에 `sudo `를 붙여 `sudo npm install -g https://github.com/bjcho4141/sapjil-download/releases/latest/download/sapjil.tgz`를 먼저 하고(맥 비밀번호 입력), 그다음 `node "$(npm root -g)/sapjil/dist/cli.js" init ~/sapjil-play`.
- 마지막에 노란 **🏗 공사 시작!**이 보이면 끝. Dock에 「삽질코딩」 아이콘이 생겨요.

### 3단계 — 게임 시작

1. Dock의 **「삽질코딩」 아이콘** → 브라우저(게임 화면)와 **VS Code**가 같이 열려요. (처음에 "터미널을 제어하려고 합니다" 창이 뜨면 [허용])
2. VS Code 위쪽에 **"제한 모드"** 줄이 보이면 **[관리] → [신뢰]** — **터미널을 열기 전에 먼저!**
3. `⌘ + J` → 아래에 **🏗 작업 기록 터미널**이 열려요. 탭 이름이 `zsh`면 🗑으로 닫고 `+`.

**끄기**: 게임 화면 오른쪽 위 **[⏻ 끄기]**.

---

## 🔄 업데이트 (새 버전이 나왔을 때)

게임 폴더(`~/sapjil-play`)와 진행 상황은 **그대로** 남아요. 다시 설치할 필요 없어요.

### 🪟 윈도우

1. 게임 화면 오른쪽 위 **[⏻ 끄기]**
2. **Git Bash**를 열고 아래 줄을 붙여 넣고 Enter (`changed … packages`가 나오면 끝)

```bash
npm install -g https://github.com/bjcho4141/sapjil-download/releases/latest/download/sapjil.tgz
```

3. 바탕화면 **「삽질코딩」 아이콘** 더블클릭

### 🍎 맥

1. 게임 화면 오른쪽 위 **[⏻ 끄기]**
2. **터미널**을 열고 아래 줄을 붙여 넣고 Enter (`changed … packages`가 나오면 끝)

```bash
npm install -g https://github.com/bjcho4141/sapjil-download/releases/latest/download/sapjil.tgz
```

   권한(`EACCES`) 오류가 나면 이걸로 (맥 비밀번호를 물어봐요):

```bash
sudo npm install -g https://github.com/bjcho4141/sapjil-download/releases/latest/download/sapjil.tgz
```

3. Dock의 **「삽질코딩」 아이콘**

---

## 🆘 막히면

| 이런 게 보이면 | 이렇게 |
|---|---|
| `npm: command not found` | 프로그램 설치(1단계)가 끝났는지 보고, Git Bash/터미널을 **닫았다가 새로** 열어서 다시 |
| `sapjil: command not found` | 게임 아이콘으로 한 번 켜면 고쳐져요. 그 뒤 Git Bash/터미널을 새로 열어요 |
| VS Code 터미널이 `powershell`·`zsh` | 위쪽 "제한 모드" → [관리] → [신뢰] → 🗑으로 그 터미널 닫기 → `+` |
| 아이콘을 눌러도 아무 일이 없어요 | Git Bash/터미널에서 `cd ~/sapjil-play && node "$(npm root -g)/sapjil/dist/cli.js" play` 를 입력하고 나오는 화면을 캡처 |
| 그 밖에 이상한 화면 | 캡처해서(윈도우 `Win+Shift+S`, 맥 `⌘+Shift+4`) 보내 주세요. 테스트 버전이라 그게 제일 큰 도움이에요 |
