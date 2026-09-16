# Muhammad Khan

Mathematics undergraduate in the UK, working in quantitative finance and applied
machine learning. The part I find interesting is usually not getting a number —
it is establishing whether the number is real.

**Currently:** day-ahead energy forecasting, portfolio risk and tail modelling,
and algorithmic trading research.

---

## Selected projects

### [power-load-forecast](https://github.com/MuhammadxKhan/power-load-forecast)

Day-ahead forecasting of German hourly electricity demand, built to measure what
better weather information is actually worth.

Gradient boosting reaches **1,201 MW MAE (2.27% MAPE)** on a held-out 2019–2020
test period — a **0.50 skill score** against the seasonal-naive baseline, and
ahead of the TSOs' own published day-ahead forecast scored on the same rows
(1,762 MW MAE, though it is issued at a different hour, so not quite
like-for-like).

The weather question is the point of the project. Temperature enters through
four switchable modes — `none`, `lagged`, `noisy`, `perfect` — so its value gets
measured rather than assumed. Perfect foreknowledge buys 2.5%; `lagged` is worse
than no weather at all, because yesterday's temperature only adds noise the
model has already taken from yesterday's demand. A ten-seed study and a
rolling-origin backtest then put that gain in context: the fold-to-fold range is
about five times the mean effect, so the honest answer is seasonal — 13–16% in
July and August, and nothing across winter.

`OPSD · ERA5 · PyTorch · scikit-learn · CI running self-checks and ruff on every push`

### [quantitative-portfolio-risk-engine](https://github.com/MuhammadxKhan/quantitative-portfolio-risk-engine)

Portfolio risk and allocation tested across scenario assumptions rather than one.

EWMA and Ledoit-Wolf shrinkage covariance, three scenario engines (GBM,
fat-tailed Student-t, historical bootstrap), VaR and CVaR estimation,
constrained efficient-frontier optimisation, and a walk-forward backtest against
an equal-weight benchmark that charges turnover and transaction costs.

`NumPy · pandas · SciPy · yfinance`

### [imc-prosperity-4-trading-strategies](https://github.com/MuhammadxKhan/imc-prosperity-4-trading-strategies)

Relative-value strategy for Round 5 of IMC Prosperity 4, contributing to a
**top 1% global team score**.

Ten product families of five instruments each, treated as common movement plus
residual. The strategy prices each instrument off its family mean, trades only
the residual past a per-product threshold, and holds inventory inside the band
rather than forcing a flat exit. Fair-value offsets are calibrated rather than a
live EMA — validation showed the adaptive version drifted toward bad prices and
weakened the signal.

**Also:** a computer algebra system in C# — custom parser, symbolic
differentiation and integration — and a macro-regime portfolio simulator in
Python covering crisis shocks, leverage constraints, transaction costs and risk
limits.

---

## Tools

Python (NumPy, pandas, SciPy, scikit-learn, PyTorch, matplotlib) · C# · C/C++ · SQL · R · JavaScript
Git · Jupyter · LaTeX

## Contact

muhammad.khan.quant@gmail.com
