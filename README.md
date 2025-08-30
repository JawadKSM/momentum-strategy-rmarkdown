# 📈 Momentum Strategy with RSI Filter (R Markdown Project)

This repository hosts my project for the course *Introduction to Data Science with R* (MSc Finance – emlyon business school).  
The goal was to design, implement, and evaluate a **momentum-based trading strategy** in R, comparing it with a benchmark portfolio.

---

## ✨ Project Overview

- **Benchmark strategy:** equally-weighted portfolio of 88 S&P 100 stocks (2005–2025).  
- **Advanced strategy:**  
  - 6-month **momentum signal** for stock selection,  
  - **RSI filter (14 days)** to avoid overbought/oversold traps,  
  - **Long–short allocation** with weights proportional to signal strength.  
- **Dataset:** 88 stocks from the S&P 100 (via Yahoo Finance), + market capitalization data (Excel file).  
- **Evaluation metrics:** annualized return, volatility, Sharpe ratio, maximum drawdown, and return distributions.  
- **Implementation:** reproducible R Markdown (`.Rmd`) notebook knitted into an interactive HTML report.

---

## 📊 Key Findings

- The **momentum + RSI strategy** delivered higher long-term returns compared to the benchmark.  
- However, it also showed **higher volatility** and **deeper drawdowns** during crises (2008, COVID-19).  
- Sharpe ratios of both portfolios are close, suggesting comparable risk-adjusted performance.  
- The strategy demonstrates the trade-off between capturing strong market trends and exposure to sharp reversals.  

---

## 📂 Repository Structure

- `R_Project_Jawad_KASSIMI.Rmd` → R Markdown notebook with full code and explanations.  
- `R_Project_Jawad_KASSIMI.html` → rendered HTML report (with plots & results).  
- `Market_Cap.xlsx` → supplementary dataset for market capitalization analysis.  

---

## 🚀 View the Report

👉 [Click here to view the full HTML report](https://JawadKSM.github.io/momentum-strategy-rmarkdown/R_Project_Jawad_KASSIMI.html)  
---

## 🛠️ Requirements

Install the following R packages before running the `.Rmd`:  

```r
install.packages(c("quantmod", "PerformanceAnalytics", "ggplot2", "xts", 
                   "tidyverse", "dplyr", "tidyquant", "readxl", "plotly", 
                   "reshape2", "corrplot", "knitr", "kableExtra", "TTR"))
