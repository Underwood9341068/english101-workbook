# ENGLISH101 · 모의고사 워크북 생성기

> 고1 전국연합학력평가 모의고사 PDF를 업로드하면  
> **해석 연습 워크북**과 **단어 시험지**를 자동으로 만들어주는 웹앱

---

## 🖥️ 데모

**GitHub Pages**: `https://[내 계정].github.io/english101-workbook/`

---

## ✨ 기능

| 기능 | 설명 |
|------|------|
| PDF 자동 분석 | 모의고사 PDF → 문제 자동 추출 |
| 문장 해석 워크북 | 1문제 1페이지 / 굴림 9pt / 교사용+학생용 |
| 단어 시험지 | 2문제 1페이지 / 랜덤 셔플 / 교사용 답지 동일 순서 |
| 4가지 출력 | 워크북(교사/학생) + 단어시험지(교사/학생) 각각 .docx |

---

## 🚀 GitHub Pages 배포 방법

### 1. 저장소 생성
```
GitHub → New repository → 이름: english101-workbook → Public → Create
```

### 2. 파일 업로드
```
index.html 파일을 저장소 루트에 업로드
```

### 3. Pages 활성화
```
Settings → Pages → Source: main branch / (root) → Save
```

### 4. 접속
```
https://[내계정].github.io/english101-workbook/
```

---

## 🔑 API 키 설정

1. [console.anthropic.com](https://console.anthropic.com) 접속
2. API Keys → Create Key
3. 앱 실행 후 Step 1에서 키 입력 (브라우저 로컬스토리지에만 저장)

> ⚠️ API 사용 비용: 문서 1건당 약 $0.02~0.05 (Claude claude-opus-4-5 기준)

---

## 📋 사용 방법

```
Step 1  API 키 입력
Step 2  모의고사 PDF 업로드 (텍스트 PDF, 스캔본 불가)
Step 3  문제 범위 설정 (기본: 21~40번) → 생성 시작
Step 4  4개 파일 다운로드
```

---

## 📁 출력 파일 형식

### 해석 워크북
- A4 / 굴림 9pt / 상하 2.5cm · 좌우 2cm
- **교사용**: 한국어 해석 녹색 텍스트
- **학생용**: 해석 칸 빈칸 (EN = KR 동일 너비)
- 푸터: ENGLISH101 로고 + 페이지 번호

### 단어 시험지
- 6열 구조 (No. | 영어 | 뜻 | No. | 영어 | 뜻)
- 2문제씩 1페이지 구성
- Fisher-Yates 셔플 (교사/학생 동일 순서 보장)
- **교사용**: 녹색 답지 / **학생용**: 빈칸

---

## 🛠️ 기술 스택

- **Pure HTML/CSS/JS** (프레임워크 없음)
- [PDF.js](https://cdnjs.cloudflare.com/ajax/libs/pdf.js/) — PDF 텍스트 추출
- [docx.js](https://unpkg.com/docx@9.6.1/) — Word 파일 생성
- [Anthropic Claude API](https://api.anthropic.com) — AI 문장 분석 및 번역

---

## ⚙️ 지원 PDF

- ✅ 한국교육과정평가원 공식 문제지 PDF
- ✅ EBSi 다운로드 PDF
- ❌ 스캔 이미지 PDF (텍스트 레이어 없는 파일)

---

## 📝 License

MIT License — 자유롭게 수정·배포 가능합니다.

---

Made with ❤️ for Korean English teachers · ENGLISH101
