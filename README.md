# Nifty50 Analysis — Python + Power BI

**One-line:** A small project to fetch, process, and analyze Nifty 50 stock data using a Python script and visualize the results in Power BI.

---

## 📊 Project Overview

This repository automates the process of downloading Nifty 50 historical stock data from Yahoo Finance using **Python**, cleans and structures it into a tidy dataset, and then uses **Power BI** to visualize performance insights.

**Key highlights:**

* Fetches daily data for all Nifty 50 stocks (2020–2025)
* Cleans and merges into a single CSV (`nifty50_tidy.csv`)
* Builds Power BI dashboards showing:

  * Top 5, bottom 5, Top consistent performing stocks
  * Risk vs return comparison
  * Consistency and volatility analysis
  * Average market return and total stocks analyzed

---

## 🧠 Files in This Repo

```
README.md                # Project documentation
nse_data_collection.ipynb     # Python script (Colab-compatible)
stock_analysis_from_2020_using_powerbi.pbix   # Power BI report file
```

---

## ⚙️ Requirements

* Python 3.8+
* Libraries: `pandas`, `yfinance`, `google.colab`
* Power BI Desktop (to view `.pbix` file)

Install required libraries:

```bash
pip install pandas yfinance
```

> If running locally (not in Colab), remove `google.colab.files` lines and use normal CSV export.

---

## 🚀 How It Works

### 1. **Download Nifty 50 Data (Python)**

Run the script in **Google Colab** or any Python environment.

It will:

* Download data for all Nifty 50 tickers from Yahoo Finance
* Combine all tickers into one dataset
* Save as `nifty50_tidy.csv`
* Automatically download the CSV (in Colab)

### Example Output (first few rows):

| Date       | Symbol      | Open   | High   | Low    | Close  | Volume  |
| ---------- | ----------- | ------ | ------ | ------ | ------ | ------- |
| 2020-01-01 | RELIANCE.NS | 1500.0 | 1520.0 | 1490.0 | 1510.0 | 1234567 |

---

### 2. **Power BI Dashboard**

* Open `nifty50_dashboard.pbix` in Power BI Desktop.
* Update the CSV path to where your `nifty50_tidy.csv` is saved.
* Click **Refresh** to load the latest data.

**Visuals include:**

* KPI cards: Total stocks analyzed, average return, best performer
* Bar charts: Top 5 and bottom 5 performers
* Scatter plots: Risk vs Return, Consistency vs Volatility
* Consistency score charts

---

## 📈 Insights Example

From the sample dashboard:

* **Best performer:** `WIPRO.NS`
* **Average market return:** 1.90%
* **Top consistent stocks:** ITC, TCS, HDFCBANK, RELIANCE, INFY
* **Top losers:** HINDUNILVR, KOTAKBANK, INDUSINDBK

---

## 🗂️ Folder Suggestion (Optional)

If you expand the project later:

```
README.md
/data/nifty50_tidy.csv
/src/nifty50_analysis.py
/reports/nifty50_dashboard.pbix
/images/dashboard_screens.png
```

---

## 🧰 Troubleshooting

* **No data for some tickers:** Yahoo Finance sometimes skips tickers; the script already handles this.
* **Blank visuals in Power BI:** Ensure the CSV path and field names match.
* **Slow downloads:** yfinance batching may lag; try smaller ticker lists.

---

## 🪪 License

You may include an MIT license or similar.

---

## 💬 Author

Created by **Deepesh Sreecharan** — Data & Visualization Enthusiast.

For any suggestions or improvements, feel free to open an issue or pull request!
