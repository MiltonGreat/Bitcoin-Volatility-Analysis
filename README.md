# Volatility Modeling and Risk Assessment using GARCH Models

![screenshot-localhost_8888-2025 03 30-12_01_42](https://github.com/user-attachments/assets/f82db776-8afa-4636-b1e1-6124f9ea96bd)

## Project Overview

This project aims to analyze price fluctuations and financial risk using GARCH family models. By implementing GARCH(1,1), EGARCH(1,1), and GJR-GARCH(1,1), we estimate volatility dynamics and assess risk exposure through Value at Risk (VaR) analysis.

### Dataset

The dataset contains Bitcoin price data at 1-minute intervals (high-frequency data). The columns include:

- **Timestamp:** Unix timestamp (epoch time).
- **Open:** The price at the start of the minute.
- **High:** The highest price reached during the minute.
- **Low:** The lowest price reached during the minute.
- **Close:** The final price at the end of the minute.
- **Volume:** The number of Bitcoins traded during that minute.
- **datetime:** A converted, human-readable timestamp.

The dataset starts at January 1, 2012 and contains data points up to at least January 3, 2012.

### Methodology

1. Stationarity Check:
- Used the Augmented Dickey-Fuller (ADF) test to ensure the time series is stationary.

2. Model Implementation:
- Applied GARCH(1,1), EGARCH(1,1), and GJR-GARCH(1,1) to capture volatility clustering.
- Used Maximum Likelihood Estimation (MLE) for model parameter estimation.
- Compared models using Akaike Information Criterion (AIC) and Bayesian Information Criterion (BIC).

3. Volatility Forecasting:
- Predicted future annualized volatility based on the fitted models.

4. Risk Analysis (VaR Calculation):
- Assessed risk exposure by calculating VaR breaches to evaluate model performance.

### Key Findings

- EGARCH(1,1) performed best (lowest AIC & BIC), confirming the presence of asymmetric volatility in price movements.
- The volatility forecasts suggest high market fluctuations, requiring further validation.
- VaR breaches (95.45%) indicate risk underestimation, implying the need for improved risk modeling.

### Future Improvements

- Use heavy-tailed distributions (e.g., Student’s t) for better volatility modeling.
- Explore deep learning-based volatility forecasting (e.g., LSTMs).
- Implement regime-switching GARCH models to capture structural changes in volatility.

### Source

![Bitcoin Historical Data from Kaggle](https://www.kaggle.com/datasets/mczielinski/bitcoin-historical-data)
