# Retail Demand Forecasting for Inventory & Revenue Planning

## Business Problem
Retailers face a persistent tradeoff between stockouts, which lead to lost revenue and overstocking, which ties up working capital. The objective of this project is not to predict sales perfectly but to forecast demand accurately enough to support better inventory and planning decisions under uncertainty.

## Why Demand Forecasting Matters
Accurate demand forecasts enable retailers to:
- Set appropriate inventory and safety stock levels
- Plan promotions more effectively
- Reduce operational risk caused by demand volatility
- Understanding where forecasts are reliable and where they are not is critical for informed decision-making.

## Dataset
- Source: Walmart Store Sales dataset (Kaggle)
- Time period: 2010–2012 (weekly data)
- Scope:
  - Two representative stores:
    - Store 1 (relatively stable demand)
    - Store 20 (high demand volatility)
- Key variables:
  - Weekly sales
  - Holiday indicator
  - Fuel price, CPI, unemployment rate

## Approach
The analysis follows a disciplined, business-first forecasting framework:
1. Exploratory analysis to understand demand stability, seasonality and volatility
2. Feature engineering using lagged sales and rolling averages
3. Time-aware train-test split
4. Two forecasting models:
   - Exponential Smoothing (ETS) as a statistical baseline
   - Prophet with holiday and macroeconomic regressors as the primary model
5. Evaluation using business-friendly metrics:
   - MAPE
   - MAE
   - Forecast bias

## Key Findings
- Store 1 exhibits stable demand with lower forecast error, making it suitable for lean inventory strategies.
- Store 20 shows significantly higher volatility and larger demand spikes, particularly around peak periods.
- Prophet provides smoother, more stable forecasts suitable for planning, while ETS reacts more aggressively to short-term fluctuations.
- Forecast reliability varies meaningfully by store, highlighting the need for differentiated inventory policies.

## Managerial Recommendations
- Use stable-demand forecasts (e.g., Store 1) to maintain lean inventory with minimal safety stock.
- Maintain higher buffer stock for volatile stores (e.g., Store 20) to mitigate stockout risk during demand spikes.
- Avoid overreacting to short-term noise by relying on smoothed forecasts for base inventory planning.
- Apply human judgment and overrides during known peak or promotional periods.

## Limitations & Next Steps
- The analysis is based on historical data from 2010–2012; while absolute demand levels may differ today, the forecasting methodology and decision framework remain relevant.
- Future work could incorporate supply lead times, product-level granularity and scenario-based stress testing to further enhance inventory planning decisions.

