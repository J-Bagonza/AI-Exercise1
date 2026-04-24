# Exercise 1: International Football Results Analysis (1872–2024)
BY BAGONZA OHM JOHN S13/07759/22
## Overview

This project explores over 150 years of international football match data sourced from Kaggle.  
The analysis covers basic data exploration, goals patterns, match outcomes, and historical team performance.

## Dataset

**Source:** [International Football Results from 1872 to 2024 – Kaggle](https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017)

Download `results.csv` from Kaggle and place it in the `data/` folder before running the notebook.

The dataset contains one row per match with the following key columns:

| Column | Description |
|---|---|
| `date` | Match date |
| `home_team` | Home country |
| `away_team` | Away country |
| `home_score` | Goals scored by home side |
| `away_score` | Goals scored by away side |
| `tournament` | Competition name |
| `city` | Host city |
| `country` | Host country |
| `neutral` | True if match was played at a neutral venue |

## Project Structure

```
exercise1_football_analysis/
│
├── data/
│   └── results.csv            # Download from Kaggle (not committed – see note below)
│
├── notebooks/
│   └── football_analysis.ipynb
│
└── README.md
```

## How to Run

1. Clone this repository.
2. Create a virtual environment and install dependencies:
   pip install -r requirements.txt
   
3. Download `results.csv` from Kaggle and place it in `data/`.
4. Open the notebook:
   jupyter notebook notebooks/football_analysis.ipynb

5. Run all cells top to bottom (`Kernel > Restart & Run All`).

## Analysis Sections

### Part 1 – Basic Exploration
- Total match count, date range, number of unique countries.
- Identifying the team that appears most frequently as home side.

### Part 2 – Goals Analysis
- Average goals per match.
- Highest-scoring match in the dataset.
- Comparison of total home vs away goals.
- Most common combined goal total.

### Part 3 – Match Results
- Labelling each match as Home Win, Away Win, or Draw.
- Percentage breakdown of each outcome.
- Discussion of whether home advantage exists.
- Ranking countries by all-time wins.

### Part 4 – Visualizations
- Histogram of total goals per match.
- Bar chart of match outcome distribution.
- Horizontal bar chart of the top 10 teams by total wins.

All three charts are saved as PNG files in the `data/` folder when the notebook runs.

## Key Findings

- **Home advantage is real and persistent.** Home teams win roughly 46% of all matches – significantly more than away wins (~30%) or draws (~24%). This pattern holds consistently across the entire 150-year history of the dataset.
- **Low-scoring matches dominate.** The most common total goals in a match is 2, and the distribution is heavily right-skewed.
- **Brazil leads the all-time wins table**, followed closely by England and Germany.
- The dataset spans **300+ unique national teams**, many of which are short-lived states or territories that no longer exist as independent football nations.

## Notes on the Data

- The dataset covers official international matches as well as friendlies. Tournament context matters when interpreting results.
- Some very early matches (pre-1900) may have inconsistencies because record-keeping standards varied widely.
- The `neutral` flag is important for home advantage analysis – neutral venue matches should arguably be excluded from that calculation.
