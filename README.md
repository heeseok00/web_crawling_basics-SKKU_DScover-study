# Python Web Crawling Basics

HTML/CSS 기초와 정적 웹페이지 크롤링을 단계별로 연습하는 학습용 프로젝트입니다.  
`requests`, `BeautifulSoup`, `pandas`를 사용해 페이지에서 데이터를 추출하고, 표 형태로 정리해 엑셀로 저장하는 흐름까지 다룹니다.

## Project Structure

```text
python_web_crawling/
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

- Python 3.10+
- Jupyter Notebook
- 주요 라이브러리
  - `requests`
  - `beautifulsoup4`
  - `pandas`
  - (엑셀 저장 시) `openpyxl`

## How to Run

1. 가상환경 생성 및 활성화
2. 필요한 패키지 설치
3. Jupyter 실행 후 노트북을 순서대로 실행

예시 명령:

```bash
pip install requests beautifulsoup4 pandas openpyxl jupyter
jupyter notebook
```

## Notes

- 실습 산출물(`result.xlsx`)은 재생성 가능한 파일이라 `.gitignore`에서 제외되어 있습니다.
- 학습 중 사용한 가상환경(`venv/`)도 버전 관리에서 제외되어 있습니다.

