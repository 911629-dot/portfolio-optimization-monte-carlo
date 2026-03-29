# Portfolio Optimization (Monte Carlo)

This project implements a classic Monte Carlo simulation to evaluate different portfolio allocations and identify both the portfolio that minimizes volatility and the one that delivers the highest return per unit of risk (Sharpe Ratio).

The notebook also provides a theoretical explanation of key concepts such as volatility, expected value, variance, standard deviation, covariance, and portfolio weights.

Stock data is downloaded using the yfinance library. It is recommended to avoid repeated downloads to prevent unnecessary API requests and improve efficiency.

## Objective

To explore how different portfolio weight combinations affect risk and return, and to determine the optimal allocation under different criteria.

## Methodology

* Random generation of portfolio weights
* Calculation of expected returns and portfolio volatility
* Computation of the Sharpe Ratio
* Identification of optimal portfolios

## Content

* portfolio_optimization_monte_carlo.ipynb

## Requirements

* Python 3.12
* numpy
* pandas
* matplotlib
* yfinance

## Installation

Using conda:
conda install -c conda-forge yfinance -y

## Results

* Simulation of multiple portfolio allocations
* Identification of optimal portfolios


Your Name
