# Bitcoin Market Sentiment Analysis Using Fear & Greed Index

This project explores the relationship between cryptocurrency trading performance (using historical trading data from Hyperliquid) and market sentiment (using the Bitcoin Fear & Greed Index).

## Objective
The goal of this analysis is to:
1. Examine how different market sentiment conditions influence trading profitability (`Closed PnL`), trading volume, transaction costs, and trader behavior.
2. Uncover hidden behavioral patterns in trade outcomes across different market cycles.
3. Deliver data-driven recommendations that can assist in forming smarter, sentiment-aware Web3 trading strategies.

## Datasets Used
* **Historical Trader Data (Hyperliquid):** Contains transaction-level logs (211,224 entries) with columns including `Account`, `Coin`, `Execution Price`, `Size USD`, `Side`, `Direction`, `Closed PnL`, and `Fee`.
* **Bitcoin Fear & Greed Index Dataset:** Contains daily sentiment classification metrics (2,644 entries) with columns `timestamp`, `value`, `classification` (Extreme Fear, Fear, Neutral, Greed, Extreme Greed), and `date`.

## Methodology
1. **Data Cleaning & Alignment:** Standarized all timestamp formats and parsed daily date keys.
2. **Data Integration:** Merged the transaction-level trading data with daily market sentiment indexes via a left merge on the `date` key.
3. **Exploratory Data Analysis (EDA):** Grouped trading records by sentiment category to analyze profitability distribution, trade sizes, transaction volumes, and fees.
4. **Behavioral Analysis:** Analyzed trading direction (Long vs. Short, Buy vs. Sell) and win/loss frequencies across different market sentiments.
5. **Correlation & Segmentation Analysis:** Computed correlation heatmaps for numeric variables and conducted top vs. bottom trader profitability comparisons.

## Key Findings
* **Profitability vs. Sentiment:** Traders achieved the highest average profitability per trade during **Extreme Greed** periods (67.89 USD). However, **Fear** conditions contributed the largest share of overall realized profits (32.7% of total gains) because of significantly higher trading volume.
* **Volume & Fees:** Fear periods generated the highest total trading volume (483+ million USD) and highest average fees (1.50 USD), showing that periods of market anxiety are associated with intense trading activity and transaction costs.
* ** speculation:** speculative trades (Open Short / Close Short) surged during Greed periods, while Open Long and Close Long trades peaked during Fear conditions.
* **Asset Concentration:** Profitability was highly concentrated, with a small number of assets (led by `@107`, `HYPE`, `SOL`, `ETH`, and `BTC`) driving the vast majority of realized gains.

## Tools Used
* **Python** (Programming language)
* **Pandas** (Data manipulation and analysis)
* **Matplotlib & Seaborn** (Data visualization)
* **Jupyter Notebook** (Interactive research environment)

## Conclusion
Market sentiment is a powerful driver of cryptocurrency trading behavior and profitability. While Extreme Greed conditions offer the highest average profit per trade with lower relative transaction costs, Fear conditions create high-volatility, high-volume environments where the largest cumulative profits are generated. Integrating sentiment indicators such as the Fear & Greed Index into trading models helps optimize asset exposure and improve risk management.
