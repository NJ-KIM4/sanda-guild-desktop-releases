# sanda-guild-desktop-releases — Claude 작업 가이드

## 개요

이 repo는 **산다길드 데스크톱 앱(`sanda-guild-desktop`, Tauri 2)의 릴리즈/자동 업데이트 매니페스트(`latest.json`) + 인스톨러(`.exe`, `.exe.sig`) 호스팅 전용 public 저장소**입니다.

- 설치된 앱들이 이 repo의 GitHub **Releases**를 자동 업데이트 서버로 직접 참조합니다.
- 실제 배포 산출물(`latest.json`, `.exe`, `.exe.sig`)은 working tree가 아니라 GitHub **Releases**에 있습니다.
- 로컬 working tree에는 `README.md`, `_삭제금지_의존성정리.md`, `.gitignore`만 존재합니다.
- **빌드 시스템이 없습니다.** 릴리즈는 `nyanggames`(private)의 CI 워크플로(`desktop-release.yml`)가 이 repo로 발행합니다.
- 매니페스트 URL: `https://github.com/NJ-KIM4/sanda-guild-desktop-releases/releases/latest/download/latest.json`

## 규칙·주의

- **코드 작업 repo가 아닙니다.** 여기서 앱 기능/소스를 수정하지 마세요. 실제 앱 코드는 별도 repo(`sanda-guild-desktop`, 소스는 private `nyanggames`의 `projects/sanda_guild_desktop`)에 있습니다.
- **`latest.json` 형식·서명에 주의.** 자동 업데이트는 minisign 공개키로 `.sig` 서명을 검증합니다. 매니페스트 구조나 서명을 손으로 건드리면 출고된 앱들의 자동 업데이트가 깨질 수 있습니다.
- **임의 파일 삭제 금지.** 특히 `_삭제금지_` 표기 파일(`_삭제금지_의존성정리.md`)은 의존성 체인과 삭제 금지 사유를 담고 있으니 절대 지우지 마세요.
- 이 repo는 설치된 앱·웹(sandakoko.kr)·CI가 의존하므로 **repo 자체를 삭제하면 안 됩니다.** 자세한 의존성/안전 조건은 `_삭제금지_의존성정리.md` 참고.
- 시크릿(`.env`, `*.key`, credential 등)은 `.gitignore`로 보호됩니다. 커밋하지 마세요.
