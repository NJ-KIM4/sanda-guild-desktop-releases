# 산다길드 데스크톱 릴리즈 (sanda-guild-desktop-releases)

산다길드 데스크톱 앱(Tauri 2)의 자동 업데이트 매니페스트(`latest.json`)와 인스톨러를 호스팅하는 public 저장소입니다. 설치된 앱들이 이 저장소의 GitHub Releases를 자동 업데이트 서버로 직접 참조합니다.

## 구성

- `README.md` — 저장소 소개 문서.
- `_삭제금지_의존성정리.md` — 이 저장소를 삭제하면 안 되는 이유와 의존성 체인, 안전한 정리 조건을 정리한 메모.
- `.gitignore` — 시크릿(`.env`) 보호용 무시 규칙.

실제 배포 산출물(`.exe`, `.exe.sig`, `latest.json`)은 working tree가 아니라 GitHub **Releases**에 업로드되어 있습니다.

## 비고

- 데스크톱 앱 소스코드는 별도 private 저장소(`NJ-KIM4/nyanggames`)의 `projects/sanda_guild_desktop` 경로에 있으며, 릴리즈는 해당 저장소의 CI 워크플로(`desktop-release.yml`)를 통해 이 저장소로 발행됩니다.
- 자동 업데이트 매니페스트 URL: `https://github.com/NJ-KIM4/sanda-guild-desktop-releases/releases/latest/download/latest.json`

GitHub: https://github.com/NJ-KIM4/sanda-guild-desktop-releases
