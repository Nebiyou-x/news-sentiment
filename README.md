
# Predicting Price Moves with News Sentiment

This project explores how **financial news headlines** relate to **stock price movements** using the FNSPID (Financial News and Stock Price Integration Dataset).



## 1. Goal

Use news sentiment as a **predictive signal** for stock returns so Nova Financial Solutions can:

* Better **forecast short-term price moves**
* Build **sentiment-aware trading and risk tools**

We focus on:

* **Sentiment Analysis** of news headlines (positive / negative / neutral)
* **Correlation** between daily sentiment and **daily stock returns**


## 2. Data

**News dataset (FNSPID):**

* `headline` — news title
* `url` — link to article
* `publisher` — news source
* `date` — publication datetime (UTC-4)
* `stock` — ticker symbol (e.g. AAPL)

**Market data:**

* Daily OHLCV: `Date`, `Open`, `High`, `Low`, `Close`, `Volume`

News is aligned with price data by **ticker** and **trading date**.



## 3. What This Repo Contains

Typical structure:

```text
src/          # Data loading, EDA, sentiment, indicators, correlations
notebooks/    # EDA and analysis notebooks
tests/        # Basic unit tests
scripts/      # Optional: end-to-end pipeline runner
README.md     # (this file)
requirements.txt
```



## 4. Main Tasks

**Task 1 – EDA**

* Descriptive stats on headlines (length, counts)
* Publisher activity analysis
* News volume over time and time-of-day patterns
* Basic keyword/topic exploration

**Task 2 – Technical Indicators**

* Load OHLCV stock data
* Compute indicators: MA, RSI, MACD
* Visualize price + indicators

**Task 3 – Sentiment & Correlation**

* Score headline sentiment
* Aggregate sentiment by stock & day
* Compute daily returns
* Measure correlation between sentiment and returns (same day and next day)



## 5. How to Run

```bash
# Clone repo
git clone https://github.com/Nebiyou-x/news-sentiment.git
cd Nebiyou-x

# Create & activate venv
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# (Optional) start notebooks
jupyter lab
```



