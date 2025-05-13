# Optimal Portfolio Selection using Dynamic Programming

This project was completed as part of a university assignment on optimization. The objective was to construct an optimal stock portfolio using dynamic programming under risk constraints. The approach uses historical market data to calculate expected returns and standard deviations, then selects a portfolio that maximizes return while keeping total risk within a specified limit.

---

## Features

- **Dynamic Programming-based Optimization**  
  Selects an optimal set of stocks by maximizing expected return under a defined risk constraint.

- **Historical Price Analysis**  
  Fetches daily closing prices using `yfinance` for a wide range of major stock tickers.

- **Expected Return & Risk Calculation**  
  Computes log returns and uses them to derive expected monthly returns and risk (standard deviation).

- **Constraint-Aware Portfolio Selection**  
  Ensures a minimum number of stocks are selected and the total risk does not exceed the allowable threshold.

---

## Technologies Used

- **Python**
- **yfinance** – For downloading historical stock price data  
- **NumPy** – For numerical computations  

---

## How It Works

1. **Data Fetching**  
   Downloads stock price data between specific dates for over 100 well-known tickers.

2. **Metric Calculation**  
   Calculates expected return and risk using log returns over a 30-day (1.5-month) period.

3. **Dynamic Programming Optimization**  
   Builds a DP table to find the optimal subset of stocks that fit within the max risk threshold.

4. **Backtracking**  
   Identifies the selected stocks by backtracking the DP table.
