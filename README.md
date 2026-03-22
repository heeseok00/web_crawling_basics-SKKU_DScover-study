# Python Web Crawling Basics

HTML/CSS 기초와 정적 웹페이지 크롤링을 단계별로 연습하는 학습용 프로젝트입니다.  
`requests`, `BeautifulSoup`, `pandas`를 사용해 페이지에서 데이터를 추출하고, 표 형태로 정리해 엑셀로 저장하는 흐름까지 다룹니다.

## Project Structure

```text
python_web_crawling/
├─ .gitignore
├─ 01.HTMLCSS/
│  ├─ 01.HTML_BASIC.html
│  └─ 02.CSS_BASIC.html
├─ 02.static_page_crawling/
│  ├─ 01.library_usage.ipynb
│  ├─ 02.step1.ipynb
│  ├─ 03.step2.ipynb
│  ├─ 04.step3_copy.ipynb
│  ├─ 05.step4.ipynb
│  └─ DScover_11기양희석_화면캡쳐.png
└─ README.md
```

## Learning Flow

1. **HTML/CSS 기본 문법 익히기**
   - `01.HTMLCSS/01.HTML_BASIC.html`: 태그 구조, 링크, 입력 폼, 리스트 등 기본 HTML 요소
   - `01.HTMLCSS/02.CSS_BASIC.html`: id/class 선택자, 자식 선택자, 박스 스타일링

2. **정적 페이지 크롤링 기초**
   - `02.static_page_crawling/01.library_usage.ipynb`
   - `requests.get()`으로 HTML 요청
   - `BeautifulSoup`으로 파싱 후 `select_one()` 사용

3. **단일 상품 데이터 추출**
   - `02.static_page_crawling/02.step1.ipynb`
   - 카테고리, 상품명, 상세 링크, 가격 추출
   - 문자열 전처리(`strip`, `replace`, `split`)로 가격 정리

4. **여러 상품 반복 수집**
   - `02.static_page_crawling/03.step2.ipynb`
   - `select('.product')` + 반복문으로 목록 수집

5. **페이지네이션 처리**
   - `02.static_page_crawling/04.step3_copy.ipynb`
   - `?page=1~4`를 순회하며 다중 페이지 수집

6. **데이터프레임 생성 및 엑셀 저장**
   - `02.static_page_crawling/05.step4.ipynb`
   - 수집 결과를 `pandas.DataFrame`으로 변환
   - `result.xlsx`로 저장

## Environment

- Python 3.10.11
- Jupyter Notebook
- 주요 라이브러리
  - `requests`
  - `beautifulsoup4`
  - `pandas`
  - (엑셀 저장 시) `openpyxl`

## Virtual Environment Setup (현재 환경 기준)

현재 프로젝트의 `venv` 정보:
- Python: `3.10.11`
- `include-system-site-packages = false`

### 1) 가상환경 생성/활성화 (Windows PowerShell)

```bash
python -m venv venv
.\venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
```

### 2) 현재 설치 버전 그대로 설치

```bash
pip install beautifulsoup4==4.14.3 bs4==0.0.2 openpyxl==3.1.5 pandas==2.3.3 requests==2.32.5
pip install ipykernel==7.2.0 ipython==8.38.0 jupyter_client==8.8.0 jupyter_core==5.9.1 pyzmq==27.1.0 tornado==6.5.5 traitlets==5.14.3
```

### 3) 실행

```bash
jupyter notebook
```

필요 시 현재 환경을 잠그려면 아래 명령으로 버전 목록을 만들 수 있습니다.

```bash
pip freeze > requirements.txt
```

## File-by-File Summary

- `.gitignore`: Python 캐시, 가상환경(`venv/`), 노트북 체크포인트, 산출물(`result.xlsx`), 압축파일(`*.zip`) 등을 Git 추적에서 제외.
- `01.HTMLCSS/01.HTML_BASIC.html`: HTML 기본 태그(`h1`, `p`, `a`, `input`, `button`, `ul/li`) 사용 예제 페이지.
- `01.HTMLCSS/02.CSS_BASIC.html`: `id/class` 선택자와 자식 선택자(`>`)를 활용한 기본 스타일링 예제.
- `02.static_page_crawling/01.library_usage.ipynb`: `requests` + `BeautifulSoup` 기본 사용법과 `select_one`, `attrs`, `text` 확인.
- `02.static_page_crawling/02.step1.ipynb`: 단일 상품의 카테고리/이름/링크/가격 추출 및 문자열 전처리.
- `02.static_page_crawling/03.step2.ipynb`: 상품 리스트 전체를 반복문으로 순회하며 다건 데이터 추출.
- `02.static_page_crawling/04.step3_copy.ipynb`: 페이지 번호(`?page=1~4`)를 순회하는 페이지네이션 크롤링.
- `02.static_page_crawling/05.step4.ipynb`: 수집 데이터를 리스트로 누적해 `DataFrame`으로 변환하고 `result.xlsx`로 저장.
- `02.static_page_crawling/DScover_11기양희석_화면캡쳐.png`: 실습/제출 관련 화면 캡처 이미지.
- `README.md`: 프로젝트 개요, 실행 방법, 학습 흐름, 파일 요약 문서.

## Notes

- 실습 산출물(`result.xlsx`)은 재생성 가능한 파일이라 `.gitignore`에서 제외되어 있습니다.
- 학습 중 사용한 가상환경(`venv/`)도 버전 관리에서 제외되어 있습니다.

