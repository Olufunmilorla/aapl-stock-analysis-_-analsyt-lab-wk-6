# aapl-stock-analysis-_-analsyt-lab-wk-6
Python analysis of 5 years of Apple (AAPL) stock data: data cleaning, time-series analysis, feature engineering, and visualization using Pandas, NumPy, Matplotlib, and Seaborn.

# Apple Inc. (AAPL) Historical Stock Market Analysis

Advanced Python analysis of 5 years of Apple Inc. (AAPL) daily stock data — covering data cleaning, transformation, time-series analysis, feature engineering, and visualization.

**Project:** Week 6 Internship Task — Advanced Python for Data Analysis
**Program:** AnalystLab Africa Internship, Batch B
**Author:** Olufunmilola Ogunmefun 

---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Tools & Libraries](#tools--libraries)
- [Project Workflow](#project-workflow)
- [Visualizations](#visualizations)
- [Key Findings](#key-findings)
- [Recommendations](#recommendations)
- [How to Run](#how-to-run)
- [Skills Demonstrated](#skills-demonstrated)

---

## Overview

This project analyzes the historical stock market performance of Apple Inc. (AAPL) using Python. The goal was to apply advanced data analysis techniques — data cleaning, transformation, time-series analysis, feature engineering, and visualization — to uncover meaningful patterns and trends in Apple's stock behavior over a 5-year period.

## Dataset

The dataset was sourced from Yahoo Finance via the `yfinance` library and contains Apple's historical daily stock market data, including:

| Column | Description |
|---|---|
| `Date` | Trading date |
| `Open` | Opening price |
| `High` | Highest intraday price |
| `Low` | Lowest intraday price |
| `Close` | Closing price |
| `Volume` | Shares traded |

**Size:** 1,254 daily trading records across a 5-year window.

## Tools & Libraries

- **Python** — core language
- **Pandas** — data cleaning, transformation, time-series operations
- **NumPy** — numerical operations
- **Matplotlib / Seaborn** — data visualization
- **Jupyter Notebook** — analysis environment

## Project Workflow

### 1. Data Exploration
Inspected dataset structure, data types, summary statistics, missing values, and duplicate records before any preprocessing.

### 2. Data Cleaning & Preprocessing
- Removed the multi-row ticker header from the raw `yfinance` export
- Converted `Date` to datetime and set it as the reference for all time-based operations
- Converted numeric columns to correct dtypes
- Removed duplicate records and sorted the dataset chronologically

### 3. Data Transformation
- Reordered columns into a clear, logical sequence
- Engineered a **Price Range** feature (`High − Low`) to capture intraday price movement

### 4. Time-Series Analysis
- Extracted `Year`, `Month`, `Quarter`, and `Day of week` from the date index
- Calculated monthly and yearly average closing prices via grouping and resampling
- Computed **daily returns** (% change in closing price)
- Calculated **7-day and 30-day moving averages** to separate trend from noise
- Calculated **30-day rolling volatility** to track periods of market uncertainty
- Computed **monthly returns** via month-end resampling

### 5. Feature Engineering
- **Daily Price Change** (`Close − Open`)
- **Percentage Change** (daily price change as a % of the opening price)

### 6. Data Visualization
Seven charts were built to support the analysis — see below.

## Visualizations

Seven charts were built in the notebook to support the analysis:

1. **Closing Price Trend** — Apple's 5-year price trajectory, showing a sustained long-term uptrend.
2. **Daily Trading Volume** — spikes often align with earnings or major market events.
3. **7-Day & 30-Day Moving Averages** — smooths short-term noise to reveal the underlying trend.
4. **Monthly Average Closing Price** — compares performance across months and years.
5. **Distribution of Daily Returns** — most daily moves are moderate; large swings are rare.
6. **30-Day Rolling Volatility** — highlights periods of elevated market uncertainty.
7. **Correlation Heatmap** — Open/High/Low/Close are tightly correlated; Volume is only weakly related to price.

All charts are available in the Jupyter notebook (`AAPL_Stock_Analysis_AnalystLab.ipynb`) in this repo.

## Key Findings

- AAPL's closing price followed an overall upward trend across the 5-year period, despite normal short-term fluctuations.
- Trading volume varied considerably, with visible spikes likely tied to earnings releases or major market events.
- The 7-day moving average tracked short-term price movement closely, while the 30-day average revealed the broader trend — together they help separate signal from noise.
- Monthly average closing prices confirmed sustained long-term growth.
- Daily returns were concentrated near zero; large single-day gains or losses were infrequent, consistent with typical large-cap equity behavior.
- Rolling volatility moved in cycles, alternating between calm stretches and periods of heightened uncertainty.
- Open, High, Low, and Close prices were strongly positively correlated with each other, while Trading Volume showed only a weak relationship with price levels.

## Recommendations

- Track short-term and long-term moving averages together rather than in isolation for a fuller read on trend direction.
- Read volume alongside price movement — unusual spikes often signal a significant event worth investigating.
- Monitor rolling volatility as an ongoing risk indicator.
- Extend this analysis with additional technical indicators (RSI, MACD, Bollinger Bands).
- Incorporate external context — earnings reports, interest rate changes, macroeconomic news — to explain moves the price data alone can't.
- Use the engineered features here (returns, moving averages, volatility) as a starting feature set for a future predictive model.

## How to Run

```bash
# Clone the repo
git clone https://github.com/<your-username>/aapl-stock-analysis.git
cd aapl-stock-analysis

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Launch the notebook
jupyter notebook AAPL_Stock_Analysis_AnalystLab.ipynb
```

## Skills Demonstrated

`Python` · `Pandas` · `NumPy` · `Data Cleaning` · `Data Transformation` · `Time-Series Analysis` · `Feature Engineering` · `Exploratory Data Analysis (EDA)` · `Data Visualization (Matplotlib, Seaborn)` · `Statistical Analysis` · `Financial Data Analysis`

---

*This project was completed as part of the AnalystLab Africa Data Analytics Internship, Batch B (June–August 2026).*
