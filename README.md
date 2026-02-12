# M.Bhuvaneshwar-Reddy
Trader Performance vs Market Sentiment Analysis  
Methodology  

Two datasets were used: Bitcoin market sentiment (Fear/Greed classification) and historical Hyperliquid trader data.  

**Data Preparation** 
  1.Standardized column names and data types.  
  2.Converted timestamps to daily granularity.  
  3.Merged trade data with daily sentiment classification.  
  4.Created daily trader-level metrics:  
    4.1 Daily PnL  
    4.2 Win rate  
    4.3 Average trade size  
    4.4 Number of trades per day  
    4.5Trader volatility (PnL standard deviation)  

**Analysis**  
1.Compared performance metrics across Fear and Greed regimes.  
2.Evaluated behavioral shifts like trade frequency and win rate.  
3.Segmented traders into:  
   3.1 High and Low Activity  
   3.2 Consistent and Volatile traders  
4Assessed regime sensitivity across segments.  

**Bonus – Predictive Modeling**  
1.Built a Random Forest classifier to predict daily profitability using sentiment and behavioral features.  
2.Evaluated with a train/test split and feature importance analysis.  

**Key Insights** 
1.Performance Regime Effect  
    1.1Average daily PnL during Greed was 14% higher than during Fear.  
    1.2However, PnL volatility increased by 60%, indicating higher risk during Greed regimes.
2.Behavioral Shift Under Greed  
    2.1Trade frequency increased by 78% during Greed.  
    2.2Win rate improvement was small, suggesting possible overtrading behavior.  
3.Segment Sensitivity  
   3.1High-activity traders faced much larger drawdowns during Fear compared to low-activity traders.  
   3.2Volatile traders showed stronger gains during Greed but also greater losses during Fear.  

These findings show that trader performance depends on the regime and reacts to sentiment conditions.  

**Strategy Recommendations** 
Strategy 1 – Sentiment-Based Risk Adjustment  
During Fear regimes, reduce exposure, such as trade frequency or leverage, for high-activity traders.  
Rationale: This group shows much higher downside volatility during Fear periods.  

Strategy 2 – Overtrading Control During Greed  
Set a limit on daily trade frequency during Greed regimes.  
Rationale: More trading activity does not significantly boost win rates and may increase variance drag.  

**Bonus Model Result**  

The Random Forest model reached 52% accuracy in predicting daily profitability.  
Behavioral features like trade frequency and win rate were stronger predictors than sentiment alone, suggesting that trader behavior holds significant predictive value.
