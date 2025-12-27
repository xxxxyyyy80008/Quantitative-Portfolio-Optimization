# Portfolio Optimization and Analysis


![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

A collection of Jupyter notebooks implementing **Modern Portfolio Theory (MPT)**, **Monte Carlo simulation**, and **advanced risk analytics** for quantitative portfolio management and risk measurement.

---

##  Table of Contents

- [Overview](#overview)
- [Notebooks](#notebooks)
  1. Portfolio Optimization using Monte Carlo Methods
      - [Documentation](https://github.com/xxxxyyyy80008/Quantitative-Portfolio-Optimization/blob/main/docs/01_portfolio_optimization_monte_carlo.md)
      - [Github Notebook](https://github.com/xxxxyyyy80008/Quantitative-Portfolio-Optimization/blob/main/notebooks/01_portfolio_optimization_monte_carlo.ipynb)
      - [Kaggle Notebook](https://www.kaggle.com/code/xxxxyyyy80008/portfolio-optimization-with-monte-carlo)
  2. Portfolio Optimization - PyPortfolioOpt
      - [Documentation](https://github.com/xxxxyyyy80008/Quantitative-Portfolio-Optimization/blob/main/docs/02_portfolio_optimization_pyportfolioopt.md)
      - [Github Notebook](https://github.com/xxxxyyyy80008/Quantitative-Portfolio-Optimization/blob/main/notebooks/02_portfolio_optimization_pyportfolioopt.ipynb)
      - [Kaggle Notebook](https://www.kaggle.com/code/xxxxyyyy80008/portfolio-optimization-mc-and-pyportfolioopt) 
  3. Portfolio Risk Analytics - VaR & ES](#3-portfolio-risk-analytics---var--es) 
      - [Documentation](https://github.com/xxxxyyyy80008/Quantitative-Portfolio-Optimization/blob/main/docs/03_portfolio_risk_analytics_var_and_es.md)
      - [Github Notebook](https://github.com/xxxxyyyy80008/Quantitative-Portfolio-Optimization/blob/main/notebooks/03_portfolio_risk_analytics_var_and_es.ipynb)
      - [Kaggle Notebook](https://www.kaggle.com/code/xxxxyyyy80008/portfolio-risk-analytics-var-and-es)
- [Key Features](#key-features)
- [Installation](#installation)
- [Requirements](#requirements)
- [License](#license)

---

##  Overview

This repository provides a complete quantitative finance toolkit for portfolio construction, optimization, and risk management. The framework implements **17+ distinct methodologies** spanning portfolio optimization and risk measurement, validated through rigorous backtesting and statistical analysis.

**Analysis Period**: January 2019 - December 2025  
**Confidence Level**: 99% (α = 0.01)  
**Random Seed**: 3407 (full reproducibility)

###  Applications

- **Portfolio Management**: Optimal asset allocation and risk budgeting
- **Risk Management**: VaR/ES estimation and stress testing
- **Quantitative Research**: Comparative methodology studies
- **Regulatory Compliance**: Basel III internal models validation
- **Academic Projects**: Modern Portfolio Theory implementation

---

##  Notebooks

### 1. Portfolio Optimization - Monte Carlo

**Notebook**: `01_portfolio_optimization_monte_carlo.ipynb`

[]()


#### Overview
Traditional portfolio optimization using **SciPy SLSQP** algorithm with Monte Carlo simulation to map the efficient frontier.

#### Key Features
-  **50,000 Monte Carlo simulations** for efficient frontier mapping
-  **SLSQP optimization** maximizing Sharpe Ratio
-  **Logarithmic returns** analysis
-  **Correlation analysis** for diversification insights
-  **Comprehensive visualizations**: efficient frontier, allocation charts, weight distributions

#### Methodology
- **Objective**: Maximize Sharpe Ratio
- **Algorithm**: Sequential Least Squares Programming (SLSQP)
- **Constraints**: 
  - Weights sum to 100%
  - No short selling (0 ≤ w_i ≤ 1)
- **Risk-Free Rate**: 3.6% (1-year US Treasury yield)

#### Mathematical Framework
$$\mu_P = \sum_{i=1}^{n} w_i \mu_i \times 252$$

$$\sigma_P = \sqrt{w^T \Sigma w \times 252}$$

$$SR = \frac{\mu_P - r_f}{\sigma_P}$$

---

### 2. Portfolio Optimization - PyPortfolioOpt

**Notebook**: `portfolio_optimization_pypfopt.ipynb`

#### Overview
Advanced portfolio optimization using **PyPortfolioOpt** library with dual optimization approach and discrete allocation functionality.

#### Key Features
- **Dual optimization methods**: SciPy SLSQP + PyPortfolioOpt
- **Multiple optimization strategies**: Max Sharpe, Min Volatility, Efficient Risk
- **Discrete allocation**: Convert continuous weights to integer shares
- **Side-by-side comparison**: Traditional vs. advanced methods
- **Practical implementation**: Real-world portfolio construction with $100,000 capital

#### Optimization Strategies

1. **Maximum Sharpe Ratio**
   - Optimal risk-adjusted returns
   - Best performance per unit of risk

2. **Minimum Volatility**
   - Conservative risk minimization
   - Lowest portfolio variance

3. **Efficient Risk**
   - Target volatility approach
   - Customizable risk tolerance


### 3. Portfolio Risk Analytics - VaR & ES

**Notebook**: `portfolio_risk_analytics_var_es.ipynb`

#### Overview

Comprehensive risk measurement framework implementing 17 distinct VaR and Expected Shortfall methodologies with rigorous backtesting. 

#### Key Features
- 17 VaR/ES methods: Parametric, non-parametric, and advanced historical
- Kupiec POF backtesting: Statistical validation of all methods
- Rolling window analysis: 250-day estimation windows
- Advanced methods: Bootstrapped, age-weighted, volatility-weighted, correlation-weighted
- Comprehensive visualizations: Heatmaps, comparison charts, temporal analysis

#### VaR/ES Methods Implemented

**Parametric Methods (6)**

1. Normal Distribution VaR/ES
2. Student-t Distribution VaR/ES
3. EWMA VaR (λ = 0.94)
4. Cornish-Fisher VaR

**Non-Parametric Methods (4)**

5. Historical Simulation VaR/ES
6. Kernel Density Estimation (KDE) VaR/ES

**Advanced Historical Simulation (10)**

7. Bootstrapped Historical Simulation (BHS) - 1,000 samples
8. Age-Weighted Historical Simulation (AWHS) - λ = 0.98
9. Volatility-Weighted Historical Simulation (VWHS)
10. Correlation-Weighted Historical Simulation (CWHS)
11. Filtered Historical Simulation (FHS) - Optional GARCH
   
#### Backtesting Framework

- Kupiec Proportion of Failures (POF) Test
- Likelihood Ratio Statistic: LR ~ χ²(1)
- Decision Rule: p-value < 0.05 → Reject model
- Metrics: Breach rate, LR statistic, p-value, adequacy assessment

## Features

####  Portfolio Optimization

- Dual Optimization Approach: Compare traditional (SciPy) vs. modern (PyPortfolioOpt) methods
- Monte Carlo Simulation: 50,000 random portfolios mapping efficient frontier
- Discrete Allocation: Convert theoretical weights to actual share quantities
- Multiple Strategies: Max Sharpe, Min Volatility, Efficient Risk
- Comprehensive Analysis: Returns, volatility, correlations, Sharpe ratios

####  Risk Analytics

- 17 VaR/ES Methods: Complete methodology comparison
- Statistical Validation: Kupiec POF backtesting
- Advanced Techniques: Bootstrap, KDE, age-weighted, volatility-weighted
- Rich Visualizations: Heatmaps, comparison charts, temporal analysis
- Rolling Windows: Dynamic 250-day estimation


## Prerequisites
- Python 3.8+
- Jupyter Lab or Notebook
- Libraries: See `requirements.txt`

## Setup Instructions
1. Clone the repo: `git clone https://github.com/xxxxyyyy80008/Quantitative-Portfolio-Optimization.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Launch Jupyter: `jupyter lab`
4. Open the notebooks folder and run them in order.

## License
MIT License (see LICENSE file).
