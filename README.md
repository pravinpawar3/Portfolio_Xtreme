# Portfolio Risk Assessment and Backtesting Tool

## Overview

This tool is designed to assess portfolio performance through various metrics including Value at Risk (VaR), Conditional Value at Risk (CVaR), and backtesting with daily rebalancing. The program simulates multiple portfolios with different asset compositions, performs risk assessments, conducts scenario analysis, and plots key metrics such as cumulative returns, volatility, Sharpe ratio, and max drawdown.

The tool uses historical data of stocks downloaded from Yahoo Finance (`yfinance`) and performs analysis on different portfolio compositions, including tech stocks, diverse assets, and high dividend yield stocks.

![image](https://github.com/user-attachments/assets/418db030-52a5-478f-ba8e-31ec2dea0ae1)

![image](https://github.com/user-attachments/assets/48603384-47f9-48ae-a937-1953658afca2)

## Features

- **Portfolio Simulation**: Simulates multiple portfolios with different asset compositions.
- **Risk Assessment**: Calculates Value at Risk (VaR) and Conditional Value at Risk (CVaR) for the portfolios.
- **Scenario Analysis**: Analyzes portfolio performance under different market scenarios (e.g., Bull Market, Bear Market, Stagnant Market).
- **Backtesting**: Evaluates portfolio performance using daily rebalancing, and calculates key metrics such as cumulative returns, volatility, Sharpe ratio, and max drawdown.
- **Visualizations**: Plots portfolio performance metrics, including cumulative returns, rolling volatility, and rolling Sharpe ratio, and generates a heatmap for asset correlations.

## Requirements

The following libraries are required to run this tool:

- `os`
- `requests`
- `time`
- `matplotlib`
- `seaborn`
- `numpy`
- `pandas`
- `scipy`
- `statsmodels`
- `yfinance`
- `sklearn`

To install all the necessary libraries, run:

```bash
pip install -r requirements.txt
```

## How to Use

1. **Download Historical Data**:
   The program will automatically download historical price data for the selected portfolios from Yahoo Finance, using the `yfinance` library.

2. **Run Portfolio Simulation**:
   The simulation will generate multiple random portfolios and calculate their performance using metrics like Sharpe ratio and annualized returns.

3. **Perform Risk Assessments**:
   The tool calculates the Value at Risk (VaR) and Conditional Value at Risk (CVaR) for each portfolio. These metrics help assess potential losses under normal market conditions.

4. **Scenario Analysis**:
   The program evaluates the portfolios under three different market scenarios: Bull Market, Bear Market, and Stagnant Market, and provides results like expected return and volatility.

5. **Backtesting**:
   A backtest is run on the portfolios with daily rebalancing. The results are evaluated by calculating cumulative returns, volatility, Sharpe ratio, and max drawdown.

6. **Visualizations**:
   The program generates visualizations, including:
   - Cumulative returns over time for each portfolio.
   - Rolling volatility and Sharpe ratio.
   - Correlation heatmap of the assets in the "Tech Stocks Portfolio."

## Example Usage

To use the tool, simply run the Python script:

```bash
python portfolio_risk_assessment.py
```

The script will:
- Download historical stock price data for the specified portfolios.
- Perform risk assessment calculations.
- Simulate portfolios and perform scenario analysis.
- Generate visualizations and display them using `matplotlib` and `seaborn`.

### Example Output

- **Optimal Weights for Portfolios**: The script will display the optimal asset weights for each portfolio to maximize the Sharpe ratio.
- **Risk Metrics**: Value at Risk (VaR) and Conditional Value at Risk (CVaR) for each portfolio.
- **Scenario Analysis Results**: Portfolio returns and volatility under various market conditions (Bull, Bear, Stagnant).
- **Backtesting Results**: Portfolio performance, including cumulative returns, volatility, Sharpe ratio, and max drawdown.
- **Visualizations**: Graphs showing cumulative returns, rolling volatility, rolling Sharpe ratio, and a correlation heatmap.

## Code Explanation

- **Risk Metrics Functions**:
  - `calculate_var`: Calculates Value at Risk (VaR) based on the returns of the portfolio.
  - `calculate_cvar`: Calculates Conditional Value at Risk (CVaR) based on the returns of the portfolio.
  
- **Scenario Analysis**: The `scenario_analysis` function simulates different market scenarios (Bull Market, Bear Market, Stagnant Market) and calculates portfolio returns and volatility for each scenario.

- **Backtesting**: The `backtest_portfolio` function performs backtesting with daily rebalancing, calculating cumulative returns, volatility, Sharpe ratio, and max drawdown for each portfolio.

- **Daily Rebalancing**: The `daily_rebalance` function recalculates portfolio weights daily based on the returns of the assets.

- **Plotting**:
  - The tool plots cumulative returns, rolling volatility, rolling Sharpe ratio, and a heatmap of asset correlations using `matplotlib` and `seaborn`.

## License

This project is licensed under the MIT License.

```

### Instructions:
1. The script will download historical price data for the assets in the selected portfolios (e.g., tech stocks, diverse assets, high dividend yield stocks) from Yahoo Finance.
2. It will simulate multiple portfolios to determine the optimal weights that maximize the Sharpe ratio.
3. The script will calculate risk metrics like Value at Risk (VaR) and Conditional Value at Risk (CVaR).
4. Scenario analysis is performed to assess how each portfolio would perform under different market conditions.
5. Backtesting is performed with daily rebalancing and various metrics are calculated.
6. Visualizations (such as cumulative returns, volatility, Sharpe ratios, and correlations) are generated for better analysis.
