# Bitcoin-Historical-Data-Analysis-2014-2026-
Bitcoin Historical Data Analysis (2014–2026)
A comprehensive exploratory data analysis of Bitcoin's price history from September 2014 to June 2026, covering over 4,200 trading days. This project applies core data analysis techniques — cleaning, feature engineering, trend analysis, volatility modelling, and visualisation — to one of the most volatile financial assets in history.
Author: Levi Sadoh  
Tools: Python, Pandas, NumPy, Matplotlib  
Dataset: kaggle
Environment: Google Colab
---
Project Structure
```
bitcoin-analysis/
│
├── data/
│   └── bitcoin_dataset.csv          # Raw OHLCV daily data
│
├── bitcoin_analysis.ipynb           # Main Colab notebook (Steps 1–7)
│
├── visuals/
│   └── bitcoin_summary_dashboard.png  # Summary dashboard (Step 7)
│
├── README.md
└── requirements.txt
```
---
Objectives
Understand the long-term price behaviour of Bitcoin through exploratory analysis
Engineer meaningful financial features from raw OHLCV data
Identify patterns in volatility, seasonality, and market cycles
Quantify key milestones: best/worst days, annual returns, and drawdowns
Present findings through clear, publication-ready visualisations
---
Methodology
The analysis is structured across seven steps:
Step	Focus
1	Data loading, type conversion, and cleaning
2	Exploratory analysis — price and volume over time
3	Feature engineering — daily returns, log returns, daily range
4	Trend analysis — yearly and monthly groupby aggregations
5	Market cycle annotation — crash and peak events
6	Volatility — rolling averages, rolling standard deviation, volume correlation
7	Summary statistics and key findings
---
Key Findings
Price Performance
Starting price (Sep 17, 2014): $457.33
Latest price (Jun 2026): ~$74,000
All-time high: $126,198 — reached on October 6, 2025
All-time low: $171.51 — recorded on January 14, 2015
Total return over the full period: +13,221%
Time to Multiply
Multiple	Target Price	Date Reached	Time Taken
10x	$4,573	August 29, 2017	2.9 years
100x	$45,733	February 8, 2021	6.4 years
200x	$91,467	November 19, 2024	10.2 years
Best & Worst Single Days
	Date	Return	Closing Price
📈 Best Day	December 7, 2017	+25.4%	$17,899
📉 Worst Day	March 12, 2020	–37.2%	$4,970
The worst single day coincides with the global COVID-19 market crash, when Bitcoin dropped alongside traditional equities before staging one of its strongest recoveries on record.
Annual Returns
Year	Annual Return
2014	–31.27%
2015	+34.37%
2016	+123.75%
2017	+1,369.03% ← Best year
2018	–73.48% ← Worst year
2019	+92.00%
2020	+303.09%
2021	+59.71%
2022	–64.27%
2023	+155.41%
2024	+120.98%
2025	–6.33%
2017 stands out as Bitcoin's most extraordinary year  a 13x return driven by retail speculation and the initial coin offering (ICO) boom. The following year saw an equally dramatic reversal.
Drawdowns
The single largest drawdown in this dataset occurred on December 15, 2018, when Bitcoin had fallen –83.4% from its then-all-time high of approximately $19,500 set in late 2017. The 2022 bear market produced a second major drawdown of over 77%, driven by the collapse of the Terra/LUNA ecosystem and the FTX exchange.
Volatility & Volume
Bitcoin closed higher than it opened on 52.4% of trading days only marginally above random, highlighting how difficult short-term prediction is
The correlation between trading volume and directional price movement is 0.027 essentially zero meaning high-volume days do not reliably predict whether the price will rise or fall
The 30-day rolling volatility peaks sharply during crash events (2018, 2020, 2022), confirming that volatility is mean-reverting but fat-tailed in Bitcoin markets
---
Visualisations
The notebook produces the following charts:
Bitcoin Closing Price Over Time — full price history from 2014 to 2026
Trading Volume Over Time — daily volume with structural growth visible post-2020
Price with Annotated Market Events — crashes (2018, 2022) and peaks (2021, 2024) highlighted
Moving Averages (7-day & 30-day) — trend smoothing overlaid on close price
Price & Volume Combined Chart — dual-axis layout with volume bars beneath price

---
How to Run
Option 1 — Google Colab (recommended):  
Open `bitcoin_analysis.ipynb` directly in Google Colab and run all cells in order. Upload `bitcoin_dataset.csv` when prompted.
Option 2 — Local environment:
```bash
git clone https://github.com/YOUR_USERNAME/bitcoin-analysis.git
cd bitcoin-analysis
pip install -r requirements.txt
jupyter notebook bitcoin_analysis.ipynb
```
---
Requirements
```
pandas
numpy
matplotlib
jupyter
```
---
Data Source
Daily OHLCV (Open, High, Low, Close, Volume) data sourced from kaggle . The dataset spans September 17, 2014 to June 5, 2026 and contains 4,280 records with no missing values.
---
Limitations
This analysis is purely descriptive and retrospective — no predictive modelling is applied
Past performance of Bitcoin is not indicative of future results
The dataset does not account for exchange-specific pricing differences or on-chain metrics
---
Author
Levi Sadoh  
Data Analyst  
GitHub · LinkedIn
---
This project was completed as a personal portfolio piece to demonstrate applied data analysis on real-world financial time series data.
