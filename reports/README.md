# Social Engine Users — Data Cleaning & EDA

A small data-cleaning and exploratory-analysis project on a Social Engine platform's user
export: 1,500+ users across location, language, account-creation date, and follower count.

## Project Structure

```
project/
├── data/
│   ├── Social_Engine_Users_raw.csv        # Raw, uncleaned export
│   └── Social_Engine_Users_cleaned.csv    # Cleaned output (produced by the notebook)
├── notebooks/
│   └── data_cleaning_eda.ipynb            # Step-by-step cleaning process + assumptions
├── reports/
│   ├── EDA_Report.md                      # Full exploratory data analysis write-up
│   └── figures/                           # Charts referenced in the EDA report
└── README.md
```

## How to Reproduce

1. Open `notebooks/data_cleaning_eda.ipynb`.
2. Run all cells top to bottom. It reads `data/Social_Engine_Users_raw.csv`, applies each
   cleaning step (with the reasoning documented in markdown cells above the code), and writes
   the result to `data/Social_Engine_Users_cleaned.csv`.
3. See `reports/EDA_Report.md` for the analysis built on top of the cleaned dataset.

## Data Cleaning Issues Addressed

- Exact duplicate rows
- Duplicate `user_id`s with conflicting field values
- Missing values in `location`, `language`, `follower_count`
- Inconsistent casing and whitespace in text fields
- Malformed language codes
- Mixed date formats in `account_created`
- Invalid (non-numeric) and negative `follower_count` values
- High-end outliers in `follower_count`

Each fix is paired with an explicit **assumption** in the notebook explaining why that
approach (drop / impute / correct / cap) was chosen over the alternatives.

## Key Findings (see full report for details)

- The user base spans 19 countries and 10 languages with no single group dominating.
- Follower counts are moderately right-skewed (median ≈ 25,000) but not strongly driven by
  language or country.
- Monthly signups were roughly stable through 2023, with no strong trend.
