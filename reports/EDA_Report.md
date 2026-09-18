# Exploratory Data Analysis Report — Social Engine Users

## 1. Overview

| | |
|---|---|
| **Dataset** | `Social_Engine_Users_cleaned.csv` |
| **Rows (final)** | 1,474 users |
| **Columns** | 5 (`user_id`, `location`, `language`, `account_created`, `follower_count`) |
| **Time period** | Jan 2023 – Dec 2023 |
| **Source** | Raw export (`Social_Engine_Users_raw.csv`), cleaned in `notebooks/data_cleaning_eda.ipynb` |

This report summarizes the cleaned Social Engine Users dataset: data quality, distributions,
geographic and language composition, growth trends, and relationships between fields. See the
companion notebook for the full, step-by-step cleaning process and the assumptions behind it.

---

## 2. Data Quality Summary (Raw → Cleaned)

| Issue | Raw dataset | Action taken | Rows affected |
|---|---|---|---|
| Exact duplicate rows | 9 | Dropped | 9 |
| Duplicate `user_id` (conflicting data) | 47 | Kept first occurrence | 47 |
| Missing `location` | 30 | Dropped (couldn't be reliably imputed) | 30 |
| Missing `language` | 30 | Imputed with mode (`zh`) | 30 |
| Missing `follower_count` | 45 | Imputed with median | 45 |
| Negative `follower_count` | 22 | Corrected via absolute value | 22 |
| High-end outliers (IQR) | 11 | Capped at upper fence (~73,522) | 11 |
| Inconsistent casing/whitespace | ~8% of rows | Standardized (Title Case / lowercase) | — |
| Mixed date formats | ~45% of rows | Parsed to ISO 8601 | — |
| **Net result** | **1,560 raw rows** | | **→ 1,474 cleaned rows** |

Full reasoning for each decision is documented inline in the notebook.

---

## 3. Follower Count Distribution

![Follower count distribution](figures/01_follower_distribution.png)

- Follower counts range roughly from **~100 to ~73,500** (post-capping), with a **median around
  25,000**.
- The distribution is **right-skewed** (skewness ≈ 0.22) — a long tail of higher-follower
  accounts pulls the mean slightly above the median, but the skew is mild, not extreme.
- No sharp spikes or artificial clustering — consistent with organically distributed follower
  counts once outliers were capped.

---

## 4. Follower Count by Language

![Follower count by language](figures/02_followers_by_language.png)

- Median follower counts are **broadly comparable across all 10 languages** — no single
  language group dominates in typical account reach.
- Spread (IQR) is similar across groups, suggesting language is **not a strong driver** of
  follower count on its own.

---

## 5. Geographic Composition

![Top 15 countries by user count](figures/03_top_countries.png)

- **USA** leads with the largest user base, followed by **China, Germany, Brazil, and Japan**.
- The user base spans **19 countries** across 33 city/country pairs — a globally distributed
  audience rather than one concentrated in a single region.
- The top 5 countries account for roughly **40%** of all users; the remaining 60% is spread
  across 14 other countries, indicating a reasonably long geographic tail.

![Average follower count by top 10 countries](figures/06_avg_followers_by_country.png)

- Average follower count across the top 10 countries by volume is fairly even, with no country
  showing a dramatically higher or lower average — reach looks geography-agnostic in this
  sample.

---

## 6. Language Composition

![User count by language](figures/04_language_distribution.png)

- **Chinese (`zh`)** is the most common language (194 users), followed by **Japanese (`ja`)**
  and **Hindi (`hi`)**.
- All 10 languages are represented with between ~130–195 users each — a relatively even split,
  not dominated by any single language.

---

## 7. Account Growth Over Time

![Signups per month](figures/05_signups_over_time.png)

- New account signups fluctuate between **~103 and ~141 per month** across 2023, with **no
  strong overall upward or downward trend** — growth looks roughly steady month to month.
- **December 2023** had the highest signup volume; **July 2023** the lowest — differences are
  modest (±15% around the monthly average) and don't suggest a clear seasonal pattern on their
  own from a single year of data.

---

## 8. Key Takeaways

1. **User base is global and language-diverse** — no single country or language dominates,
   which suggests the platform has broad international reach rather than a regional
   concentration.
2. **Follower counts are moderately right-skewed** but not driven by language or, on average,
   by country — engagement/reach appears to vary at the individual level more than by these
   demographic splits.
3. **Signup volume is roughly stable** across 2023 with no major growth or decline trend
   visible in this single year of data.
4. **Data quality issues in the raw export were moderate but material** (~5.5% of rows had at
   least one issue) — casing/whitespace inconsistency and mixed date formats were the most
   common problems, alongside a smaller number of missing values, invalid/negative follower
   counts, and duplicate records.

---

## 9. Suggested Next Steps

- Extend the observation window beyond a single year to test for genuine seasonality or growth
  trends in signups.
- Bring in an engagement metric (posts, likes, sessions) to see whether follower count
  correlates with actual activity, not just account age or geography.
- If raw exports continue to arrive with mixed date formats and casing inconsistencies,
  address this at the source/ETL layer rather than downstream, to reduce repeated cleaning
  overhead.

---

*Generated as part of the Social Engine Users project. See `notebooks/data_cleaning_eda.ipynb`
for the full cleaning methodology and `data/` for the raw and cleaned datasets.*
