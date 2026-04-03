# Portfolio Optimization

This project explores two approaches to portfolio optimization using **KO, WMT, and VOO** 
as assets, covering the period from January 2020 to January 2024.

Stock data is downloaded using the `yfinance` library. It is recommended to avoid 
repeated downloads to prevent unnecessary API requests.

---

## Approaches

**1. Monte Carlo Simulation**
Random generation of portfolio weights to explore the risk-return space and identify 
the portfolios with the minimum volatility and the highest Sharpe Ratio.

**2. Mathematical Optimization (SLSQP)**
Formal maximization of the Sharpe Ratio by solving a constrained nonlinear programming 
problem via `scipy.optimize.minimize`.

$$\min_{w} \left( -\frac{\mu_p}{\sigma_p} \right) \quad \text{subject to} \quad \sum_i w_i = 1, \quad 0 \leq w_i \leq 1$$

For full documentation on the optimizer:
[scipy.optimize.minimize — SciPy v1.17.0 Manual](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.minimize.html)

---

## Results

The optimizer assigned **0% to KO**, the full analysis is documented in the notebook. 
In short: KO delivered roughly half the return of VOO and WMT with nearly identical 
volatility, and its high correlation with VOO (0.68) eliminated any diversification benefit.

---

## Content
* `portfolio_optimization_monte_carlo.ipynb`
* `portfolio_optimization_slsqp.ipynb`

## Requirements
* Python 3.12
* numpy
* pandas
* matplotlib
* scipy
* yfinance

## Installation
```bash
conda install -c conda-forge yfinance scipy -y
```

