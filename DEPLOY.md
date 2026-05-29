# 배포 가이드 (1회용)

> 이 파일은 강사 본인이 직접 1회 실행하는 단계입니다.
> 완료 후 Git/Vercel은 자동 운영되므로 이 파일은 삭제해도 됩니다.

## 사전 준비

- [ ] **GitHub 계정** — github.com에서 생성 (무료)
- [ ] **Vercel 계정** — vercel.com에서 GitHub로 로그인 (무료, 결제 정보 불필요)
- [ ] **Git 설치** — `git --version` 으로 확인. 없으면 [git-scm.com](https://git-scm.com) 다운로드

## Step A: GitHub 리포 생성 + 푸시

### A-1. 로컬에서 git 초기화

PowerShell을 `C:\Users\pc\shinhwa-ai-lecture\` 디렉토리에서 열고 실행:

```powershell
cd C:\Users\pc\shinhwa-ai-lecture
git init -b main
git config user.name "신화"
git config user.email "your-email@example.com"
git add .
git status
```

`git status` 출력에서 다음을 확인:
- `.claude/`나 `CLAUDE.md`가 안 보여야 함 (`.gitignore`로 제외됨)
- `lecture/`, `docs/`, `source/`, `README.md`, `vercel.json`, `.gitignore`만 보여야 함

### A-2. 첫 커밋

```powershell
git commit -m "Initial commit: 공인중개사 AI 활용 특강 v1.1.0"
```

### A-3. GitHub 리포 생성 (웹)

1. github.com 로그인 → 우상단 `+` → **New repository**
2. Repository name: `shinhwa-ai-lecture`
3. Description: `공인중개사를 위한 AI 활용 특강 (180분) - 5명 AI 에이전트 팀으로 제작`
4. **Public** 선택
5. **"Add a README file" 체크 해제** (이미 있음)
6. **"Add .gitignore" 체크 해제** (이미 있음)
7. **Create repository** 클릭

### A-4. 원격 연결 + 푸시

GitHub가 안내한 명령어 그대로 PowerShell에 입력 (대략 다음 형태):

```powershell
git remote add origin https://github.com/{본인-아이디}/shinhwa-ai-lecture.git
git push -u origin main
```

푸시 후 GitHub 페이지를 새로고침하면 파일이 보입니다.

## Step B: Vercel 자동 배포 연동

### B-1. Vercel 프로젝트 생성

1. vercel.com 로그인 → 우상단 **Add New** → **Project**
2. **Import Git Repository** 섹션에서 `shinhwa-ai-lecture` 리포 선택
3. (선택) Vercel에 GitHub 권한 부여가 처음이면 GitHub 권한 화면이 뜸 → All repositories 또는 본 리포만 선택 후 Install

### B-2. 빌드 설정 (그냥 둬도 됨)

- **Framework Preset:** Other (Vercel이 자동 감지)
- **Root Directory:** `./` (기본)
- **Build Command:** 비워두기
- **Output Directory:** 비워두기 (`vercel.json`이 처리)
- **Install Command:** 비워두기

`vercel.json`이 이미 있어서 추가 설정 불필요.

### B-3. Deploy 클릭

약 30초~1분 후 배포 완료. Vercel이 URL 발급:
- 예: `https://shinhwa-ai-lecture.vercel.app`
- 또는: `https://shinhwa-ai-lecture-{user}.vercel.app`

`/` 접속 → 루트 `index.html` 강의 페이지 표시 (정적 파일 직접 서빙).
`/practice` 접속 → `cleanUrls`로 `practice.html` 실습 자료 페이지 서빙.

### B-4. (선택) 커스텀 도메인

본인 도메인 (예: `lecture.shinhwa.kr`)이 있으면:
1. Vercel 프로젝트 → Settings → Domains
2. Add domain → 본인 도메인 입력
3. DNS 설정에 Vercel이 안내한 CNAME 레코드 추가

## Step C: 운영 — 업데이트할 때마다

콘텐츠 수정 후:

```powershell
cd C:\Users\pc\shinhwa-ai-lecture
git add .
git commit -m "Update: {뭘 바꿨는지 한 줄}"
git push
```

→ Vercel이 자동 감지하고 1분 이내 재배포. **별도 작업 불필요.**

### 미리보기 배포 (브랜치 활용, 선택)

큰 변경을 본 강의 자료에 반영하기 전 미리 확인하고 싶다면:

```powershell
git checkout -b update-module-3
# 수정
git add . && git commit -m "Update module 3"
git push -u origin update-module-3
```

Vercel이 자동으로 **프리뷰 URL**을 발급 (예: `shinhwa-ai-lecture-git-update-module-3-{user}.vercel.app`).
확인 후 만족스러우면:

```powershell
git checkout main
git merge update-module-3
git push
```

## Step D: 배포 후 URL 채워넣기

배포 URL을 받았으면 다음 파일에서 placeholder를 실제 URL로 교체:

- `README.md` (2곳 — "Live 강의 페이지", "실습 자료")
- `docs/case-study.md` (1곳 — "본 강의 페이지")
- `docs/student-guide.md`의 카톡 채널 안내 등

수정 후:

```powershell
git add . && git commit -m "docs: Add live URL" && git push
```

## 문제 해결

### "git push" 시 비밀번호 인증 거부
GitHub는 비밀번호 인증을 폐기함. **Personal Access Token (PAT)** 발급 필요:
1. github.com → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generate new token → repo 권한 체크 → Generate
3. 토큰을 비밀번호 대신 입력

또는 **GitHub CLI** (`gh auth login`) 또는 **SSH 키** 설정 권장.

### Vercel 배포 후 페이지가 404
- `index.html`·`practice.html`이 리포 **루트**에 있는지 확인 (정적 파일 직접 서빙, rewrites 미사용)
- `/practice`가 404면 `vercel.json`의 `cleanUrls: true` 설정 확인
- Vercel 프로젝트 → Deployment 상세 → Deployment Protection이 Disabled인지 확인

### Vercel 무료 플랜 한계
- 월 100GB 대역폭 (강의 페이지 트래픽으로는 충분)
- 빌드 시간 6,000분/월 (이 프로젝트는 빌드 거의 안 쓰니 무제한)
- 100건/분 요청 한도

## 완료 후 — 이 파일 삭제

배포가 안정적으로 작동하면 이 파일은 더 이상 필요 없음:

```powershell
git rm DEPLOY.md
git commit -m "chore: Remove one-time deploy guide"
git push
```

(또는 보관용으로 그대로 둬도 무방. 다음 강의 자료 만들 때 참고 가능.)
