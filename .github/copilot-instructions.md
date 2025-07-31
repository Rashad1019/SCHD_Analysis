# Copilot Instructions for SCHD Risk Analysis Dashboard

## Project Overview
- This project analyzes the Schwab U.S. Dividend Equity ETF (SCHD) to advise on building a well-balanced mutual fund investment portfolio.
- The workflow is strictly sequential: **do not advance to the next task or sub-task until explicitly instructed**.
- All code and analysis are performed in a Jupyter Notebook (`SCHD1.ipynb`) in VS Code on Windows.

## Architecture & Data Flow
- **Data Source:** Historical SCHD prices are obtained using `yfinance` and saved as `schd_data_2015-07-12_to_2025-07-12.csv`.
- **Analysis Steps:**
  1. Data cleaning and validation (handle missing values).
  2. Core risk metrics calculation: returns, volatility, Sharpe Ratio, Beta, Alpha, correlation.
  3. Dashboard visualization: performance charts, risk assessment summary, investment suitability.
  4. Future value projections: Monte Carlo simulation, scenario analysis.
- **Notebook Cell Numbering:** All scripts must be labeled with a sequential cell number (e.g., `#Cell 1`, `#Cell 2`).

## Developer Workflow
- **Notebook-first:** All code, analysis, and output are managed in `SCHD1.ipynb`. Do not create standalone scripts unless instructed.
- **Windows/VS Code:** All code must be compatible with Windows and VS Code Jupyter environment.
- **Data File Location:** All files are in `C:\Users\rasha_ejuf17z\Downloads\0Today\SCHD`.
- **Tasklist:** Follow `tasklist.md` for step-by-step progress and cell mapping.
- **PRD Reference:** Use `Project Requirements Document (PRD).md` for project goals, constraints, and analytics techniques.

## Project-Specific Conventions
- **Strict Task Order:** Never skip or reorder tasks. Wait for explicit instruction before advancing.
- **Communication:** Ask for clarification if anything is unclear. Do not assume or guess requirements.
- **Cell Labeling:** Every code cell must start with a comment indicating its cell number.
- **Metrics & Recommendations:** Use risk metrics (Sharpe, Beta, Alpha, volatility) to generate investment insights and recommendations.
- **Visualization:** Performance and risk visualizations are required in later steps.

## Integration & Dependencies
- **External Libraries:** Use `yfinance`, `pandas`, `numpy`, and standard Python data science libraries.
- **No clustering/segmentation:** Only analyze SCHD, not multiple assets.
- **Benchmark:** Use SPY (S&P 500 ETF) for Beta and correlation calculations.

## Example Patterns
- Data cleaning and saving:
  ```python
  #Cell 1
  schd_adj_close.to_csv('schd_data_2015-07-12_to_2025-07-12.csv')
  ```
- Risk metrics calculation:
  ```python
  #Cell 4
  daily_volatility = schd_returns.std()
  sharpe_ratio = (annual_return - risk_free_rate) / annualized_volatility
  ```
- Investment recommendation logic:
  ```python
  #Cell 5
  if sharpe_ratio > 1.0:
      print("Superior risk-adjusted returns")
  ```

## Key Files
- `SCHD1.ipynb`: Main analysis notebook
- `schd_data_2015-07-12_to_2025-07-12.csv`: Data file
- `tasklist.md`: Task progress and cell mapping
- `Project Requirements Document (PRD).md`: Project goals and constraints

---
**If any section is unclear or missing, please provide feedback so this guide can be improved.**
