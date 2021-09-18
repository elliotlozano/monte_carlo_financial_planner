# Financial Planner with Monte Carlo Simulations

`This project uses Monte Carlo Simulations to evaluate credit union members' financial health by creating a financial plan for budgeting and retirement.`

---

## Description

In this project, I’ll create two financial analysis tools by using a single Jupyter notebook. In "Part 1" I will create a financial planner for emergencies. The members will be able to use this tool to visualize their current savings. The members can then determine if they have enough reserves for an emergency fund. In "Part 2" I will create a financial planner for retirement. This tool will forecast the performance of their retirement portfolio in 30 years. To do this, the tool will make an Alpaca API call via the Alpaca SDK to get historical price data for use in Monte Carlo simulations.

---

## Technologies

This project leverages python 3.7 with the following packages:

* [pandas](https://github.com/pandas-dev/pandas) - For reading data into a DataFrame.

* [matplotlib](https://matplotlib.org/stable/users/index.html) - For embedding plots in the application.

* [os](https://docs.python.org/3/library/os.html) - For providing a portable way of using operating system dependent functionality.

* [datetime](https://docs.python.org/3/library/datetime.html) - For supplying classes for manipulating dates and times.

* [json](https://docs.python.org/3/library/json.html) - For data interchange.

* [requests](https://docs.python-requests.org/en/master/index.html) - For sending HTTP/1.1 requests.

* [dotenv](https://pypi.org/project/python-dotenv/) - For reading key-value pairs from a .env file and setting them as environment variables.

* [alpaca_trade_api](https://alpaca.markets/docs/api-documentation/) - For collecting relevant price data from Alpaca Trade API.

* [pytz](https://pypi.org/project/pytz/) - For accurate timezone calculations.

---

## Installation Guide

Before running the application first install the following dependencies:

```python
  pip install pandas
  pip install mkdocs
  pip install requests
  pip install python-dotenv
  pip install alpaca-trade-api
```

---

## Usage

To use the Portfolio Optimizer:

1. Locally clone the monte_carlo_financial_planner repository from GitHub using the following link:

```python
git clone https://github.com/elliotlozano/monte_carlo_financial_planner.git
```

2. Run the [Monte Carlo Financial Planner](financial_planning_tools.ipynb) program.

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