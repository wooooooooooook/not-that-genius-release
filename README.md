# Not That Genius (ntg)

**Radiology Context Assistant** — 판독문을 작성하는 바로 그 순간, 환자 소견에 꼭 맞는 정량적 영상의학 가이드라인과 추적 권고안을 실시간으로 제시하는 Windows 컴패니언입니다.

> 모든 걸 다 외울 필요는 없습니다. 어디서 찾아야 할지만 알면 됩니다.

[**Windows용 최신 빌드 다운로드**](https://github.com/wooooooooooook/not-that-genius-release/releases/latest)

> **Alpha** — 가이드라인 매칭과 PACS 컴패니언은 실제로 동작합니다. AI 소견 요약은 아직 포함되어 있지 않습니다.

---

## 무엇을 하는 도구인가

ntg는 진단을 대신하지 않습니다. 판독의가 소견을 기술할 때 기억하기 까다로운 수치 기준 — 결절 크기 구간, 추적 검사 간격, FNA·조직검사 컷오프 — 을 공인된 진료 지침 원문에 근거해 그 자리에서 보여주는 임상 컨텍스트 어시스턴트입니다.

지침 책자를 뒤적이거나 브라우저 탭을 오가지 않아도 되도록, 판독 창 옆에 작게 떠서 필요한 기준만 보여줍니다.

## 핵심 원칙

- **Zero-Click 자동 매칭** — 소견 텍스트에서 크기, 위치, 조영 양상, 위험 인자를 자동으로 인식해 별도의 클릭이나 검색어 입력 없이 연관 가이드라인을 띄웁니다.
- **검증된 근거 기반** — 학회 공인 가이드라인 원문의 정량 기준을 1:1로 대조해 수록했습니다. 임의로 생성된 수치가 없습니다.
- **프라이버시 중심 설계** — 환자 소견과 판독문은 외부 클라우드로 전송되지 않습니다. 가이드라인 매칭은 모두 사용자 워크스테이션 안에서 실행됩니다.

## 주요 기능

| 기능 | 설명 |
| --- | --- |
| 원클릭 판독문 삽입 | 추천된 권고문과 추적 관찰 주기를 판독문 하단 `[RECOMMENDATION]`에 바로 삽입합니다. |
| 정량 기준표 & 원문 링크 | 크기별 분류 테이블, 위험도 계층, 공식 논문 링크를 상세 화면에서 확인합니다. |
| 빠른 검색 (Ctrl/Cmd+K) | 판독 도중 언제든 전체 가이드라인을 검색하고 열람합니다. |
| 판독 창 옆 상주 | PACS 판독 창을 인식해 항상 위에 작게 표시하며, 이미지를 가리지 않습니다. |
| 자동 업데이트 | 서명된 업데이트 피드를 확인하고, 검증을 통과한 빌드만 사용자 확인 후 적용합니다. |

## 수록 가이드라인

총 **281개**의 큐레이션된 영상의학 가이드라인을 수록했습니다. 부위별 구성은 Chest & cardiovascular 56, Abdomen 70, Neuroradiology 88, Musculoskeletal 42, Head & Neck 15, Spine 10입니다.

대표 항목:

- **Fleischner 2017** — 폐 우연 결절 추적 (Solid & Subsolid)
- **ACR TI-RADS 2017** — 갑상선 결절 위험도 및 FNA 기준 (TR1–TR5)
- **Bosniak v2019** — 신장 낭종 CT/MRI 분류 (Class I–IV)
- **LI-RADS v2018** — 간세포암 고위험군 간 결절 표준 (LR-1–LR-5)
- **Pancreatic Cyst 2017** — 췌장 낭성 병변 (Fukuoka / ACR, IPMN·MCN)
- **Fazekas Scale** — 뇌 백질 고신호강도 정량 분류 (Grade 0–3)

> 수록 항목 중 26개 AJCC 병기 항목은 재배포 라이선스 사유로 은퇴(provenance 보존) 표시되어 있으며 임상 추천에서 제외됩니다.

## 다운로드 및 실행

1. [최신 릴리즈](https://github.com/wooooooooooook/not-that-genius-release/releases/latest)에서 `NTG-Companion_<version>_x64-portable.zip`을 내려받습니다.
2. 압축을 풀고 `NTG Companion.exe`를 실행합니다. 설치 프로그램은 필요 없습니다.
3. 전역 단축키 `Ctrl+Alt+Space`로 패널을 표시하거나 숨깁니다. 패널을 클릭하거나 스크롤하면 포커스가 잡힙니다.

**요구 사항**

- Windows 10 1809 이상 또는 Windows 11 (x64)
- Microsoft Edge WebView2 Evergreen 런타임 (대부분의 Windows 10/11에 기본 포함)

**데이터**

- 창 상태와 앱 데이터는 실행 파일 옆의 `app-data` 폴더에 저장됩니다. 폴더를 지우면 초기화됩니다.
- 쓰기 가능한 위치에 두어야 합니다. 읽기 전용 폴더에서는 시작되지 않습니다.
- Program Files나 레지스트리에 아무것도 쓰지 않습니다. 삭제는 폴더 삭제로 끝납니다.

## 로드맵

**지금 · Alpha (제공 중)**

- 281개 가이드라인 자동 매칭
- PACS 판독 창 자동 인식 · 항상 위 표시
- 자동 업데이트
- Windows 10/11, 설치 없이 실행

**다음 · Beta (진행 중)**

- AI 소견 요약 · 설명 *(아직 없음)*
- 다양한 PACS 뷰어 호환성 확대
- 소견 · 결론 · 권고 구분 개선
- 듀얼 모니터 환경 최적화

**그다음 · Release (계획, 일정 미정)**

- 병원 정보시스템 연동 및 판독 서식
- 팀 지식 관리 · 사용 기록
- 정식 배포를 위한 보안 요건
- macOS 지원 검토

## 자주 묻는 질문

**AI가 진단을 대신 내리나요?**
아닙니다. ntg는 의사의 진단과 판단을 대체하지 않습니다. 소견을 기술할 때 참조할 수치 기준을 공인 지침에 근거해 찾아주는 보조 도구입니다.

**환자의 판독문이나 개인정보가 외부로 전송되나요?**
전송하지 않습니다. 가이드라인 매칭은 로컬에서만 실행되며, 소견 텍스트는 기기 밖으로 나가지 않습니다.

**기존 PACS나 판독 환경을 바꿔야 하나요?**
아닙니다. 기존 PACS 및 판독 워크스테이션 옆에 뜨는 작은 컴패니언으로 동작합니다. 판독 동선과 기존 소프트웨어는 그대로 두면 됩니다.

**AI가 소견을 요약해 주나요?**
아직 아닙니다. 알파 빌드는 공인 지침에 고정된 규칙으로만 추천합니다. AI 요약은 베타 단계 작업입니다.

## 릴리즈 자산과 업데이트 피드

This public repository hosts the signed release artifacts for the Not That Genius Windows companion. The source repository stays private.

- Latest portable build: <https://github.com/wooooooooooook/not-that-genius-release/releases/latest>
- Signed update feed: <https://github.com/wooooooooooook/not-that-genius-release/releases/latest/download/latest-portable.json>

Each release contains the portable ZIP, its detached Ed25519 signature, and the signed `latest-portable.json` manifest. The app verifies the manifest signature and the ZIP hash before installing an update.

This repository contains release artifacts only. It is created and populated by the `Desktop Release` workflow in the source repository and by `npm run desktop:publish:github`.

## 고지

Not That Genius는 개발 중인 알파 단계의 임상 판단 보조 소프트웨어입니다. 단독 진단이나 법적 의료 행위를 대신하지 않으며, 모든 최종 판단과 책임은 판독하는 의료인에게 있습니다. AI 요약 기능은 아직 포함되어 있지 않습니다.

*Alpha · 개발 중*
