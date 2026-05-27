# 🚇 Coding Metro — 코딩 입문자를 위한 지하철 노선도 기반 게이미피케이션 학습 플랫폼

> 파편화된 코딩 지식을 지하철 노선도 메타포로 체계화한 인터랙티브 웹 학습 플랫폼

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/ko/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://developer.mozilla.org/ko/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/ko/docs/Web/JavaScript)
[![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=flat&logo=jquery&logoColor=white)](https://jquery.com/)

---

## 📖 프로젝트 소개

**Coding Metro**는 코딩 학습자들이 직면하는 **정보 과부하 문제**와 **체계적인 로드맵 부재**를 해결하기 위해 개발된 웹 기반 학습 플랫폼입니다.

지하철 노선도를 메타포로 활용하여 프론트엔드, 백엔드, CS 기초, 개발도구 등 핵심 코딩 개념 16개를 '역(Station)'으로 시각화하고, 게이미피케이션 요소를 통해 학습 동기를 지속적으로 유지할 수 있도록 설계하였습니다.

---

## ✨ 주요 기능

### 🗺️ 노선도 맵
- **4개 노선, 16개 역** 배치 (1호선 웹 프론트엔드 / 2호선 백엔드 / 3호선 CS기초 / 4호선 개발도구)
- 역 클릭 시 열차 아이콘이 CSS `transition`으로 해당 역으로 이동
- 노선 필터 버튼(1~4호선 / ALL)으로 원하는 노선만 하이라이트
- 환승역(JavaScript역, Database역)에서 다른 노선으로 자연스럽게 전환
- 학습 완료한 역에 깃발 아이콘 표시

### 📋 학습 정보 패널 (우측)
- **대기 / 도착 / 학습 정보** 3가지 상태 전환
- 각 역의 개념 설명, 권장 학습 방법, 검색 키워드, 참고자료 링크 제공
- 이전·다음 역 탐색 버튼으로 노선 따라 순차 이동

### 🎮 게이미피케이션
- 헤더 **CLEAR 카운터** 실시간 갱신 (0 / 16)
- 16개 역 전부 완주 시 **Canvas 폭죽 애니메이션**
- **수료증 오버레이** 발급 (완료 날짜 + 학습한 역 목록)
- 완주 후 수료증 재열람 버튼 및 Footer 히든 메시지 등장

### 🔊 효과음
| 상황 | 파일 |
|---|---|
| 역 도착 | `station_arrive.mp3` |
| 하차(내리기) | `door_open.mp3` |
| 학습 완료 | `complete_chime.mp3` |
| 전체 완주 | `all_clear_fanfare.mp3` |

### 📱 반응형 웹
- 900px 이하에서 태블릿/모바일 세로 레이아웃 자동 전환
- `100svh` 적용으로 iOS Safari 주소창 대응

---

## 🛠️ 기술 스택

| 구분 | 기술 |
|---|---|
| 마크업 | HTML5 |
| 스타일 | CSS3 (Flexbox, CSS Variables, `clamp()`, Media Query) |
| 스크립팅 | JavaScript (ES6+), jQuery 3.7.1 |
| 그래픽 | SVG, HTML5 Canvas |
| 오디오 | HTML `<audio>` 태그 |
| 폰트 | Press Start 2P, Noto Sans KR (Google Fonts) |
| 빌드 도구 | 없음 (순수 정적 웹, 별도 설치 불필요) |

---

## 📁 파일 구조

```
Coding-Metro/
├── index.html          # 전체 소스 (HTML + CSS + JavaScript 통합)
├── sounds/
│   ├── station_arrive.mp3
│   ├── door_open.mp3
│   ├── complete_chime.mp3
│   └── all_clear_fanfare.mp3
└── README.md
```

---

## 🚀 실행 가이드

별도의 서버나 패키지 설치가 **필요 없습니다.** 아래 두 가지 방법 중 하나를 선택하세요.

### 방법 1. GitHub에서 직접 다운로드

1. 우측 상단 **`Code`** 버튼 클릭 → **`Download ZIP`** 선택
2. 다운로드된 ZIP 파일 압축 해제
3. 압축 해제된 폴더 안의 **`index.html`** 파일을 브라우저로 열기

### 방법 2. Git으로 클론

```bash
git clone https://github.com/HotteokDough/Coding-Metro.git
cd Coding-Metro
```

클론 후 `index.html` 파일을 브라우저로 열면 바로 실행됩니다.

> **⚠️ 주의사항**
> - `index.html`과 `sounds/` 폴더는 **반드시 같은 위치**에 있어야 효과음이 재생됩니다.
> - 효과음 자동재생 정책으로 인해 **첫 클릭 이후**부터 소리가 재생됩니다.
> - 최적 환경: **Chrome** 또는 **Edge** 최신 버전 권장

---

## 🗺️ 노선도 구성

| 호선 | 테마 | 역 목록 |
|---|---|---|
| 1호선 (파란색) | 웹 프론트엔드 | HTML/CSS → JavaScript → DOM/이벤트 → React/Vue |
| 2호선 (초록색) | 백엔드 언어 | Python/Java → 네트워크 → JavaScript → Database → Node.js/Spring |
| 3호선 (금색) | CS 기초 | C언어 → 자료구조 → Database → 컴퓨터구조 → 운영체제 |
| 4호선 (보라색) | 개발도구 | Git기초 → GitHub → UI/UX기획 → 웹배포 |

> **환승역**: JavaScript역 (1·2호선), Database역 (2·3호선)  
> **출발역**: Hello, World!역 (전 노선 공통)

---

## 👥 팀 정보

**팀명:** 타코켓챱  
**소속:** 경기대학교 소프트웨어경영대학 AI컴퓨터공학부  
**수행 기간:** 2026년 3월 ~ 6월 (2026학년도 1학기)

| 이름 | 역할 |
|---|---|
| 장서윤 | 팀장 · 프로젝트 총괄 · 플랫폼 최종 아키텍처 구현 · 3호선 구현 · 논문 초안 작성 및 최종 수정 · 영상 스토리보드 및 제작 |
| 정세린 | 1호선 구현 · 논문 선행 연구 및 기술 분석 자료조사 · 발표 영상 제작 · 시연영상 촬영 |
| 박채정 | 2호선 구현 · 논문 데이터 분석 및 효과 검증 자료조사 · 논문 컴파일 및 교정 · 발표 PPT 제작 |
| 박정현 | 4호선 구현 · 논문 학술적 배경 및 당위성 확립 자료조사 · 논문 컴파일 및 교정 · 최종보고서 작성 |

---

## 📄 라이선스

본 프로젝트는 경기대학교 2026학년도 1학기 웹프로그래밍 산학협력 프로젝트 결과물입니다.

**본 ReadMe는 초안작성 후 AI로 다듬었습니다.**
