# 🌴 Project Paradise

<!-- 커버 이미지 (1280x640 권장) -->
<p align="center">
  <img src="./assets/cover.png" alt="Project Paradise Cover" width="100%"/>
</p>

<!-- 배지 모음 -->
<p align="center">
  <img src="https://img.shields.io/badge/Unreal_Engine_5-000000?style=for-the-badge&logo=unrealengine&logoColor=white"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white"/>
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20Android-blue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge"/>
</p>

<p align="center">
  <a href="https://paradiseproject.github.io/ParadiseProject_Docs/">
    📄 API 문서 (Doxygen + GitHub Pages) 보러가기
  </a>
</p>

---

## 📌 프로젝트 소개

> 스쿼드 액션과 디펜스가 결합된 모바일 기반 전략 게임

| 항목 | 내용 |
|------|------|
| 🎮 장르 | 태그 액션 타워 디펜스 |
| 🖥️ 대상 플랫폼 | Windows (PC) / Android (Mobile) |
| 👥 개발 인원 | 5명 (유성민, 김성현, 김수진, 김민준, 최지원) |
| 📅 개발 기간 | 2026.02.03 ~ 2026.04.03 |
| ⚙️ 엔진 | Unreal Engine 5 |
| 💻 언어 | C++ |

---

## 🎬 시연 영상

<!-- 썸네일 이미지에 유튜브 링크를 연결 (GIF로 대체 가능) -->
<p align="center">
  <a href="https://youtube.com/링크를_입력하세요">
    <img src="./assets/thumbnail.png" alt="Demo Video" width="70%"/>
  </a>
</p>

---

## ✨ 주요 기능

| 기능 | 설명 | 코드 바로가기 |
|------|------|--------------| 
| 태그 시스템 | 전투 중 캐릭터를 실시간으로 교체하는 태그 액션 | [바로가기](./Source/) |
| 타워 디펜스 | 퍼밀리어 소환 및 방어 라인 구축 | [바로가기](./Source/) |
| 크로스 플랫폼 조작 | PC 키보드 / 모바일 가상 조이스틱 동시 지원 | [바로가기](./Source/) |
| 무기 스킬 & 궁극기 | 캐릭터별 고유 콤보 공격 및 필살기 | [바로가기](./Source/) |

---

## 🎮 조작 방법 (Controls)

본 프로젝트는 Windows(PC) 및 Android(Mobile) 크로스 플랫폼 조작을 지원합니다.

| 기능 | Windows (Key) | Android (UI) | 동작 정의 |
| :--- | :---: | :---: | :--- |
| **캐릭터 이동** | <kbd>W</kbd> <kbd>A</kbd> <kbd>S</kbd> <kbd>D</kbd> | 가상 조이스틱 (좌측 하단) | 8방향 자유 이동 및 이동 속도 비례 애니메이션 |
| **캐릭터 태그** | <kbd>U</kbd> <kbd>I</kbd> <kbd>O</kbd> | 캐릭터 아이콘 (우측 상단) | 해당 번호 캐릭터로 즉시 교체 |
| **기본 공격** | <kbd>J</kbd> | 공격 버튼 (우측 하단) | 장착된 무기로 고유 공격 |
| **무기 스킬** | <kbd>K</kbd> | 스킬 아이콘 (공격 버튼 좌측) | 장착된 무기로 콤보 공격 |
| **궁극기 (필살기)** | <kbd>L</kbd> | 궁극기 아이콘 (공격 버튼 상단) | 캐릭터의 고유한 궁극기 사용 |
| **퍼밀리어 소환** | <kbd>1</kbd> <kbd>2</kbd> <kbd>3</kbd> <kbd>4</kbd> <kbd>5</kbd> | 퍼밀리어 슬롯 (중앙 하단) | 슬롯에 등록된 유닛 소환 |

## 🗂️ 프로젝트 구조

```
📁 Source/
 ├── 📁 ParadiseProject/
 │    ├── 📁 Character/       # 캐릭터 & 태그 시스템
 │    ├── 📁 Combat/          # 공격, 스킬, 궁극기
 │    ├── 📁 Familiar/        # 퍼밀리어 소환 & AI
 │    ├── 📁 Tower/           # 타워 디펜스 로직
 │    ├── 📁 UI/              # HUD, 조이스틱, 슬롯 UI
 │    └── 📁 Core/            # 게임 모드, 매니저
📁 Content/
 ├── 📁 Characters/           # 캐릭터 에셋
 ├── 📁 Maps/                 # 레벨 & 맵
 ├── 📁 UI/                   # 위젯 블루프린트
 └── 📁 VFX/                  # 이펙트
📁 Config/                    # 프로젝트 설정
📁 Docs/                      # 기획서 & 문서
```

---

## 🛠️ 코드 컨벤션

### 에셋 관리
- UE5 기본 콘텐츠 브라우저 구조 준수
- 에셋 접두사 규칙: `BP_`, `SK_`, `SM_`, `T_`, `M_`, `WBP_` 등 Unreal 표준 적용

### 코드 스타일
- 변수명: `CamelCase` / 멤버 변수: `m_` 접두사
- 클래스명: UE5 표준 접두사 (`A`, `U`, `F`, `E` 등) 준수
- 주석은 `/** */` Doxygen 형식으로 작성 → [API 문서 자동 생성](https://paradiseproject.github.io/ParadiseProject_Docs/)

### 아키텍처
- Unreal 컴포넌트 기반 설계
- GameplayAbilitySystem(GAS) 활용 검토

---

## 📝 Git 컨벤션

### Commit Message Prefix

| prefix | 설명 |
|--------|------|
| `feat` | 새로운 기능 추가 |
| `fix` | 버그 수정 |
| `docs` | 문서 수정 |
| `refactor` | 코드 리팩토링 |
| `asset` | 에셋 추가 / 수정 |
| `chore` | 빌드, 설정 변경 |

```
feat: 태그 시스템 캐릭터 교체 로직 추가
fix: 모바일 조이스틱 입력 누락 버그 수정
asset: 퍼밀리어 소환 VFX 추가
```

### Branch 전략

| 브랜치 | 용도 |
|--------|------|
| `main` | 배포 / 최종 빌드 |
| `develop` | 개발 통합 브랜치 |
| `feature/기능명` | 기능 개발 |
| `fix/버그명` | 버그 수정 |

### PR 가이드
- PR은 `develop` 브랜치로 요청
- 최소 1인 이상 리뷰 후 머지
- PR 템플릿에 맞게 작성 필수

---

## 👥 팀원

| 이름 | 역할 | GitHub |
|------|------|--------|
| 유성민 | 　 | [@github-id](https://github.com/) |
| 김성현 | 　 | [@github-id](https://github.com/) |
| 김수진 | 　 | [@github-id](https://github.com/) |
| 김민준 | 　 | [@github-id](https://github.com/) |
| 최지원 | 　 | [@github-id](https://github.com/) |
