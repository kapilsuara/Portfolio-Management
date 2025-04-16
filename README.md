# Portfolio-Management
This repository focuses on data analysis, quantitative methodologies, and algorithm development.

# Stock Portfolio Analysis and Trading Strategy


This project implements a systematic stock selection and portfolio management strategy with performance analysis against the NIFTY 50 benchmark index.

## Features

- **Data Integration**: Combines ESV (Economic Scenario Variables) and Hover technical indicator datasets
- **Stock Selection Algorithm**: Implements a 10-condition filter for quality stock selection
- **Dynamic Portfolio Allocation**: Adjusts number of stocks based on investment amount
- **Monthly Portfolio Churning**: Regular rebalancing based on updated technical indicators
- **Performance Analytics**: 
  - Volatility comparison with NIFTY 50
  - Statistical significance testing
  - Risk-adjusted return metrics (Sharpe Ratio)
  - Maximum drawdown analysis
- **Visualization**: Interactive plots of portfolio vs benchmark performance

## Methodology

### Stock Selection Criteria
1. Price above 200-day moving average (D_MP200 == 'DPA200')
2. Price above 50-day moving average (D_MP50 == 'DPA50')
3. Daily RSI between 60-85
4. Monthly RSI > 40
5. Weekly RSI > 40
6. Hourly price above 50-period MA (H_MP50 == 'HPA50')
7. Hourly momentum confirmation (H_MCo == 'HBUCO')
8. Daily PDEMA20 between -2 and 2

### Portfolio Construction
```python
Investment Amount    | Stocks to Purchase
--------------------|-------------------
₹500 - ₹50,000      | 3 stocks
₹50,001 - ₹1,000,000| 4 stocks
> ₹1,000,000        | 5 stocks (max)
