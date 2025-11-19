<!-- Profile README for https://github.com/JuYongwoo -->

<h1 align="center">게임 개발자 주용우</h1>
<p align="center">
  <a href="https://github.com/JuYongwoo"><img alt="GitHub followers" src="https://img.shields.io/github/followers/JuYongwoo?style=flat&label=Followers"></a>
  <a href="https://github.com/JuYongwoo?tab=repositories"><img alt="Total Stars" src="https://img.shields.io/github/stars/JuYongwoo?affiliations=OWNER%2CCOLLABORATOR&style=flat&label=Stars"></a>
  <a href="https://github.com/JuYongwoo"><img alt="Profile Views" src="https://komarev.com/ghpvc/?username=JuYongwoo&style=flat&color=blueviolet"></a><br/>
</p>

<p align="center">
  <b>Game Developer · Unity Specialist · AI & Systems Enthusiast</b><br/>
  협업과 유지보수를 최우선으로 고려하여, 빠르게 개발하고 오래 서비스할 수 있는 구조를 설계합니다.<br/>
  대형 프로젝트에서는 매니저를 적극 사용하고 소-중형 프로젝트에서는 컴포넌트 스스로 완결 구조를 가지도록 하고 있습니다.<br/>
</p>

---

## 소개
- 캐주얼 2D부터 3D·공포 장르까지 **상용 수준의 플레이 흐름**을 설계·구현합니다.
- 모든 커밋은 전부 기록에 남아 있으며 대부분 직접 개발하였고 AI의 사용은 널 체크, 오탈자, 간단한 기능 구현에 사용되었습니다.
- Scriptable Object를 통해 리소스 중앙 제어 및 패키지화 하는 것을 좋아합니다.
---

## 기술 스택
**클라이언트**  
Unity (UGUI, Addressables, ScriptableObject, asmdef, Editor 확장) · Android Studio · Unreal Engine 5.1

**서버**  
.NET(C#) · Linux(Ubuntu) · AWS · SQLite

**공통 설계**  
DRY · SOLID · FSM · MVC · Event Aggregator · Object Pooling · GitHub Actions(CI)

---

# 프로젝트 하이라이트

## Farm — 3D 호러 퍼즐  
[리포지토리](https://github.com/JuYongwoo/Farm_Public) · [다운로드](https://github.com/JuYongwoo/Farm_Public/releases)

![게임 시연](https://github.com/JuYongwoo/Farm_Public/blob/main/README/Farm_GIF1.gif)

- **핵심 설계**: 리플렉트 이용한 함수 다형성, ScriptableObject 기반 이벤트 실행, 매니저가 없는 컴포넌트 완결 구조
- **주요 모듈**: `ItemsInteractable`, `PlayerInteractor`, `EventSO`
- **리포지토리 구조(요약)**
  ```
  작성 중입니다.
  ```

---

## ArrowBattle — 2D 액션 횡스크롤  
[리포지토리](https://github.com/JuYongwoo/ArrowBattle_Public) · [다운로드](https://github.com/JuYongwoo/ArrowBattle_Public/releases)

![게임 시연](https://raw.githubusercontent.com/JuYongWoo/ArrowBattle_Public/main/README/ArrowBattle_GIF1.gif)

- **핵심 설계**: Addressables 기반 리소스 로드/캐시, ScriptableObject 데이터 캡슐화, 오브젝트 풀링, 이벤트 허브, UGUI UI 계층화
- **주요 모듈**: `ResourceManager`, `PoolManager`, `AudioManager`, `Enemy/Player`
- **리포지토리 구조(요약)**
  ```
  Scripts/
  ├─ Characters
  ├─ Commons
  ├─ Managers
  ├─ Scenes
  ├─ Skills
  ├─ SOs
  ├─ UIs
  └─ Utils
  ```

---

## JewelPop — 캐주얼 퍼즐  
[리포지토리](https://github.com/JuYongwoo/JewelPop_Public) · [다운로드](https://github.com/JuYongwoo/JewelPop_Public/releases)

![게임 시연](https://github.com/JuYongWoo/JewelPop_Public/main/README/JewelPop_GIF1.gif)

- **핵심 설계**: Addressables 자산 관리, ScriptableObject로 단계/과일 데이터 분리, 풀링 기반 생성/회수, 이벤트 허브, UGUI
- **주요 모듈**: `EventManager`, `PoolManager`, `ResourceManager`, `SoundManager`, `InputManager`, `FruitDataSO`, `ScorePanel`
- **리포지토리 구조(요약)**
  ```
  Scripts/
  ├─ Cameras · Commons · Fruits · Managers · Scenes
  ├─ ScriptableObjects · UIs · Utils
  ```

---

## RandomSurvival — 탑다운 액션 생존  
[리포지토리](https://github.com/JuYongwoo/RandomSurvival_Public) · [다운로드](https://github.com/JuYongwoo/RandomSurvival_Public/releases)

![게임 시연](https://github.com/JuYongwoo/RandomSurvival_Public/blob/main/README/RandomSurvival_GIF1.gif)

- **핵심 설계**: 이벤트 허브, Addressables 리소스 허브(`ResourceManager`), ScriptableObject 기반 밸런스/무기/타일, FSM 상태 전환, UGUI HUD
- **시스템 구성**: CSV→타일 SO 매핑 `MapManager`, 경량 TCP 클라이언트 골격 `Managers/Core/NetworkClient`
- **리포지토리 구조(요약)**
  ```
  Scripts/
  ├─ Commons · Enemies · Items · Managers(Core 포함)
  ├─ Maps · Players · Scenes · SOs · UIs · Utils
  ```

> DOTS/ECS는 본 리포지토리 스크립트 범위에서 사용 내역을 확인하지 않았습니다.

---

## Tunnel — 1인칭 3D 공포  
[리포지토리](https://github.com/JuYongwoo/Tunnel_Public) · [다운로드](https://github.com/JuYongwoo/Tunnel_Public/releases)

![게임 시연](https://github.com/JuYongWoo/Tunnel_Public/raw/main/README/Tunnel_GIF.gif)

- **핵심 설계**: Addressables 리소스 관리, 이벤트 허브, UGUI, 오브젝트 풀링
- **트리거 파이프라인**: `SOs/TriggerEventSO` + `Scenes/Systems/TriggerEventManager`로 씬 이벤트 시퀀스화
- **게임플레이**: 상호작용(`Door`, `Key`, `MovingWall`), 적 AI(`Following`, `Patrolling`, `Zombie`)
- **리포지토리 구조(요약)**
  ```
  Scripts/
  ├─ Commons · Enemy · Items · Managers · Player
  ├─ Scenes/Systems · SOs · UI · Utils
  ```

---

## JellySuika — 물리 낙하·합체 퍼즐  
[리포지토리](https://github.com/JuYongwoo/JellySuika_Public) · [다운로드](https://github.com/JuYongwoo/JellySuika_Public/releases)

![게임 시연](https://github.com/JuYongwoo/JellySuika_Public/blob/main/README/JellySuika_GIF1.gif)

- **핵심 설계**: 풀링·리소스 허브·이벤트 허브, Addressables 자산 관리, UGUI
- **주요 모듈**: `PoolManager`, `ResourceManager`, `InputManager`, `SoundManager`, `FruitDataSO`, `Title/Score Panel`
- **리포지토리 구조(요약)**
  ```
  Scripts/
  ├─ Cameras · Commons · Fruits · Managers · Scenes
  ├─ ScriptableObjects · UIs · Utils
  ```

---

## 상용 프로젝트
**BattleOops!** (Google Play 배포)  
- 모바일 RTS, **클라이언트 & 서버 개발 담당**  
- Firebase Ads 연동, 서버–DB 연동, UI/UX  
- NDA로 코드 미공개

---

## 학력·경력
- 2025 명지대학교 컴퓨터공학과 석사 (4.38/4.5)  
- 2022 청주대학교 컴퓨터정보공학과 (3.89/4.5)  
- 前 ㈜퍼니뎁 모바일 게임개발 인턴 (2021-09-01 ~ 2021-12-31)  
- 前 ㈜퍼니뎁 모바일 게임개발 계약직 (2022-01-01 ~ 2022-12-31)  
- 석사 논문: *1인칭 슈팅 게임 속 AI 분류 및 개선*

## 자격·수상
- 정보처리기사, 정보처리산업기사, 리눅스마스터 2급  
- 충북게임아카데미 프로그래밍 최우수상(2021), 그래픽 우수상(2020)  
- 교내 학습동아리 최우수상(2017)

---

## 연락처
- Email: **parsnip618@outlook.com**  
- GitHub: [JuYongwoo](https://github.com/JuYongwoo)

