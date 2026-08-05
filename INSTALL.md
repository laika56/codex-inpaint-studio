# Codex 인페인트 스킬 설치 요청서

이 문서를 받은 수강생은 **이 파일을 Codex 대화창에 첨부한 뒤** 아래처럼 요청하세요.

```text
첨부한 INSTALL.md의 지침대로 인페인트 스킬을 설치해줘.
```

---

## Codex가 수행할 작업

이 문서를 읽고 있는 Codex는 다음 공개 GitHub 경로의 스킬을 설치하세요.

```text
https://github.com/hueflowstudio/codex-inpaint-studio/tree/main/skills/inpaint-studio
```

설치 대상 폴더는 다음과 같습니다.

```text
~/.codex/skills/inpaint-studio
```

다음 파일이 모두 설치되어야 합니다.

```text
inpaint-studio/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── assets/
    └── inpaint-studio.html
```

### 설치 규칙

1. Codex의 GitHub 스킬 설치 기능을 우선 사용합니다.
2. 설치 기능을 사용할 수 없으면 저장소를 임시 폴더에 내려받고 `skills/inpaint-studio` 폴더를 설치 대상에 복사합니다.
3. 같은 이름의 기존 스킬이 있으면 임의로 덮어쓰지 말고 사용자에게 교체 여부를 확인합니다.
4. 설치 후 위의 세 파일이 존재하는지 확인합니다.
5. 사용자에게 새 대화를 열거나 Codex 앱을 다시 시작하라고 안내합니다.

## 설치 후 사용법

새 Codex 대화에서 다음과 같이 입력합니다.

```text
인페인트 스킬 열어줘
```

오른쪽 패널에 편집기가 열리면 사진을 불러오고 수정할 부분을 표시한 뒤 **코덱스로 보내기**를 누릅니다. Codex 입력창에서 `⌘V` 또는 `Ctrl+V`로 붙여넣고 원하는 수정 내용을 설명합니다.

