# STAT 4710J — Midterm Review | Fall 2026

## About these materials

This package contains two complementary resources for the STAT 4710J midterm review:

| File | Purpose |
| --- | --- |
| `STAT4710J_Midterm_Review_Material.pdf` | The 47-page review handout: concepts, explanations, code examples, in-class practice, and reference answers. |
| `STAT4710J_Midterm_Review_Code_Practice_English(2).ipynb` | A companion Jupyter notebook with executable examples, sample datasets, SQL exercises, visualizations, and checks. |

**Use the PDF to study the concepts and the notebook to test the code.** The PDF is a reading/print copy, not an editable Word document. The notebook can be edited and executed.

## Topics covered

The handout and notebook follow the same broad chapter sequence:

1. Data Fundamentals and Exploratory Data Analysis (EDA)
2. Pandas I & II — indexing, filtering, strings, GroupBy, pivot tables, and joins
3. Text Data — string methods and regular expressions
4. Text Representation and Embeddings — BoW, n-grams, TF-IDF, cosine similarity, and Word2Vec concepts
5. Data on the Internet — HTTP, JSON, APIs, HTML, and BeautifulSoup
6. Visualization — distributions, plots, KDE, and visual design
7. SQL I & II — filtering, grouping, HAVING, CASE, NULL, and joins
8. Machine Learning Supplement — OLS, evaluation, cross-validation, regularization, and bias–variance

**Scope note:** Chapter 8 is labeled as supplementary. Confirm its inclusion in the current midterm syllabus with the instructor.

## Getting started with the notebook

### Option A: Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Choose **File → Upload notebook** and select the `.ipynb` file.
3. Run the setup cells first, then work through the notebook from top to bottom.
4. If a package is missing, install it in a separate code cell, then rerun the affected cell.

### Option B: JupyterLab / Jupyter Notebook (local)

1. Install Python 3.10+ and JupyterLab (or Jupyter Notebook).
2. Open a terminal in the folder containing the notebook.
3. Create and activate a virtual environment if desired.
4. Install the dependencies:

   ```bash
   python -m pip install jupyterlab numpy pandas matplotlib seaborn scipy scikit-learn requests beautifulsoup4
   ```

5. Launch JupyterLab:

   ```bash
   jupyter lab
   ```

6. Open the notebook and select a Python kernel.

`sqlite3`, `re`, and `json` are included with Python and do not need separate installation.

### Important note about the first notebook cells

The uploaded notebook begins with several `!pip install` commands, including a line with a misspelled `intall` command. **Do not use those cells as your definitive setup instructions.** Install packages using the command above, then skip the notebook's installation cells and start with its import/setup and data cells. In Colab, package installation commands can be run in a new cell when needed.

## Recommended study workflow

1. **Read a topic in the PDF.** Focus on the definitions, syntax, and highlighted distinctions.
2. **Attempt the in-class practice before reading its reference answer.** Many practice questions have answers immediately after them in the PDF.
3. **Open the corresponding notebook section.** Section numbers generally match the PDF's chapter structure, although individual exercises and code cells are not necessarily one-to-one.
4. **Run the code in order.** Some cells reuse variables, DataFrames, imports, and database connections created earlier.
5. **Change a value or condition.** Predict the output, rerun the cell, and compare.
6. **Revisit mistakes.** Pay particular attention to indexing, Boolean conditions, grouping, regex capture groups, SQL query order, and joins.

For a fresh start, restart the kernel and run the notebook cells sequentially, skipping the problematic package-installation cells described above.

## How to use the exercises

- **Concept questions:** Explain the answer in words before checking the PDF.
- **Pandas and regex questions:** Write the expression yourself, then test it on the notebook's example data.
- **Visualization questions:** Identify the variable types, choose a suitable plot, and explain what the plot shows.
- **SQL questions:** Work out the required rows, groups, and joins before running the query. The notebook uses an in-memory SQLite database for its SQL examples.
- **Machine learning questions:** Focus on interpreting the concepts and checking code behavior, subject to the instructor's confirmed exam scope.

## Practical notes and troubleshooting

**`NameError` or a missing DataFrame:** Run the earlier setup and data-definition cells in order.

**`ModuleNotFoundError`:** Install the missing dependency in the same Python environment/kernel used by Jupyter, then restart the kernel if necessary.

**Unexpected results after multiple runs:** Restart the kernel and run sequentially. Some cells modify data or create SQL tables.

**Plots do not appear:** Ensure the plotting cells were executed and that the notebook is using a working Python kernel.

**SQL syntax differences:** The notebook uses SQLite. Some SQL features and syntax vary across database systems.

**Internet access:** The notebook's illustrative `requests` example is commented out, but installing packages requires network access unless dependencies are already installed. Avoid uncommenting live web requests unless you understand the website's access rules and rate limits.

## For instructors and teaching assistants

The PDF is suitable as a guided review handout or presentation reference. The notebook is intended for live demonstrations and independent code verification. Because the PDF includes reference answers, consider asking students to attempt each question before revealing the solution. Check the current course syllabus and test all demonstration cells in the classroom environment before the session.

These resources support review; they do not replace the official lectures, labs, assignments, or instructor announcements. The presence of a topic here does not guarantee that it will appear on the exam.
