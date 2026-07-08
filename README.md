# Job Listings Analysis

An exploratory data analysis project investigating which factors influence how many views a job listing receives.

The analysis focuses on listing views rather than applications because the source data contains fewer missing values for views, making it a more reliable target for comparison and visualization.

## Research Question

**What factors influence how many views a job listing receives?**

## Project Overview

This notebook combines multiple job posting datasets, cleans salary and location fields, and visualizes how listing views vary across:

- Annual salary
- U.S. state
- Remote work availability
- Job title
- Experience level

The project is written as a Jupyter Notebook and uses Python for data cleaning, transformation, and visualization.

## Key Findings

- Remote job listings receive more views on average than non-remote listings.
- Location appears to influence listing visibility, with some states attracting higher average views.
- Salary alone does not show a strong direct relationship with listing views.
- Certain job titles receive unusually high average views.
- Experience level has a weaker and less consistent relationship with view count.

## Repository Structure

```text
.
+-- job-listings-analysis.ipynb   # Main analysis notebook
+-- datasets/                     # Local CSV inputs, not committed
+-- requirements.txt              # Python dependencies
+-- .gitignore                    # Local files excluded from version control
+-- README.md                     # Project documentation
```

## Data

The notebook expects four CSV files in the `datasets` folder:

```text
datasets/postings1.csv
datasets/postings2.csv
datasets/postings3.csv
datasets/postings4.csv
```

These files are not included in the repository. Add them locally before running the notebook.

## Methods

The analysis follows these steps:

1. Load four job posting CSV files.
2. Select relevant columns from each dataset.
3. Merge the datasets using `job_id`.
4. Convert salary values into annual USD salary estimates.
5. Extract valid U.S. state codes from job locations.
6. Clean missing remote-work values.
7. Create visualizations to compare views across salary, location, remote status, job title, and experience level.

## Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd job-listings-analysis
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it:

```bash
# Windows
.venv\Scripts\activate

# macOS/Linux
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Add the data files

Place `postings1.csv`, `postings2.csv`, `postings3.csv`, and `postings4.csv` in the `datasets` folder.

### 5. Run the notebook

```bash
jupyter notebook job-listings-analysis.ipynb
```

## Dependencies

- Python 3.10+
- pandas
- numpy
- matplotlib
- jupyter

## Notes

- Currency conversion rates are hard-coded in the notebook for the purpose of analysis.
- The analysis removes extreme salary outliers above 500,000 for selected visualizations.
- The project is intended for exploratory analysis, not production prediction or causal inference.
