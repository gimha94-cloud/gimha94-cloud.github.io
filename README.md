# 소원 기계 — 하이퍼 디포엠

하이퍼텍스트 구조의 디지털 시. 독자의 선택이 경로를 만든다.

## GitHub Pages 배포 방법

### 1단계 — 리포지토리 만들기

1. GitHub에 로그인 후 우측 상단 **+** → **New repository** 클릭
2. Repository name에 `username.github.io` 입력 (username은 본인 GitHub 아이디)
3. **Public** 선택
4. **Create repository** 클릭

### 2단계 — 파일 올리기

**방법 A: 웹에서 직접 업로드**
1. 리포지토리 페이지에서 **Add file** → **Upload files** 클릭
2. 이 폴더의 모든 파일 선택해서 드래그
3. **Commit changes** 클릭

**방법 B: Git으로 올리기**
```bash
git init
git add .
git commit -m "하이퍼 디포엠 첫 배포"
git branch -M main
git remote add origin https://github.com/username/username.github.io.git
git push -u origin main
```

### 3단계 — Pages 활성화 확인

1. 리포지토리 **Settings** → 좌측 **Pages**
2. Source: **Deploy from a branch**, Branch: **main**, Folder: **/ (root)**
3. **Save** 클릭
4. 약 1~2분 후 `https://username.github.io` 에서 확인

---

## 파일 구조

```
index.html          ← INTRO (입장 페이지)
unit1.html          ← 소원 선택
love.html           ← 사랑 소원
love-result.html    ← 사랑 결과
money.html          ← 돈 소원
money-result.html   ← 돈 결과
fame.html           ← 인기 소원
fame-result.html    ← 인기 결과
revenge.html        ← 복수 소원
revenge-result.html ← 복수 결과
freedom.html        ← 자유 소원
freedom-result.html ← 자유 결과
error.html          ← 시스템 오류 (모든 결과 → 여기로)
truth.html          ← 진실
last-choice.html    ← 마지막 선택
ending1.html        ← 엔딩 1: 삭제
ending2.html        ← 엔딩 2: 유지
ending-hidden.html  ← 숨겨진 엔딩 (ending1에서 숨겨진 링크)
style.css           ← 공유 스타일시트
```

## 협업 팁

- 각자 다른 HTML 파일을 맡아 내용 수정 가능
- `style.css`의 CSS 변수(`--accent`, `--danger` 등)만 바꾸면 전체 분위기 변경
- 새 경로 추가 시 HTML 파일 하나 더 만들고 링크 연결하면 됨
