# Portfolio Optimization & Risk Analysis Using Python

This project demonstrates **portfolio optimization and risk analysis** using Python.  
I've analyzed 5 major US stocks (AAPL, MSFT, TSLA, JNJ, JPM) to build an **optimal portfolio** using **daily returns, risk metrics, and Monte Carlo simulation**.

## Project Overview

The project workflow includes:

1. **Data Collection:** Downloading daily stock prices from Yahoo Finance.
2. **Exploratory Data Analysis (EDA):** Visualizing price movements, computing daily returns, and checking correlations.
3. **Portfolio Construction:** Building an equal-weighted portfolio and computing performance metrics (returns, volatility, Sharpe ratio, drawdown).
4. **Performance Attribution:** Determining each stock’s contribution to portfolio returns.
5. **Portfolio Optimization:** Using Monte Carlo simulation to find the portfolio with maximum Sharpe ratio.
6. **Visualization:** Plotting cumulative returns, correlation heatmap, and optimal portfolio allocation.

**Tools & Libraries:**
- Python
- pandas, NumPy
- matplotlib, seaborn
- yfinance

## Data

**Stocks Analyzed:**  
- Apple Inc. (AAPL)  
- Microsoft Corp. (MSFT)  
- Tesla Inc. (TSLA)  
- Johnson & Johnson (JNJ)  
- JPMorgan Chase & Co. (JPM)

**Sample Data (Closing Prices):**

| Date       | AAPL      | JNJ       | JPM       | MSFT      | TSLA     |
|------------|-----------|-----------|-----------|-----------|----------|
| 2025-01-02 | 242.53    | 139.00    | 233.97    | 414.57    | 379.28   |
| 2025-01-03 | 242.04    | 139.17    | 237.17    | 419.29    | 410.44   |
| 2025-01-06 | 243.67    | 138.66    | 236.01    | 423.75    | 411.05   |
| 2025-01-07 | 240.89    | 141.14    | 238.28    | 418.32    | 394.36   |
| 2025-01-08 | 241.38    | 137.31    | 238.24    | 420.49    | 394.94   |

**Visualization:**  
- Stock Price Movement Graph  <img width="1005" height="518" alt="download" src="https://github.com/user-attachments/assets/1e047956-a9e2-4fd8-8ef3-3343f6d4e01f" />

  _MSFT is trending highest, followed by TSLA, JPM, AAPL, JNJ._

---

## Exploratory Data Analysis (EDA)

**Daily Returns (sample):**

| Date       | AAPL      | JNJ       | JPM       | MSFT      | TSLA     |
|------------|-----------|-----------|-----------|-----------|----------|
| 2025-01-03 | -0.00201  | 0.00118   | 0.01367   | 0.01140   | 0.08216  |
| 2025-01-06 | 0.00674   | -0.00368  | -0.00488  | 0.01063   | 0.00149  |
| 2025-01-07 | -0.01139  | 0.01789   | 0.00963   | -0.01281  | -0.04060 |
| 2025-01-08 | 0.00202   | -0.02708  | -0.00016  | 0.00519   | 0.00147  |
| 2025-01-10 | -0.02410  | -0.00148  | -0.01341  | -0.01321  | -0.00051 |

**Daily Returns Histogram:**   <img width="977" height="680" alt="download" src="https://github.com/user-attachments/assets/089d1b8e-6792-4bdc-918f-f05a46f26b08" />

**Correlation Heatmap:**  <img width="645" height="545" alt="download" src="https://github.com/user-attachments/assets/9d9f0608-dfed-4628-96a4-45fc4587bd4d" />


---

## Portfolio Construction (Equal Weight)

**Weights:** 20% per stock (equal weight)  
**Cumulative Return Graph:**   <img width="575" height="453" alt="download" src="https://github.com/user-attachments/assets/ce70a47b-0bac-4940-9cbf-052ef2c091b6" />

- Initial $1 investment grows to ~\$1.30 over the year.

**Portfolio Metrics:**

| Metric                | Value        |
|-----------------------|--------------|
| Annual Return         | 0.3055       |
| Volatility            | 0.2362       |
| Sharpe Ratio          | 1.2594       |
| Maximum Drawdown      | -0.2251      |

**Interpretation:**
- **Sharpe Ratio 1.26:** Portfolio provides good return per unit of risk.  
- **Max Drawdown -22.5%:** Largest peak-to-trough loss.  
- **Annual Return 30.5%:** Total growth over the year.

---

## Performance Attribution

**Contribution to Portfolio Return (Absolute & %):**

| Ticker | Absolute | % Contribution |
|--------|----------|----------------|
| AAPL   | 0.0329   | 11.19%         |
| JNJ    | 0.0824   | 28.03%         |
| JPM    | 0.0693   | 23.57%         |
| MSFT   | 0.0361   | 12.28%         |
| TSLA   | 0.0733   | 24.92%         |

_Observation:_ JNJ, TSLA, and JPM contributed the most to portfolio gains.

---

## Portfolio Optimization (Monte Carlo Simulation)

Goal: Maximize Sharpe Ratio.

**Optimal Portfolio Weights:**

| Ticker | Weight  |
|--------|---------|
| MSFT   | 0.7448  |
| JNJ    | 0.1151  |
| TSLA   | 0.0970  |
| JPM    | 0.0381  |
| AAPL   | 0.0050  |

**Visualization:** 
- MSFT dominates the optimal portfolio (>74% allocation).  
- Remaining stocks have minor allocations.
<img width="567" height="456" alt="download" src="https://github.com/user-attachments/assets/f308405e-73df-4373-b6c6-5f517c5c1984" />

---

## Visualizations 

1. `stock_prices.png` → Daily stock price movement
 <img width="1005" height="518" alt="download" src="https://github.com/user-attachments/assets/4a9126ce-99a7-4104-a09f-56a652a3e04d" />

2. `returns_histogram.png` → Daily returns distribution
 <img width="977" height="680" alt="download" src="https://github.com/user-attachments/assets/c941bba0-32db-4a1d-bd0d-ee321929046e" />

3. `correlation_heatmap.png` → Correlation between stocks
 <img width="645" height="545" alt="download" src="https://github.com/user-attachments/assets/4d3223af-4e1e-47e5-a822-5473a8b6d0d4" />

4. `equal_weight_cum_returns.png` → Equal-weight portfolio cumulative returns
 <img width="575" height="453" alt="download" src="https://github.com/user-attachments/assets/83019e8f-8809-442f-add4-7863c643fa7e" />

5. `optimal_portfolio_allocation.png` → Optimal weights bar chart
 <img width="567" height="456" alt="download" src="https://github.com/user-attachments/assets/62ea98fd-6116-49b3-8b95-f9c501604b0d" />

6. Efficient Frontier of Simulated Portfolios
Each point represents a portfolio with different weight allocations.  
- X-axis: Portfolio risk (volatility)  
- Y-axis: Expected return  
- Color: Sharpe ratio (risk-adjusted return)  
Bright points represent portfolios with higher Sharpe ratios, indicating optimal trade-offs between risk and return.
<img width="822" height="545" alt="download" src="https://github.com/user-attachments/assets/151204dd-e2a8-4831-84f4-a5443d17ae71" />

7 Efficient Frontier Visualization
The scatter plot shows all simulated portfolios with varying weights. 
- X-axis: Portfolio Volatility (Risk)
- Y-axis: Portfolio Expected Return
- Color gradient: Sharpe Ratio (reward per unit risk)
- Red Star: Portfolio with highest Sharpe Ratio (Optimal Portfolio)
<img width="576" height="453" alt="download" src="https://github.com/user-attachments/assets/896ebbef-663b-49fd-bdba-6fa82329dd84" />

