# Data Science Report: Trader Behavior vs Market Sentiment

## 1. Objective
The goal of this analysis was to explore the relationship between trader behavior (profitability, volume, leverage choice) and overall market sentiment (Fear vs. Greed Index). Understanding these correlations can help in developing sentiment-aware trading strategies.

## 2. Methodology
### Data Processing
- **Trading Data**: Aggregated historical trade data (`historical_data.csv`) by date to calculate daily metrics:
  - Total Trading Volume (USD)
  - Net Profit/Loss (PnL)
  - Long/Short Ratio
- **Sentiment Data**: Aligned the Bitcoin Fear & Greed Index (`fear_greed_index.csv`) with the trading dates.
- **Merging**: The datasets were merged on the `Date` field to allow for daily comparison.

### Analyzed Metrics
- **Volume vs Sentiment**: Investigating if extreme sentiment correlates with higher trading activity.
- **PnL by Sentiment**: analyzing if traders are more profitable during "Fear" or "Greed" periods.
- **Risk Behavior**: Observing if leverage or position sizes change with sentiment.

## 3. Key Findings & Visualizations

### 3.1 Trading Volume vs Sentiment
**Visualization**: `outputs/Tradingvol_vs_Marketsentiment.png` and `outputs/Tradingvol_vs_FearGreedIndex.png`
- The analysis plots daily trading volume against the Fear & Greed Index.
- Periods of **Extreme Greed** often coincide with heightened market activity and volume spikes, as retail interest peaks.
- Conversely, **Extreme Fear** can also drive volume due to panic selling, fitting a "U-shaped" volume profile relative to sentiment.

### 3.2 Profitability (PnL) across Sentiment Zones
**Visualization**: `outputs/TotalPnL_by_MarketSentiment.png`
- Box plots of Daily PnL grouped by sentiment classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed).
- The distribution highlights the variance in trader performance. High volatility during "Extreme Fear" can lead to both significant gains (for short sellers) and losses (liquidations).

### 3.3 Sentiment-Driven Behavior
- **Output**: `csv_files/final_analysis_output.csv`
- **Long/Short Ratio**: Traders tend to be net long during Greed phases, often leading to overcrowding.
- **Contrarian Opportunities**: The data suggests that improved risk-adjusted returns might be found by taking contrarian positions when sentiment reaches extreme levels (e.g., >75 or <25).

## 4. Conclusion
Market sentiment is a powerful driver of trading flows. The analysis demonstrates that volume and profitability are not uniform across market conditions. Integrating a sentiment filter—reducing size during choppy "Neutral" periods or looking for mean reversion at "Extremes"—could enhance trading strategy performance.



