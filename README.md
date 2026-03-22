# Python Web Crawling Basics

This is a learning project to practice HTML/CSS fundamentals and static web page crawling step by step.  
Using `requests`, `BeautifulSoup`, and `pandas`, it covers extracting data from pages, organizing it into tabular form, and saving to Excel.

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

1. **Learn HTML/CSS basics**
   - `01.HTMLCSS/01.HTML_BASIC.html`: Basic HTML elements such as headings, links, inputs, and lists
   - `01.HTMLCSS/02.CSS_BASIC.html`: Styling with id/class selectors and child combinators

2. **Static page crawling basics**
   - `02.static_page_crawling/01.library_usage.ipynb`
   - Request HTML with `requests.get()`
   - Parse with `BeautifulSoup` and use `select_one()`

3. **Extract a single item**
   - `02.static_page_crawling/02.step1.ipynb`
   - Extract category, product name, detail link, and price
   - Clean price using string preprocessing (`strip`, `replace`, `split`)

4. **Loop over multiple items**
   - `02.static_page_crawling/03.step2.ipynb`
   - Use `select('.product')` and iterate through the list

5. **Handle pagination**
   - `02.static_page_crawling/04.step3_copy.ipynb`
   - Iterate `?page=1~4` to collect multiple pages

6. **Create DataFrame and save to Excel**
   - `02.static_page_crawling/05.step4.ipynb`
   - Convert collected results into a `pandas.DataFrame`
   - Save to `result.xlsx`

## Environment

- Python 3.10.11
- Jupyter Notebook
- Key libraries
  - `requests`
  - `beautifulsoup4`
  - `pandas`
  - `openpyxl` (for Excel export)

## Virtual Environment Setup (based on current environment)

Current `venv` info:
- Python: `3.10.11`
- `include-system-site-packages = false`

### 1) Create and activate venv (Windows PowerShell)

```bash
python -m venv venv
.\venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
```

### 2) Install the same package versions

```bash
pip install beautifulsoup4==4.14.3 bs4==0.0.2 openpyxl==3.1.5 pandas==2.3.3 requests==2.32.5
pip install ipykernel==7.2.0 ipython==8.38.0 jupyter_client==8.8.0 jupyter_core==5.9.1 pyzmq==27.1.0 tornado==6.5.5 traitlets==5.14.3
```

### 3) Run

```bash
jupyter notebook
```

If needed, you can lock the current environment by exporting exact versions:

```bash
pip freeze > requirements.txt
```

## File-by-File Summary

- `.gitignore`: Excludes Python caches, virtual env (`venv/`), notebook checkpoints, outputs (`result.xlsx`), archives (`*.zip`) from Git tracking.
- `01.HTMLCSS/01.HTML_BASIC.html`: Example page using basic HTML tags (`h1`, `p`, `a`, `input`, `button`, `ul/li`).
- `01.HTMLCSS/02.CSS_BASIC.html`: Styling examples using `id/class` selectors and child combinators (`>`).
- `02.static_page_crawling/01.library_usage.ipynb`: Basics of `requests` + `BeautifulSoup`, checking `select_one`, `attrs`, and `text`.
- `02.static_page_crawling/02.step1.ipynb`: Extracts category/name/link/price for a single product with string preprocessing.
- `02.static_page_crawling/03.step2.ipynb`: Iterates through the full product list to extract multiple items.
- `02.static_page_crawling/04.step3_copy.ipynb`: Pagination crawling by iterating page numbers (`?page=1~4`).
- `02.static_page_crawling/05.step4.ipynb`: Accumulates data into a list, converts to `DataFrame`, and saves as `result.xlsx`.
- `02.static_page_crawling/DScover_11기양희석_화면캡쳐.png`: Screenshot image related to the exercise/submission.
- `README.md`: Project overview, how to run, learning flow, file summaries.

## Notes

- The exercise output (`result.xlsx`) is reproducible and excluded via `.gitignore`.
- The development virtual environment (`venv/`) is also excluded from version control.

