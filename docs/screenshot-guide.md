# 스크린샷 캡처 가이드

> **대상:** 강사 (신화 공인중개사) | **작성:** html-builder 시스템 | **목적:** index.html의 placeholder 29곳을 실제 스크린샷으로 교체

---

## 1. 사용 방법

1. 이 문서를 인쇄해서 옆에 두고, 노트북으로 캡처 작업 진행
2. 표의 **우선순위 ⭐** 표시된 항목부터 캡처 (없으면 강의 진행은 가능하나 시각적 임팩트 ↓)
3. 캡처한 PNG 파일을 `_workspace/output/assets/` 디렉토리에 저장
4. 모든 캡처가 끝나면 — 또는 일부라도 — "스크린샷 N개 캡처 완료, HTML 교체해줘"라고 요청하면 html-builder가 일괄 `<img>` 태그로 교체

## 2. 파일명 규칙

```
m{모듈번호}-s{슬라이드번호}-{설명}.png
```

예시:
- `m1-s8-chatgpt-signup.png`
- `m2-s11-chatgpt-3tones.png`
- `m5-s6-mobile-mic.png`

**규칙:**
- 소문자·하이픈만 사용 (공백·한글·언더스코어 금지)
- 설명은 영문 2~4단어로 핵심만
- 5-7B처럼 알파벳 포함 슬라이드는 `m5-s7b-text-fallback.png`

## 3. 권장 해상도·포맷

| 용도 | 해상도 | 포맷 |
|------|--------|------|
| 강의장 빔프로젝터 (1920×1080 기준) | **1600×900 이상** | PNG (선호) / JPG |
| 모바일 화면 캡처 | 실제 크기 그대로 (휴대폰 화면 비율) | PNG |
| 일러스트·인포그래픽 (placeholder가 "일러스트"인 경우) | 1200×675 이상 | PNG (투명 배경) |
| QR 코드 | 600×600 | PNG |

**파일 크기:** 장당 500KB 이하 권장. 클 경우 [TinyPNG](https://tinypng.com)로 압축.

## 4. ⚠️ 마스킹 필수 — 캡처 전 점검

다음 정보가 화면에 보이면 **반드시 모자이크·블러·검은 박스**로 가리기:

- 실명 (강사·고객·실제 사람)
- 전화번호·이메일
- 실제 매물 주소·동·호수
- 결제 카드 번호 / 계좌 번호
- 사업자등록번호
- 브라우저 상단의 다른 탭 (개인 정보 노출 위험)

**팁:** 캡처 후 [Windows 기본 사진 앱](ms-photos:)이나 [Squoosh](https://squoosh.app) 같은 무료 도구로 모자이크 처리.

## 5. 표준 가상 매물 (모듈 1~5에서 일관 사용)

스크린샷에 매물 정보가 들어갈 경우, 다음 가상 매물 사용:

> **서울 마포구 공덕동 OO오피스텔**
> - 전용 23㎡ (약 7평), 신축
> - 보증금 5천만원 / 월 80만원
> - 공덕역 5호선·6호선·공항철도 도보 3분
> - 빌트인 풀옵션 (에어컨·세탁기·냉장고·인덕션)

표준 가상 고객: **고객A** (30대 여성, 1인 가구 직장인, 마포 근무)

## 6. 전체 캡처 목록 (29개)

### 모듈 1 — 오프닝 + AI 첫 켜기 (5개)

| 슬라이드 | Placeholder 현재 텍스트 | 추천 캡처 화면 | 파일명 | 우선순위 |
|---------|----------------------|--------------|--------|---------|
| 1-1 | 공덕역 인근 사무소 야경 (강사 배경) | 공덕역 부근 야경 사진 또는 강사 사무실 외관 (Unsplash 등 무료 이미지도 가능) | `m1-s1-mapo-night.jpg` | ⭐ |
| 1-2 | 강사 프로필 사진 | 강사 본인 정장/세미정장 프로필 (전문성 강조) | `m1-s2-instructor.png` | ⭐ |
| 1-8 | ChatGPT 가입 화면 (Sign up 버튼 강조) | chatgpt.com/auth/signup 화면, Sign up 버튼에 빨간 동그라미 | `m1-s8-chatgpt-signup.png` | ⭐ |
| 1-9 | ChatGPT 첫 화면 — 입력창에 화살표 표시 | ChatGPT 로그인 후 첫 화면, "Message ChatGPT…" 입력창에 빨간 화살표 | `m1-s9-chatgpt-home.png` | ⭐ |
| 1-11 | ChatGPT Settings > Data Controls 화면 | 우상단 프로필 → Settings → Data controls 메뉴, "Improve the model for everyone" OFF 강조 | `m1-s11-data-controls.png` | ⭐⭐ |

### 모듈 2 — 매물 광고문 + 법령 3중 준수 (9개)

| 슬라이드 | Placeholder 현재 텍스트 | 추천 캡처 화면 | 파일명 | 우선순위 |
|---------|----------------------|--------------|--------|---------|
| 2-1 | 마포구 공덕동 야경 + 광고문 텍스트 합성 | 1-1 야경에 광고문 텍스트 1~2줄 오버레이 (Canva로 30초 합성) | `m2-s1-ad-overlay.jpg` |  |
| 2-3 | 한국경제 기사 캡처 | "매물 소개글 4초만에 — 한국경제" 기사 화면 캡처 (저작권 표시 작게) | `m2-s3-hankyung-article.png` |  |
| 2-6 | 네이버 부동산 광고 + "위반건축물" 표시 강조 | 네이버 부동산 매물 광고 캡처에 "위반건축물" 박스 빨간 강조 (가상 매물로 자체 작성 권장) | `m2-s6-illegal-building-mark.png` | ⭐⭐ |
| 2-10 | 강사 화면 미리보기 (ChatGPT에 프롬프트 붙여넣기) | ChatGPT 화면에 5블록 광고 프롬프트가 입력된 상태 캡처 | `m2-s10-prompt-input.png` | ⭐ |
| 2-11 | ChatGPT 3톤 결과 화면 | 같은 매물로 공손/친근/전문가 톤 3개 결과가 나란히 보이는 화면 | `m2-s11-chatgpt-3tones.png` | ⭐⭐ |
| 2-16 | AI 생성 인테리어 시안 + "AI 생성" 워터마크 | Midjourney·DALL-E 등으로 생성한 가상 인테리어 + 좌하단 "AI 생성 이미지" 워터마크 | `m2-s16-ai-image-watermark.png` | ⭐ |
| 2-17 | GPTs Create 화면 캡처 | chatgpt.com/gpts/editor 진입 화면 (이름·설명·Instructions 입력란) | `m2-s17-gpts-create.png` |  |
| 2-18 | Claude Projects 화면 | claude.ai/projects 새 프로젝트 생성 화면 | `m2-s18-claude-projects.png` |  |
| 2-19 | Gamma 결과 예시 | gamma.app에서 광고문으로 카드뉴스 1장 생성한 결과 화면 | `m2-s19-gamma-result.png` | ⭐ |

### 모듈 3 — 고객 응대 + 개인정보 마스킹 (3개)

| 슬라이드 | Placeholder 현재 텍스트 | 추천 캡처 화면 | 파일명 | 우선순위 |
|---------|----------------------|--------------|--------|---------|
| 3-1 | 카톡 말풍선 → 메모장 → ChatGPT 3단 흐름도 | Canva/Figma로 3단계 흐름 다이어그램 작성 (① 카톡 ② 메모장 마스킹 ③ ChatGPT) | `m3-s1-masking-flow.png` | ⭐⭐ |
| 3-6 | 메모장 Ctrl+H 창 | Windows 메모장에서 Ctrl+H "찾기/바꾸기" 창이 열린 상태 — "010-1234-5678" → "010-****-****" 입력 예시 | `m3-s6-notepad-replace.png` | ⭐⭐ |
| 3-11 | ChatGPT 응답 화면 | 마스킹된 카톡 대화를 ChatGPT가 받아 답변 초안 3톤(공손/친근/전문) 생성한 결과 | `m3-s11-chatgpt-response.png` | ⭐ |

### 모듈 4 — 시장·법령 리서치 + 환각 검증 (4개)

| 슬라이드 | Placeholder 현재 텍스트 | 추천 캡처 화면 | 파일명 | 우선순위 |
|---------|----------------------|--------------|--------|---------|
| 4-1 | ChatGPT 답변 → 4개 1차 출처 사이트 검증 도식 | Canva/Figma로 다이어그램: [ChatGPT 답변] → 화살표 4개 → [law.go.kr / rt.molit.go.kr / glaw.scourt.go.kr / pipc.go.kr] | `m4-s1-1st-source-check.png` | ⭐⭐ |
| 4-5 | law.go.kr 검색 화면 | 법제처 사이트에서 "공인중개사법 제25조" 검색 결과 화면 | `m4-s5-law-search.png` | ⭐ |
| 4-7 | rt.molit.go.kr 검색 결과 | 국토부 실거래가 사이트에서 "마포구 공덕동 오피스텔" 검색 결과 화면 | `m4-s7-molit-search.png` | ⭐ |
| 4-12 | NotebookLM 인용 표시 화면 | notebooklm.google에 정책 PDF 업로드 후 답변에 인용 번호 표시된 화면 | `m4-s12-notebooklm-citation.png` | ⭐⭐ |

### 모듈 5 — 통합 실습 (답사→음성→광고→발송) (8개)

| 슬라이드 | Placeholder 현재 텍스트 | 추천 캡처 화면 | 파일명 | 우선순위 |
|---------|----------------------|--------------|--------|---------|
| 5-1 | 휴대폰을 들고 차량 운전석에서 음성 입력하는 일러스트 | 무료 일러스트 사이트 (unDraw, freepik 무료) 또는 강사 본인 사진 | `m5-s1-mobile-voice.png` |  |
| 5-3 | "30분 → 30초" 화살표 인포그래픽 | Canva 인포그래픽 템플릿으로 "30분" → "30초" 시각화 | `m5-s3-time-savings.png` |  |
| 5-4 | 5단계 플로우차트 | Canva/draw.io로 ① 음성 ② 텍스트 변환 ③ 정보 카드 ④ 광고 생성 ⑤ 카톡 발송 다이어그램 | `m5-s4-workflow-5steps.png` | ⭐⭐ |
| 5-6 | ChatGPT 모바일 앱 마이크 버튼 | ChatGPT iOS/Android 앱에서 입력창 옆 마이크 아이콘이 활성화된 화면 | `m5-s6-mobile-mic.png` | ⭐⭐ |
| 5-7B | 휴대폰 메모장 → ChatGPT 웹 화면 흐름 (백업) | 휴대폰 메모장 캡처 + 화살표 + ChatGPT 웹 화면 합성 (2장 가로 연결) | `m5-s7b-text-fallback.png` |  |
| 5-8 | ChatGPT가 음성을 텍스트로 변환한 화면 | ChatGPT 음성 모드 → 변환된 텍스트가 채팅창에 들어간 화면 | `m5-s8-voice-to-text.png` | ⭐ |
| 5-? (추가) | 매물 정보 카드 출력 화면 | ChatGPT가 음성 메모를 정리해 매물 정보 카드(주소·면적·가격·특징)로 출력한 화면 | `m5-s9-info-card.png` | ⭐ |
| 5-? (추가) | 카톡 발송 직전 화면 | ChatGPT가 생성한 답변을 카톡 "나에게 보내기"에 붙여넣은 화면 | `m5-s15-kakao-send.png` | ⭐ |

### 모듈 6 — Q&A + 마무리 (2개 QR)

| 슬라이드 | Placeholder 현재 텍스트 | 추천 캡처 화면 | 파일명 | 우선순위 |
|---------|----------------------|--------------|--------|---------|
| 6-9 | QR 코드 5개 (강사 발표 직전 생성) | qrcodemonkey·qr-code-generator 등에서 추가 학습 리소스 5개 URL의 QR 한 장에 모아 생성 | `m6-s9-qr-resources.png` | ⭐ |
| 6-10 | 강사 카톡 채널 QR · 피드백 Google Form QR | 강사 카톡 채널 + Google Form 두 QR을 한 슬라이드에 좌우 배치 | `m6-s10-qr-feedback.png` | ⭐⭐ |

## 7. 우선순위 정리

**⭐⭐ 최우선 (강의 핵심 차별화 시각 — 12장):**
- 1-11 Data Controls (개인정보 안전)
- 2-6 위반건축물 표기 (법령 차별화)
- 2-11 ChatGPT 3톤 결과 (광고 자동화 핵심)
- 3-1 마스킹 흐름도 (모듈 3 핵심 비주얼)
- 3-6 메모장 Ctrl+H (마스킹 실전 도구)
- 4-1 1차 출처 검증 도식 (모듈 4 핵심)
- 4-12 NotebookLM 인용 (환각 회피)
- 5-4 5단계 워크플로우 (모듈 5 핵심)
- 5-6 모바일 마이크 (현장 ROI)
- 6-10 강사 채널 QR (강의 후 연결)
- 1-1, 1-2 (강사 신뢰감)

**⭐ 권장 (시각적 임팩트 — 12장):**
- 1-8, 1-9, 2-10, 2-16, 2-19, 3-11, 4-5, 4-7, 5-8, 5-9, 5-15, 6-9

**우선순위 없음 (선택 — 5장):**
- 2-1, 2-3, 2-17, 2-18, 5-1, 5-3, 5-7B

## 8. 작업 추천 순서

1. **Day 1 — 강의 핵심 ⭐⭐ 12장 캡처** (약 2시간)
   - ChatGPT·법제처·국토부 사이트 직접 들어가 자체 캡처
   - 다이어그램은 Canva 무료 템플릿 활용
2. **Day 2 — ⭐ 권장 12장** (약 1.5시간)
3. **Day 3 — 마스킹 검수 + 압축**
   - 모든 PNG를 TinyPNG로 압축
   - 개인정보 모자이크 누락 점검
4. **Day 4 — 강사에게 "캡처 완료, HTML 교체해줘" 요청**

## 9. assets/ 디렉토리 배치

```
_workspace/output/
├── index.html
├── practice.html
└── assets/
    ├── m1-s1-mapo-night.jpg
    ├── m1-s2-instructor.png
    ├── m1-s8-chatgpt-signup.png
    ├── ...
    └── m6-s10-qr-feedback.png
```

## 10. HTML 교체 자동화 (참고)

캡처 완료 후 강사가 다음 요청을 하면 html-builder가 일괄 처리:

> "스크린샷 N개 캡처 완료, HTML 교체해줘"

html-builder는 `assets/` 폴더를 스캔하여 파일명 규칙(`m{N}-s{X}-...`)으로 매칭, 해당 `<figure class="placeholder">` 블록을 다음으로 교체:

```html
<figure class="screenshot">
  <img src="assets/m1-s9-chatgpt-home.png" alt="ChatGPT 첫 화면">
  <figcaption>ChatGPT 첫 화면 — 입력창에 화살표 표시</figcaption>
</figure>
```

`<figure class="placeholder">`에서 `<figure class="screenshot">`로 클래스 변경되면 CSS가 자동으로 점선 박스→실제 이미지 박스로 전환됩니다.

## 11. 시간이 정말 없을 때 — 미니멈 캡처 (5장)

이 5장만 캡처해도 강의 진행 가능:

1. **1-9** — ChatGPT 첫 화면 (강의 시작)
2. **2-11** — ChatGPT 3톤 결과 (모듈 2 시연)
3. **3-6** — 메모장 Ctrl+H (모듈 3 마스킹)
4. **4-12** — NotebookLM 인용 (모듈 4 핵심)
5. **5-6** — 모바일 마이크 버튼 (모듈 5 시연)

나머지는 placeholder 점선 박스 그대로 두고 강사가 말로 보완.

---

**문서 작성:** 2026-05-28 | **최종 갱신:** 동일 | **다음 단계:** 위 순서대로 캡처 → "HTML 교체해줘" 요청
