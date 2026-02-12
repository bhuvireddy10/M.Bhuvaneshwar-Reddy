# Trader Performance vs Market Sentiment Analysis

## Objective
Analyze how Bitcoin market sentiment (Fear/Greed) influences trader behavior and performance on Hyperliquid.

---

## Methodology

### 1. Data Preparation
- Standardized column names and handled missing values.
- Converted timestamps to daily granularity.
- Merged trade records with daily sentiment classification.
- Engineered trader-level daily metrics:
  - Daily realized PnL
  - Win rate
  - Number of trades per day
  - Average trade size
  - Trader volatility (PnL standard deviation)

### 2. Analytical Approach
- Compared trader performance across Fear vs Greed regimes.
- Evaluated behavioral shifts in trade frequency and win rate.
- Segmented traders into:
  - High vs Low activity
  - Consistent vs Volatile traders
- Measured regime sensitivity across segments.

### 3. Bonus – Predictive Modeling
- Built a Random Forest classifier to predict daily trader profitability using sentiment and behavioral features.
- Evaluated using train/test split and feature importance analysis.

---

## Key Insights

1. Performance is Regime-Dependent  
Trader profitability differs across sentiment regimes. Greed periods show stronger average returns but also higher volatility, indicating increased risk exposure during bullish sentiment.

2. Behavioral Expansion During Greed  
Trade frequency increases during Greed regimes, while win rate does not improve proportionally. This suggests potential overconfidence-driven trading behavior.

3. Segment Sensitivity to Sentiment  
High-activity and volatile traders exhibit larger downside impact during Fear regimes compared to low-activity or consistent traders. Aggressive trading styles amplify regime risk.

---

## Strategy Recommendations

### Strategy 1 – Sentiment-Based Risk Moderation
During Fear regimes, reduce exposure for high-activity traders through leverage control or trade frequency limits.  
Rationale: This segment demonstrates elevated downside volatility under negative sentiment conditions.

### Strategy 2 – Overtrading Control During Greed
Implement a cap on daily trade frequency during Greed regimes.  
Rationale: Increased activity does not proportionally improve win rate and may increase variance drag.

---

## Bonus – Predictive Model

A Random Forest classifier was trained to predict daily trader profitability using sentiment and behavioral features.  
The model demonstrates measurable predictive capability, with behavioral metrics contributing more predictive power than sentiment classification alone.
