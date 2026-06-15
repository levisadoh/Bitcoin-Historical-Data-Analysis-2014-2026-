Bitcoin Historical Data Analysis (2014–2026)

A comprehensive exploratory data analysis of Bitcoin's price history from September 2014 to June 2026, covering over 4,200 trading days. This project applies core data analysis techniques — cleaning, feature engineering, trend analysis, volatility modelling, and visualisation — to one of the most volatile financial assets in history.

Author: Levi Sadoh

Tools: Python, Pandas, NumPy, Matplotlib

Dataset: Kaggle

Environment: Google Colab


Project Structure

bitcoin-analysis

──data─ bitcoin_dataset.csv

──bitcoin_analysis.ipynb

──visuals ─ price_over_time.png, volume_over_time.png,high_and_low.png, 7 days_and_30_days_moving_average.png,price_and_volume_analysis.png


──README.md


──requirements.txt


Objectives


Understand the long-term price behaviour of Bitcoin through exploratory analysis
Engineer meaningful financial features from raw OHLCV data
Identify patterns in volatility, seasonality, and market cycles
Quantify key milestones: best/worst days, annual returns, and drawdowns
Present findings through clear, publication-ready visualisations



Methodology

The analysis is structured across seven steps:

StepFocus1Data loading, type conversion, and cleaning2Exploratory analysis — price and volume over time3Feature engineering — daily returns, log returns, daily range4Trend analysis — yearly and monthly groupby aggregations5Market cycle annotation — crash and peak events6Volatility — rolling averages, rolling standard deviation, volume correlation7Summary statistics and key findings


Visualisations & Analysis

1. Bitcoin Close Price Over Time

<img width="615" height="455" alt="image" src="https://github.com/user-attachments/assets/05aaf5e2-4a30-4e6f-b1f5-6542b0b9d94b" />


This is the foundational chart of the entire analysis. It plots Bitcoin's daily closing price from September 2014 to June 2026, revealing the full scope of its exponential growth trajectory. From a starting price of just $457 in 2014, Bitcoin remained relatively flat for several years before the first major bull run in late 2017, which briefly pushed the price past $19,000. What followed was an extended bear market through 2018 and 2019. The most dramatic growth occurred between 2020 and 2021, when institutional adoption and macroeconomic conditions drove Bitcoin to a then-all-time high above $60,000. The chart then captures the 2022 collapse and the subsequent recovery cycle that culminated in a new all-time high of approximately $126,000 in late 2025. The shape of this chart is the defining story of Bitcoin — long periods of consolidation punctuated by rapid, parabolic moves.


2. Bitcoin Trading Volume Over Time

<img width="584" height="455" alt="image" src="https://github.com/user-attachments/assets/6c42fca9-1aab-4ebb-b61b-6d845a9e0c5a" />


This chart tracks daily trading volume across the full dataset period. Volume is a measure of market participation — how many Bitcoin units were exchanged on any given day. The chart shows a clear structural shift: trading activity was minimal in the early years (2014–2016), began growing during the 2017 bull run, and expanded significantly from 2020 onwards as Bitcoin became a mainstream financial asset. The single most prominent spike — visible as a sharp vertical bar around 2021 — represents an extraordinary surge in trading activity, likely coinciding with Bitcoin's first breach of $60,000 and the subsequent sharp correction. The generally elevated and spiky volume pattern post-2023 reflects the maturation of the market, with more participants, derivatives activity, and institutional flows contributing to daily turnover.


3. Bitcoin Close Price with Major Market Events

<img width="1389" height="790" alt="image" src="https://github.com/user-attachments/assets/c2a1544e-6683-4a06-804a-36baddafff2e" />


This annotated chart overlays key market events directly onto the price series, providing critical context for the peaks and crashes visible in the raw price data.


2018 Crash — Following the speculative peak of late 2017, Bitcoin lost over 80% of its value through 2018, bottoming out below $3,500. This crash was driven by regulatory fears, the collapse of the ICO boom, and a broader reversal of retail sentiment.
2021 Peak — Bitcoin reached approximately $68,000 in November 2021, fuelled by institutional adoption (MicroStrategy, Tesla), the launch of Bitcoin ETF futures, and unprecedented liquidity from global monetary stimulus.
2022 Crash — The price fell from its 2021 peak to below $16,000 by late 2022. The primary catalysts were the collapse of the Terra/LUNA stablecoin ecosystem in May 2022 and the implosion of the FTX exchange in November 2022.
2024 Peak — Bitcoin surpassed $100,000 for the first time, driven by the approval of spot Bitcoin ETFs in the United States and renewed institutional and retail demand heading into the 2024 halving cycle.



4. Bitcoin Close Price with 7-Day and 30-Day Moving Averages

<img width="1389" height="790" alt="image" src="https://github.com/user-attachments/assets/baf061c6-d5e5-4193-8b7c-ee75495c25a0" />


Moving averages are among the most widely used tools in financial analysis. This chart plots the raw closing price alongside a 7-day rolling mean (orange) and a 30-day rolling mean (green).

The 7-day average reacts quickly to price changes and closely tracks the raw price, making it useful for identifying short-term momentum. The 30-day average is smoother and slower to react, making it better suited for identifying the broader trend direction. When the shorter moving average crosses above the longer one, this is commonly interpreted as a bullish signal; the reverse is a bearish signal. In this chart, the convergence of both averages with the raw price during sustained trends — such as the 2020–2021 bull run and the 2024–2025 rally — confirms the strength and persistence of those moves. During periods of high volatility, such as mid-2021 and throughout 2022, the gap between the price and the 30-day average widens considerably, reflecting the speed and severity of those market swings.


5. Bitcoin Price and Volume Combined Analysis

<img width="1389" height="989" alt="image" src="https://github.com/user-attachments/assets/8f63f181-205e-4a5d-8965-913b3a21591c" />


This dual-panel chart combines the price analysis (with moving averages) in the upper panel and trading volume in the lower panel, allowing both to be read in parallel across the same time axis. This layout makes it possible to observe the relationship between price movements and trading activity directly.

Several key observations emerge from this chart. First, the largest volume spikes tend to cluster around significant price events — both rallies and crashes — suggesting that extreme moves attract heightened participation. Second, volume in the lower panel remained structurally low before 2018 and began growing in earnest from 2020 onwards, mirroring the institutionalisation of Bitcoin as an asset class. Third, the period from 2024 to 2026 shows persistently elevated volume relative to earlier cycles, indicating a deeper and more liquid market than existed during Bitcoin's early years. The near-zero volume-price direction correlation (0.027) calculated during the analysis is consistent with what this chart shows visually: high volume days occur on both up days and down days with roughly equal frequency.



Key Findings

Price Performance


Starting price (Sep 17, 2014): $457.33
Latest price (Jun 2026): ~$62,000
All-time high: $126,198 — reached on October 6, 2025
All-time low: $171.51 — recorded on January 14, 2015
Total return over the full period: +13,221%


Time to Multiply

MultipleTarget PriceDate ReachedTime Taken10x$4,573August 29, 20172.9 years100x$45,733February 8, 20216.4 years200x$91,467November 19, 202410.2 years

Best & Worst Single Days

DateReturnClosing Price📈 Best DayDecember 7, 2017+25.4%$17,899📉 Worst DayMarch 12, 2020–37.2%$4,970

The worst single day coincides with the global COVID-19 market crash, when Bitcoin dropped alongside traditional equities before staging one of its strongest recoveries on record.

Annual Returns

YearAnnual Return2014–31.27%2015+34.37%2016+123.75%2017+1,369.03% ← Best year2018–73.48% ← Worst year2019+92.00%2020+303.09%2021+59.71%2022–64.27%2023+155.41%2024+120.98%2025–6.33%

2017 stands out as Bitcoin's most extraordinary year — a 13x return driven by retail speculation and the initial coin offering (ICO) boom. The following year saw an equally dramatic reversal.

Drawdowns

The single largest drawdown in this dataset occurred on December 15, 2018, when Bitcoin had fallen –83.4% from its then-all-time high of approximately $19,500 set in late 2017. The 2022 bear market produced a second major drawdown of over 77%, driven by the collapse of the Terra/LUNA ecosystem and the FTX exchange.

Volatility & Volume


Bitcoin closed higher than it opened on 52.4% of trading days — only marginally above random, highlighting how difficult short-term prediction is
The correlation between trading volume and directional price movement is 0.027 — essentially zero — meaning high-volume days do not reliably predict whether the price will rise or fall
The 30-day rolling volatility peaks sharply during crash events (2018, 2020, 2022), confirming that volatility is mean-reverting but fat-tailed in Bitcoin markets



How to Run

Option 1 — Google Colab (recommended):

Open bitcoin_analysis.ipynb directly in Google Colab and run all cells in order. Upload bitcoin_dataset.csv when prompted.

Option 2 — Local environment:

bashgit clone https://github.com/YOUR_USERNAME/bitcoin-analysis.git
cd bitcoin-analysis
pip install -r requirements.txt
jupyter notebook bitcoin_analysis.ipynb


Requirements

pandas
numpy
matplotlib
jupyter


Data Source

Kaggle
. The dataset spans September 17, 2014 to June 5, 2026 and contains 4,280 records with no missing values.


Limitations


This analysis is purely descriptive and retrospective — no predictive modelling is applied
Past performance of Bitcoin is not indicative of future results
The dataset does not account for exchange-specific pricing differences or on-chain metrics



Author

Levi Sadoh

Data Analyst


This project was completed as a personal portfolio piece to demonstrate applied data analysis on real-world financial time series data.
