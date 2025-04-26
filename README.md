# 📊 Quantifying Portfolio Risk: VaR, CVaR, and Stress Testing

## Overview
This project develops a full portfolio risk management framework using Value at Risk (VaR), Conditional Value at Risk (CVaR), and stress testing techniques.  
It aligns with Basel III/IV regulatory requirements and covers both standard and stressed market conditions.

---

## 🎯 Objective
* Quantify daily and multi-horizon portfolio risk using different VaR and CVaR methodologies.
* Perform regulatory backtesting (Kupiec and Christoffersen tests) to validate model reliability.
* Simulate crisis scenarios (2008 financial crisis) to assess stressed VaR.
* Compare risk estimates across normal and extreme market environments.

---

## 🛠 Methodologies Implemented
**VaR Computations:**
* Parametric (SMA, EWMA)
* Non-Parametric (Historical Simulation)
* Hybrid (Filtered Historical Simulation)
* Monte Carlo Simulation (Parametric and Bootstrap)

**CVaR (Expected Shortfall):**
* Parametric Delta-Normal
* Non-Parametric Historical Estimation

**Stress Testing:**
* Stressed VaR using returns from the 2008–2009 financial crisis.

**Regulatory Backtesting:**
* Kupiec Proportion of Failures (POF) Test
* Christoffersen Independence and Conditional Coverage Tests

---

## 📚 Data
**Assets:**
* Microsoft (MSFT) – Technology sector
* Canadian National Railway (CNR) – Transportation sector

**Period:**
* Primary dataset: 2023-01-01 to 2024-01-01
* Crisis period dataset: 2008-09-01 to 2009-09-01

**Sources:**
* Yahoo Finance via `yfinance` API

---

## 💼 Portfolio Construction
* Initial Investment: €10,000
* Weighting Scheme: Inverse Volatility Weighting
  * Microsoft: 64.79%
  * Canadian National Railway: 35.21%

---

## 📈 Key Results
* Annualized Return: **50.90%**
* Annualized Volatility: **23.89%**
* Diversification Benefit: **Low correlation (0.09)** between assets.

**Risk Estimates (Daily VaR at 99% confidence level):**
* SMA: -3.50% (€-350.12)
* EWMA: -2.79% (€-278.58)
* Historical Simulation: -3.58% (€-358.04)
* Hybrid VaR: -4.07% (€-406.76)
* Monte Carlo Parametric: -3.55%
* Monte Carlo Non-Parametric: -3.58%

**Stress Testing:**
* Stressed VaR during 2008 crisis: **€-828.52** (vs. €-358.04 in normal times)

**Backtesting:**
* Most VaR models passed Kupiec and Christoffersen tests.
* EWMA VaR showed excessive violations ("yellow zone" under Basel III).

---

## 🛠 Tools and Libraries
* Python 3.9
* pandas
* numpy
* matplotlib
* scipy
* yfinance

---

## 🚀 How to Run
1. Clone the repository.
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Run `VaR_CVaR_RiskManagement.ipynb` from start to finish.

---

## 🔮 Future Improvements
* Implement rolling window VaR and CVaR estimation.
* Incorporate GARCH models for better volatility clustering modeling.
* Extend stress testing to hypothetical future scenarios.
* Add copula-based dependency modeling for extreme tail dependence.

---

## 📖 References
* Alexander, C. (2008). *Market Risk Analysis, Volume I: Quantitative Methods in Finance*. Wiley.
* Alexander, C. & Sarabia, J. M. (2011). *Value-at-Risk Model Risk*. SSRN.
* Glasserman, P. (2004). *Monte Carlo Methods in Financial Engineering*. Springer.
* Hassani, S. S. & Dionne, G. (2021). *Nouvelle réglementation internationale du risque de marché: rôles de la VaR et de la CVaR*. Assurances et gestion des risques.
* Petrov, D. (2025). *Risk Management* [Course notes].

---

## 📑 License
This project is for educational purposes only.
