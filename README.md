# Codex 인페인트 스튜디오

Codex 데스크톱 앱의 오른쪽 패널에서 실행되는 한국어 인페인팅 마스크 편집기입니다.

사진을 불러오거나 붙여넣은 뒤 사각형, 원형, 다각형, 브러시 등으로 수정할 영역을 표시할 수 있습니다. 표시된 이미지를 클립보드에 복사해 Codex에 전달하면 선택 영역만 수정하도록 요청할 수 있습니다.

## 주요 기능

- 파일 선택, 드래그 앤 드롭, 클립보드 붙여넣기
- 사각형, 원형, 다각형, 브러시 선택
- 지우개, 실행 취소, 마스크 초기화
- 이미지 자르기
- 흑백 마스크 PNG와 표시 이미지 내보내기
- **코덱스로 보내기**를 통한 클립보드 복사

마스크에서는 흰색 또는 표시된 영역이 수정 대상이며 검은색 영역은 보존 대상입니다.

## 수강생에게 파일 하나로 전달하기

저장소의 [`INSTALL.md`](INSTALL.md)만 수강생에게 전달하면 됩니다. 수강생은 파일을 Codex 대화창에 첨부하고 다음과 같이 요청합니다.

```text
첨부한 INSTALL.md의 지침대로 인페인트 스킬을 설치해줘.
```

Codex가 이 공개 저장소에서 필요한 스킬 파일을 내려받아 설치합니다.

## 설치 방법 1: Codex에 설치 요청하기

Codex 대화창에 아래 문장을 입력하세요.

```text
https://github.com/hueflowstudio/codex-inpaint-studio/tree/main/skills/inpaint-studio
여기에 있는 인페인트 스킬을 설치해줘
```

설치가 끝나면 새 대화를 열거나 Codex 앱을 다시 시작하세요.

## 설치 방법 2: ZIP으로 직접 설치하기

1. 이 저장소 페이지에서 **Code → Download ZIP**을 선택합니다.
2. 다운로드한 ZIP 파일의 압축을 풉니다.
3. `skills/inpaint-studio` 폴더 전체를 아래 위치에 복사합니다.

```text
~/.codex/skills/inpaint-studio
```

최종 폴더 구조는 다음과 같아야 합니다.

```text
~/.codex/skills/inpaint-studio/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── assets/
    └── inpaint-studio.html
```

복사 후 새 대화를 열거나 Codex 앱을 다시 시작하세요.

## 터미널로 설치하기

macOS 또는 Linux에서 다음 명령을 실행할 수 있습니다.

```bash
temp_dir="$(mktemp -d)"
git clone --depth 1 https://github.com/hueflowstudio/codex-inpaint-studio.git "$temp_dir/codex-inpaint-studio"
mkdir -p "$HOME/.codex/skills"
cp -R "$temp_dir/codex-inpaint-studio/skills/inpaint-studio" "$HOME/.codex/skills/inpaint-studio"
```

기존에 같은 이름의 스킬이 설치되어 있다면 먼저 해당 폴더를 별도로 백업한 뒤 교체하세요.

## 사용 방법

Codex에서 다음과 같이 입력합니다.

```text
인페인트 스킬 열어줘
```

오른쪽 패널에 편집기가 열리면:

1. 사진을 불러오거나 붙여넣습니다.
2. 수정할 부분을 도구로 표시합니다.
3. **코덱스로 보내기**를 누릅니다.
4. Codex 입력창을 선택하고 `⌘V` 또는 `Ctrl+V`를 누릅니다.
5. 표시한 영역을 어떻게 바꿀지 설명합니다.

예시:

```text
표시한 영역의 의자를 밝은 원목 의자로 바꿔줘. 나머지 부분은 그대로 유지해줘.
```

## 문제 해결

### 오른쪽 패널이 열리지 않을 때

- 새 대화에서 다시 `인페인트 스킬 열어줘`라고 입력합니다.
- Codex 앱을 완전히 종료한 뒤 다시 실행합니다.
- 설치 경로가 `~/.codex/skills/inpaint-studio/SKILL.md`인지 확인합니다.

### 클립보드 복사가 되지 않을 때

- 클립보드 접근 권한을 허용하고 다시 시도합니다.
- **표시 이미지** 버튼으로 파일을 저장한 뒤 Codex 입력창에 직접 첨부합니다.

## 지원 환경

- Codex 데스크톱 앱
- macOS, Windows 또는 Linux에서 사용자 스킬 폴더를 사용할 수 있는 환경
