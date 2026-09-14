# DATA VORTEX — Round 1

## Recover → Clean → Analyze → Query

This repository contains our solution and reproducible workflow for **DATA VORTEX — Round 1**.

The project focuses on recovering the hidden dataset, performing data cleaning and preprocessing, conducting exploratory data analysis (EDA), extracting meaningful insights, and preparing the cleaned dataset for the SQL-based analytical phase.

---

##  Competition Overview

**Competition:** DATA VORTEX
**Round:** Round 1
**Phase 1:** Dataset Recovery, Cleaning & Analysis
**Phase 2:** SQL-Based Analytical Challenges

### Phase 1 Deadline

**14 September 2026 — 11:59 PM**

### Phase 2 Deadline

**15 September 2026 — 11:59 PM**

---

#  Project Objectives

The objectives of this project are to:

1. Recover the dataset from the DATA VORTEX Social Engine.
2. Preserve the original recovered dataset without modification.
3. Inspect and understand the structure and quality of the data.
4. Identify missing, duplicate, inconsistent, invalid, and anomalous records.
5. Apply justified data-cleaning and preprocessing techniques.
6. Validate the cleaned dataset.
7. Perform exploratory data analysis.
8. Identify meaningful patterns and insights from the data.
9. Export the cleaned dataset for downstream analysis.
10. Prepare the cleaned dataset for Phase 2 SQL analysis.

---

#  Dataset Recovery

The dataset for Round 1 is not treated as a conventional directly supplied dataset.

It is recovered through the **DATA VORTEX Social Engine**:

**DATA VORTEX Social Engine:**
https://datavortex-social-engine.vercel.app/

The recovery process involves examining the available recovery information and identifying the relevant pattern/connection required to locate the dataset.

### Recovery Approach

The recovery process followed these general steps:

1. Access the DATA VORTEX Social Engine.
2. Examine the recovery logs and available information.
3. Inspect the beginning of log lines and other visible patterns.
4. Identify the relevant clue/pattern.
5. Follow the discovered connection to locate the dataset.
6. Download/recover the dataset.
7. Preserve the recovered dataset as the original raw input.
8. Perform all subsequent processing programmatically.

> **Note:** The exact recovery clue and recovered location will be documented here after the dataset recovery process is completed.

---

#  Repository Structure

```text
data-vortex-round-1/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   └── README.md
│   │
│   └── processed/
│       └── README.md
│
├── notebooks/
│   └── 01_data_recovery_cleaning_eda.ipynb
│
├── src/
│   ├── __init__.py
│   └── data_cleaning.py
│
├── reports/
│   └── README.md
│
├── sql/
│   └── README.md
│
├── requirements.txt
│
└── .gitignore
```

---

#  Dataset

## Raw Dataset

The original recovered dataset is stored in:

```text
data/raw/
```

The raw dataset is preserved in its original form and is not modified during the cleaning process.

**Raw dataset filename:** `[TO BE FILLED]`

**Original format:** `[CSV / JSON / OTHER]`

**Original number of rows:** `[TO BE FILLED]`

**Original number of columns:** `[TO BE FILLED]`

---

## Cleaned Dataset

The cleaned dataset is stored in:

```text
data/processed/
```

**Cleaned dataset filename:** `[TO BE FILLED]`

**Cleaned number of rows:** `[TO BE FILLED]`

**Cleaned number of columns:** `[TO BE FILLED]`

The cleaned dataset is generated through the documented preprocessing pipeline rather than through manual modification.

---

#  Initial Data Inspection

The initial inspection covers:

* Dataset dimensions
* Column names
* Data types
* Missing values
* Duplicate records
* Unique values
* Categorical distributions
* Numerical statistics
* Date/time fields
* Potentially invalid values
* Potential anomalies and outliers

The detailed inspection is available in:

```text
notebooks/01_data_recovery_cleaning_eda.ipynb
```

---

#  Data Cleaning & Preprocessing

The cleaning process is performed systematically and each major transformation is documented.

The planned workflow is:

```text
Raw Dataset
     │
     ▼
Initial Inspection
     │
     ▼
Data Quality Assessment
     │
     ├── Missing Values
     ├── Duplicate Records
     ├── Invalid Values
     ├── Data Types
     ├── Inconsistent Categories
     └── Anomalies / Outliers
     │
     ▼
Cleaning & Standardisation
     │
     ▼
Validation
     │
     ▼
Clean Dataset
     │
     ▼
Exploratory Data Analysis
```

## Cleaning Operations

The final cleaning operations will be documented below after the dataset has been inspected.

| Issue       | Treatment     | Reason     |
| ----------- | ------------- | ---------- |
| `[Issue 1]` | `[Treatment]` | `[Reason]` |
| `[Issue 2]` | `[Treatment]` | `[Reason]` |
| `[Issue 3]` | `[Treatment]` | `[Reason]` |

No data transformation will be applied without an identifiable reason.

---

#  Data Validation

After cleaning, the dataset is validated to ensure that the transformations have not introduced new inconsistencies.

Validation includes:

* Row-count comparison
* Column validation
* Data-type validation
* Missing-value verification
* Duplicate verification
* Range checks
* Category consistency
* Date/time validation
* Key/identifier validation where applicable

The final validation results will be documented in the notebook.

---

#  Exploratory Data Analysis

The EDA is designed to understand the structure, distributions, relationships and patterns present in the cleaned dataset.

## EDA Areas

The analysis may include:

### 1. Univariate Analysis

Analysis of individual variables using:

* Frequency distributions
* Histograms
* Bar charts
* Summary statistics
* Box plots

### 2. Bivariate Analysis

Analysis of relationships between variables using:

* Scatter plots
* Grouped comparisons
* Aggregations
* Correlation analysis

### 3. Time-Based Analysis

Where applicable:

* Trends over time
* Daily/weekly/monthly patterns
* Changes in engagement/activity
* Period-based comparisons

### 4. Categorical Analysis

Where applicable:

* Category frequencies
* Category-wise performance
* Platform/content comparisons
* Behavioural differences between groups

### 5. Outlier Analysis

Potentially unusual observations will be investigated using appropriate statistical and contextual methods.

---

#  Key Insights

The final insights will be added after completing the EDA.

### Insight 1

`[TO BE FILLED AFTER EDA]`

### Insight 2

`[TO BE FILLED AFTER EDA]`

### Insight 3

`[TO BE FILLED AFTER EDA]`

### Insight 4

`[TO BE FILLED AFTER EDA]`

### Insight 5

`[TO BE FILLED AFTER EDA]`

Each insight will be supported by the underlying data and relevant visualisation or statistical analysis.

---

#  Technologies Used

The project uses Python-based data analysis tools.

Planned technologies include:

* **Python**
* **Pandas** — data manipulation and preprocessing
* **NumPy** — numerical operations
* **Matplotlib** — data visualisation
* **Seaborn** — statistical visualisation
* **Jupyter Notebook** — analysis and documentation
* **Git & GitHub** — version control and submission

Phase 2 will additionally use:

* **SQL**
* SQL-compatible database environment

The exact database system used for Phase 2 will be documented separately.

---

#  Installation

Clone the repository:

```bash
git clone https://github.com/[YOUR-USERNAME]/data-vortex-round-1.git
```

Move into the project directory:

```bash
cd data-vortex-round-1
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Activate it on macOS/Linux:

```bash
source venv/bin/activate
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---

#  Running the Analysis

Open the Jupyter notebook:

```bash
jupyter notebook
```

Then open:

```text
notebooks/01_data_recovery_cleaning_eda.ipynb
```

Run the notebook sequentially from the beginning.

The notebook is designed so that the major data-processing steps can be reproduced rather than relying on manually edited outputs.

---

#  Notebook Contents

The main notebook follows this structure:

```text
01. Project Introduction
02. Dataset Recovery
03. Dataset Loading
04. Initial Data Inspection
05. Data Quality Assessment
06. Missing Value Analysis
07. Duplicate Analysis
08. Data Type Validation
09. Invalid Value Detection
10. Data Standardisation
11. Outlier / Anomaly Analysis
12. Data Cleaning
13. Cleaning Validation
14. Exploratory Data Analysis
15. Key Findings
16. Export Clean Dataset
```

---

#  Data Provenance

The project maintains a separation between the original recovered data and processed data.

```text
Original / Recovered Data
        │
        ▼
   data/raw/
        │
        ▼
Cleaning & Preprocessing
        │
        ▼
 data/processed/
```

The raw dataset is retained as the reference input, while the processed dataset represents the output of the documented cleaning pipeline.

---

#  Reproducibility

To maintain reproducibility:

* Raw data is preserved separately from processed data.
* Cleaning operations are documented.
* Processing is performed programmatically wherever possible.
* Assumptions are explicitly recorded.
* The analysis notebook contains the major analytical steps.
* Required Python dependencies are listed in `requirements.txt`.
* Generated outputs are based on the documented workflow.

---

#  Phase 1 Deliverables

The repository is intended to contain the required Phase 1 work, including:

### 1. Cleaned Dataset

Located in:

```text
data/processed/
```

### 2. EDA / Analysis

Located in:

```text
notebooks/
```

and, where applicable:

```text
reports/
```

### 3. Source Code

Located in:

```text
src/
```

### 4. Documentation

Available through:

```text
README.md
```

---

#  Phase 2 — SQL Analysis

Phase 2 uses the cleaned dataset produced during Phase 1.

The Phase 2 workflow will be:

```text
Cleaned Dataset
      │
      ▼
SQL Database
      │
      ▼
Table Design
      │
      ▼
Analytical Queries
      │
      ├── Trend Detection
      ├── Anomaly Discovery
      ├── Behavioural Grouping
      └── Correlation Analysis
      │
      ▼
Results & Insights
```

Phase 2 SQL queries will be maintained in:

```text
sql/
```

The database schema, queries, outputs and explanations will be documented separately once Phase 2 begins.

---

#  Assumptions & Decisions

Important assumptions made during the analysis will be recorded here.

| # | Assumption / Decision | Reason     |
| - | --------------------- | ---------- |
| 1 | `[TO BE FILLED]`      | `[Reason]` |
| 2 | `[TO BE FILLED]`      | `[Reason]` |
| 3 | `[TO BE FILLED]`      | `[Reason]` |

This section will be updated as the data-quality investigation progresses.

---

#  Data Integrity

The analysis follows these principles:

* No fabricated records
* No fabricated analytical outputs
* No hardcoded query results
* No unexplained data transformations
* No intentional manipulation of results
* Original recovered data is preserved
* Analytical conclusions are based on the available dataset

---

#  Team

| Name     | Role     |
| -------- | -------- |
| `[NAME]` | `[ROLE]` |
| `[NAME]` | `[ROLE]` |
| `[NAME]` | `[ROLE]` |

---

#  Project Status

### Phase 1

* [ ] Dataset recovered
* [ ] Raw dataset preserved
* [ ] Initial inspection completed
* [ ] Data-quality assessment completed
* [ ] Cleaning completed
* [ ] Validation completed
* [ ] EDA completed
* [ ] Insights identified
* [ ] Cleaned dataset exported
* [ ] EDA report completed
* [ ] GitHub repository finalised

### Phase 2

* [ ] SQL database created
* [ ] Schema designed
* [ ] Cleaned data imported
* [ ] Analytical queries completed
* [ ] Query outputs validated
* [ ] SQL insights documented
* [ ] Phase 2 report completed

---

#  Competition Compliance

This repository is prepared according to the DATA VORTEX Round 1 requirements.

The analysis is intended to remain reproducible, transparent and based on the recovered dataset and documented transformations.

All assumptions, cleaning decisions and analytical conclusions will be documented as part of the project workflow.

---

#  Final Outcome

The final project aims to provide a complete analytical pipeline:

```text
RECOVER
   ↓
UNDERSTAND
   ↓
CLEAN
   ↓
VALIDATE
   ↓
ANALYZE
   ↓
EXTRACT INSIGHTS
   ↓
LOAD INTO SQL
   ↓
QUERY
   ↓
DISCOVER PATTERNS
```

**DATA VORTEX — Round 1**

> Recover the data. Clean it carefully. Find the patterns. Explain the evidence.
