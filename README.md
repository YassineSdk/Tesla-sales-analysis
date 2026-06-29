# 🚗 Tesla Sales Analysis and Performance


A concise exploratory data analysis of Tesla sales and profitability (price, gross profit) with time-series and categorical breakdowns. The analysis is implemented in a Jupyter Notebook and uses a provided Excel dataset.

---

## What you'll find here

- Tesla_Sales_Performance.ipynb — the interactive Jupyter Notebook containing the whole analysis, visualizations, and commentary.  
- Tesla sales data.xlsx — the raw dataset used by the notebook.  
- Tesla_Sales_Performance.pdf — an exported PDF of the notebook for quick viewing.

---

## Highlights

- Key fields in the dataset: Model, Period (YYYYMM), Country, Purchase type, Version, Price, Gross Profit.
- Period is converted to a datetime and a `year` column is extracted.  
- New metrics added: `Profitability Ratio = Gross Profit / Price` and `Cost Ratio = 1 - Profitability Ratio`.
- Visual analyses included:
  - Frequency counts for categorical features (Model, Country, Purchase type, Version).  
  - Time series of aggregated Sales (Price) and Gross Profit (total by date).  
  - Yearly slices (2016, 2017) and per-model (Model S, Model X) breakdowns.  
  - Aggregated performance by `Version` with total sales, total profit, volume sold and average profitability.

---

## Requirements

Uses standard data-science Python packages. To run locally, create a virtual environment and install:

```bash
python -m venv .venv
source .venv/bin/activate  # or .\.venv\Scripts\activate on Windows
pip install --upgrade pip
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

(If you want to export notebooks to PDF or render markdown inside, install `nbconvert` and supporting dependencies.)

---

## How to run

1. Clone the repository:

```bash
git clone https://github.com/YassineSdk/Tesla-sales-analysis.git
cd Tesla-sales-analysis
```

2. Open and run the notebook with Jupyter Lab / Notebook:

```bash
jupyter notebook Tesla_Sales_Performance.ipynb
# or
jupyter lab
```

3. The notebook reads `Tesla sales data.xlsx` from the repository root — ensure that file remains in place.

Quick non-interactive export (re-run and save output to HTML/PDF):

```bash
jupyter nbconvert --to html "Tesla_Sales_Performance.ipynb"
jupyter nbconvert --to pdf "Tesla_Sales_Performance.ipynb"  # may require extra dependencies
```

---

## Files & structure

```
Tesla_Sales_Performance.ipynb   # Main notebook with analysis and plots
Tesla sales data.xlsx           # Raw data used by the notebook
Tesla_Sales_Performance.pdf     # Notebook exported to PDF
```

How it fits together: the notebook loads the Excel file, performs light feature engineering (date/year + profitability/cost ratios), and generates aggregated tables and plots (time series, bar charts) that summarize sales and profitability by model, country, purchase type and version.




---

## Contact

Created by @YassineSdk — see the GitHub repository for more.
