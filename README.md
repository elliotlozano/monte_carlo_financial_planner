# Financial Planner with Monte Carlo Simulations

`This project uses Monte Carlo Simulations to evaluate credit union members' financial health by creating a financial plan for budgeting and retirement.`

---

## Description

As an analyst at your firm, I am trying to find the best investment strategies for our clients. This program uses the `pandas` library, the `numpy` library, and inline plotting to determine which investment will be considered for inclusion in clients' portfolios. The top investment will be selected based on favorable metrics when analyzing daily returns, cummulative returns, standard deviations, Sharpe ratios, and rolling betas. Each metric will be evaluated independently and then together so I can provide a recommendation for the best risk-reward investment option.

---

## Technologies

This project leverages python 3.7 with the following packages:

* [pandas](https://github.com/pandas-dev/pandas) - For reading data into a DataFrame.

* [pathlib](https://docs.python.org/3/library/pathlib.html) - For generating a file path to a CSV.

* [numpy](https://github.com/numpy/numpy) - For scientific computing in Python.

* [matplotlib](https://matplotlib.org/stable/users/index.html) - For embedding plots in the application.

---

## Installation Guide

Before running the application first install the following dependencies:

```python
  pip install pandas
  pip install mkdocs
```

---

## Usage

To use the Portfolio Optimizer:

1. Locally clone the portfolio_optimizer repository from GitHub using the following link:

```python
git clone https://github.com/elliotlozano/portfolio_optimizer.git
```

2. Run the [portfolio optimizer](risk_return_analysis.ipynb) program.

3. Examine the graphs and review the commentary describing the significance of the results.

---

## Findings

The following visuals helped identify the best investment option for our clients' portfolios.

![Cummulative Returns All Assets](cummulative_returns.png)
`This graph shows the cummulative return for each asset. It's clear the market gives the highest return when compared to the four whale funds. Paulson & Co. Inc. performed the worst over the period.`

![Daily Returns Boxplot for Whale Funds](whale_daily_returns_boxplot.png)
`This graph is a good analysis of risk due to volatility. The box plots show the spread of daily returns for each asset. Berkshire Hathaway Inc. shows the largest spread meaning that it experienced the most volatility over the period, and therefore higher risk. Tiger Global Management LLC had the tightest spread, meaning the fund experienced the least amount of volatility in daily returns.`

![Sharpe Ratios All Assets](Sharpe_ratios.png)
`This bar graph depicts the Sharpe ratio for each asset - a metric used to evaluate an investment's risk-reward profile. It shows only three of the five assets have a strong enough ratio to be considered a worthwhile investment. We can eliminate the funds with negative Sharpe ratios and focus on Berkshire Hathaway Inc., Tiger Global Management LLC, and the S&P 500.`

![Rolling Beta for Two Whale Funds](rolling_beta_overlay.png)
`For a more conservative portfolio we will consider only Berkshire Hathaway Inc. and Tiger Global Management LLC since the S&P 500 showed greater volatility risk. Between the top two whale funds, Berkshire Hathaway Inc. acheived a higher rolling beta (0.22 vs. 0.03), meaning it was more sensitive to movements in the market. Since both funds scored relatively low beta values (well under 1.0), neither are considered risky compared to the S&P 500 so a higher beta may actually be considered more attractive in this case. Berkshire Hathaway Inc. seems to be the best option for our clients' portfolios.`

---

## Contributors

Elliot Lozano

[E-mail](elliotlozano95@gmail.com)

---

## License

MIT