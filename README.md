# RobotArena

Unreal Engine 5.2.1의 블루프린트와 Paper2D / PaperZD로 제작한 횡스크롤 1:1 로봇 슈팅 게임입니다. 플레이어가 AI 상대와 작은 아레나에서 대결합니다.

## 주요 기능

- 좌우 이동, 점프, 이동 중 8방향 조준 및 사격
- 아래에서 통과하고 위에 착지하는 발판과 아래로 내려가기
- AI의 이동, 사격, 층간 이동
- 체력, 피격, 사망 애니메이션
- 시작 카운트다운, 승패 표시, 라운드 재시작

## 조작법

| 키 | 동작 |
| --- | --- |
| A / D | 좌우 이동 |
| Space | 점프 |
| 방향키 | 8방향 조준 |
| 왼쪽 Ctrl | 발사 |
| S | 발판 아래로 내려가기 |

## 프로젝트 열기

1. Unreal Engine 5.2.1을 설치합니다.
2. 해당 엔진에 UE 5.2용 PaperZD 플러그인을 설치합니다. 플러그인은 이 저장소에 포함되지 않습니다.
3. 저장소를 내려받은 뒤 `RobotArena.uproject`를 엽니다.
4. 시작 맵 `Content/RobotArena/Maps/MAP_Arena_Test`에서 플레이합니다.

이 저장소는 수정 가능한 언리얼 프로젝트 원본입니다. Windows 실행 파일(EXE)은 아직 제공하지 않습니다.

## 구조

- `Config`: 프로젝트 설정
- `Content/RobotArena/Blueprints`: 캐릭터, AI, 무기, 게임 흐름, UI
- `Content/RobotArena/Input`: Enhanced Input 액션 및 매핑
- `Content/RobotArena/Maps`: 아레나 맵
- `Content/RobotArena/PaperAssets`: 스프라이트, 플립북, 타일맵

공통 전투 기능은 `BP_FighterBase`, 플레이어 입력과 AI 판단은 각각 별도 블루프린트에서 처리합니다. 경기 흐름은 `GM_RobotArena`가 관리합니다.

## 개발 환경 및 아트

- Unreal Engine 5.2.1 / Blueprint
- Paper2D / PaperZD / Enhanced Input
- 싱글플레이: 플레이어 1명 대 AI 1명
- 현재 아트에는 생성형 이미지 기반의 임시 리소스가 포함되어 있습니다.

캐시와 빌드 중간 결과물은 저장소에서 제외했습니다. 기능 설명은 개발 기록을 기준으로 작성했으며, 배포용 빌드 검증은 아직 완료하지 않았습니다.
