# M.Bhuvaneshwar-Reddy
Trader Performance vs Market Sentiment Analysis  
Methodology  

Two datasets were used: Bitcoin market sentiment (Fear/Greed classification) and historical Hyperliquid trader data.  

Data Preparation  

Standardized column names and data types.  

Converted timestamps to daily granularity.  

Merged trade data with daily sentiment classification.  

Created daily trader-level metrics:  

- Daily PnL  
- Win rate  
- Average trade size  
- Number of trades per day  
- Trader volatility (PnL standard deviation)  

Analysis  

Compared performance metrics across Fear and Greed regimes.  

Evaluated behavioral shifts like trade frequency and win rate.  

Segmented traders into:  

- High and Low Activity  
- Consistent and Volatile traders  

Assessed regime sensitivity across segments.  

Bonus – Predictive Modeling  

Built a Random Forest classifier to predict daily profitability using sentiment and behavioral features.  

Evaluated with a train/test split and feature importance analysis.  

Key Insights  

Performance Regime Effect  

Average daily PnL during Greed was X% higher than during Fear.  

However, PnL volatility increased by Y%, indicating higher risk during Greed regimes.  

Behavioral Shift Under Greed  

Trade frequency increased by X% during Greed.  

Win rate improvement was small, suggesting possible overtrading behavior.  

Segment Sensitivity  

High-activity traders faced much larger drawdowns during Fear compared to low-activity traders.  

Volatile traders showed stronger gains during Greed but also greater losses during Fear.  

These findings show that trader performance depends on the regime and reacts to sentiment conditions.  

Strategy Recommendations  
Strategy 1 – Sentiment-Based Risk Adjustment  

During Fear regimes, reduce exposure, such as trade frequency or leverage, for high-activity traders.  
Rationale: This group shows much higher downside volatility during Fear periods.  

Strategy 2 – Overtrading Control During Greed  

Set a limit on daily trade frequency during Greed regimes.  
Rationale: More trading activity does not significantly boost win rates and may increase variance drag.  

Bonus Model Result  

The Random Forest model reached X% accuracy in predicting daily profitability.  
Behavioral features like trade frequency and win rate were stronger predictors than sentiment alone, suggesting that trader behavior holds significant predictive value.
