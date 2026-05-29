# 공인중개사를 위한 AI 활용 특강 (180분)

> 한국 공인중개사가 ChatGPT·Claude·Gamma·NotebookLM 등 AI 도구를 **법적으로 안전하게** 실무에 적용하기 위한 입문~중급 특강 자료.

**Live 강의 페이지:** https://shinhwa-ai-lecture.vercel.app
**실습 자료:** https://shinhwa-ai-lecture.vercel.app/practice

---

## 왜 만들었나

2024~2026년 한국 부동산 시장에서 AI 도구는 빠르게 확산되고 있지만, 동시에 **세 가지 결정적 리스크**가 함께 커지고 있다.

1. **광고법 위반** — AI 생성 콘텐츠 라벨 의무화(AI 기본법 제31조, 2026.1.22 시행), 위반건축물 표기 의무(2025.1.1), 광고법 위반 적발 연 1만 건 이상
2. **개인정보 유출** — 고객 실명·연락처를 ChatGPT에 그대로 입력하는 사고. 외산 LLM은 미국 서버 저장 → 개인정보보호법 제28조의8 국외이전 위반 소지
3. **AI 환각(Hallucination)** — ChatGPT가 가짜 법령 조문·판례를 자신 있게 인용. 검증 없이 고객에게 전달하면 법적 책임은 공인중개사에게 귀속

이 자료는 위 리스크를 **실무 워크플로우 안에서 회피하면서** AI를 활용하는 방법을 단계별로 다룬다.

## 무엇이 들어 있나

- **6개 모듈 / 111장 슬라이드 / 실습 6개 / 7일 챌린지** — 총 180분 강의분
- **법령 17건+ 인용** — 모든 조문 번호·시행일 1차 출처 검증 완료
- **표준 가상 매물** (마포구 공덕동 OO오피스텔) — 모듈 전반에 일관 사용
- **강사 모드** — 슬라이드 토글 한 번으로 강사 스크립트·진행 가이드 표시
- **실습 자료 별도 페이지** — 청중이 강의 후 사무실에서 다시 열어볼 수 있음
- **인쇄 친화 CSS** — PDF 저장 시 모듈별 page-break, 강사 스크립트 자동 포함

## 누가 쓰면 좋은가

| 대상 | 사용 방법 |
|------|----------|
| **공인중개사회·중개사 협회 강사** | 본 자료를 그대로 강의 사용 (라이선스 참조). 강의 시간이 다르면 모듈 가감 |
| **공인중개사 본인 (수강생)** | 강의 후 사무실에서 [Live 강의 페이지](.) 다시 열기 + [실습 자료](.) 따라 7일 챌린지 진행 |
| **다른 도메인 강사** | [docs/case-study.md](docs/case-study.md) — 하네스 구조로 도메인별 강의 자료 자동 생성하는 방법론 참고 |

## 빠른 시작

### 강사용 (강의 진행)

1. [index.html](index.html) 또는 배포된 URL을 강의장 컴퓨터에서 열기
2. 우상단 **"강사 모드 ON"** 버튼 클릭 → 강사 스크립트·진행 가이드 카드 표시
3. 모듈 4·5·6 시작 시 노란 가이드 카드(🎤) 먼저 읽고 시간 압축·옵션 슬라이드 판단
4. 자세한 운영 가이드: [docs/instructor-manual.md](docs/instructor-manual.md)

### 수강생용 (강의 후)

1. 강의장에서 받은 [실습 자료](practice.html) URL 열기
2. 모든 복사용 프롬프트 코드 블록 우하단의 **"복사"** 버튼 클릭 → ChatGPT에 붙여넣기
3. 7일 챌린지 (Day 1~7) 따라가기
4. 자세한 사용 가이드: [docs/student-guide.md](docs/student-guide.md)

## 시스템 구성 (어떻게 만들었나)

이 자료는 **5명의 AI 전문 에이전트 팀**이 협업하여 생성됐다. 사람 1명이 단독으로 4~6주 걸릴 작업을 약 4시간에 완료.

```
research-analyst (4명 병렬)
   ↓ 리서치 노트 4건
curriculum-designer
   ↓ 모듈 명세서
content-writer (3명 병렬)
   ↓ 슬라이드 + 강사 스크립트
html-builder
   ↓ HTML 강의 페이지
qa-reviewer (경계면 교차 검증)
```

자세한 구성·설계 의도·재현 가이드: **[docs/case-study.md](docs/case-study.md)** (← 발표·블로그용 사례 정리)

## 디렉토리 구조

```
shinhwa-ai-lecture/
├── README.md                  ← 이 파일
├── docs/
│   ├── instructor-manual.md   ← 강사 매뉴얼 (강의 진행 가이드)
│   ├── student-guide.md       ← 수강생 안내 (강의 후 활용법)
│   ├── change-log.md          ← 콘텐츠 변경 이력
│   ├── case-study.md          ← 하네스 구조 사례 (메타 콘텐츠)
│   └── screenshot-guide.md    ← 스크린샷 placeholder 가이드
├── lecture/                   ← 🚀 Vercel 배포 대상
│   ├── index.html             ← 강의 본문 (111장)
│   ├── practice.html          ← 실습 자료 모음
│   └── assets/                ← 스크린샷 이미지
└── source/                    ← 빌드 소스 (수정·재빌드용)
    ├── research/              ← 리서치 노트 4건
    ├── modules/               ← 슬라이드 .md 6개
    ├── curriculum.md          ← 커리큘럼 명세서
    └── qa-report.md           ← QA 검토 보고서
```

## 업데이트 워크플로우

자료를 수정·확장하고 싶을 때:

1. **소스 수정** — `source/modules/module-{N}.md` 또는 `source/research/{topic}.md` 수정
2. **HTML 재빌드** — Claude Code에서 `"모듈 N HTML 재빌드해줘"` 요청 → html-builder 에이전트가 `index.html` 동기화
3. **QA 재검증** (선택) — `"QA 다시 돌려줘"` 요청 → qa-reviewer가 경계면 검증
4. **변경 이력 기록** — `docs/change-log.md`에 한 줄 추가
5. **GitHub 푸시** — `git commit && git push` → Vercel 자동 배포

이 워크플로우는 `harness_system` 프로젝트의 하네스(5 에이전트 + 6 스킬)를 통해 자동화되어 있다. 자세한 내용: [docs/case-study.md](docs/case-study.md)

## 라이선스 & 인용

- **콘텐츠:** CC BY-NC-SA 4.0 (비상업적 사용 자유 / 출처 표시 / 동일조건변경허락)
- **상업 사용** (사내 교육·유료 강의 등): 별도 문의 — *(강사 이메일 placeholder)*
- **인용 시:** `신화. (2026). 공인중개사를 위한 AI 활용 특강. https://github.com/{user}/shinhwa-ai-lecture`

## 연락처

- **강사:** 공인중개사 신화 *(이름 placeholder)*
- **이메일:** *(placeholder)*
- **카톡 채널:** *(placeholder)*

## 변경 이력

전체 이력은 [docs/change-log.md](docs/change-log.md) 참조. 최신 5건:

- 2026-05-28 v1.0.0 첫 풀 사이클 — 180분 6모듈 110슬라이드 생성
- 2026-05-28 v1.0.1 강사 스크립트 톤 친근·구어체 일괄 변환
- 2026-05-28 v1.0.2 QA Major 4건 보완 (강사 진행 가이드 카드, 음성 백업 슬라이드 5-7B)
- 2026-05-28 v1.1.0 GitHub 리포 구조 정비 + 운영 문서 추가 + Vercel 배포
