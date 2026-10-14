📊 Bitcoin & Altcoin Sensitivity Analysis

A lightweight quantitative model built in Excel to evaluate altcoin sensitivity relative to Bitcoin, using historical returns, CAPM regression metrics, and a discrete-time Markov chain.

Overview

This project analyzes 1-year historical daily prices and returns for Bitcoin and a selection of altcoins to measure relative market risk, baseline performance, and regime dynamics:

Beta ($\beta$) & Alpha ($\alpha$): Linear regression against BTC daily returns to evaluate market sensitivity, systemic exposure, and excess return per asset.

Return Distributions: Variance, standard deviation, and comparative volatility across major tokens.

Dogecoin Markov Chain Model: A discrete transition probability matrix built on historical return states (Bullish / Neutral / Bearish) to calculate state transition probabilities and steady-state behavior for DOGE.

Methodology

Data Ingestion: 1-year daily closing prices for BTC and selected altcoins.

Log/Daily Returns: Derived return series used as the input for risk-adjusted metrics.

Regression Analysis:


$$R_i - R_f = \alpha_i + \beta_i (R_{BTC} - R_f) + \epsilon_i$$


Used to estimate individual altcoin elasticity against the broader crypto benchmark (BTC).

State Transition Modeling (DOGE):

Defined daily return thresholds into regimes: Bullish, Neutral, and Bearish.

Constructed an empirical 1-step transition probability matrix ($P$).

Solved for stationary distributions to model long-run state probabilities.

File Contents

altcoins.xlsx: Core workbook containing raw price series, daily return matrices, $\alpha$/$\beta$ calculations, and the DOGE Markov state transition model.
