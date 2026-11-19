# Bitcoin Market & Macroeconomic Analysis (2025–2026)

**Independent Research Project | Abrar Abdullah**

## Project Overview

Bitcoin is known for its volatility, and during the period I studied, its price fell about 30% while the S&P 500 rose about 15%. I wanted to understand whether Bitcoin's price movements are connected to the stock market and the broader economy, or whether it moves independently.

For this project, I looked at Bitcoin's relationship with the S&P 500, U.S. inflation, and Federal Reserve interest rates from October 2025 through September 2026.

I used Python in Google Colab to analyze historical financial data and test whether these factors had a measurable relationship with Bitcoin's returns.

## Research Question

How do macroeconomic conditions and traditional financial markets relate to Bitcoin's price movements?

I focused on three questions:

1. Are Bitcoin and S&P 500 daily returns positively correlated?
2. Are changes in the Effective Federal Funds Rate associated with Bitcoin's daily returns?
3. Is U.S. inflation associated with Bitcoin's monthly returns?

## Data & Methodology

I used historical Bitcoin price data from CoinGecko and macroeconomic data from the Federal Reserve Economic Data (FRED) database.

The datasets include:

- Bitcoin daily prices (`btc-usd-max.csv`)
- S&P 500 index prices (`SP500.csv`)
- Effective Federal Funds Rate (`DFF.csv`)
- Consumer Price Index (`CPIAUCSL.csv`)

I used Python to clean and organize the datasets, calculate returns and volatility, and examine correlations between Bitcoin and the other variables.

I also ran an Ordinary Least Squares (OLS) regression using S&P 500 daily returns to explain Bitcoin's daily returns. After running the regression, I checked the model's assumptions, tested how sensitive the results were to extreme observations, and compared its predictions against a simple historical-average baseline.

## Results & Findings

### Bitcoin and the S&P 500

The results showed a moderate positive relationship between Bitcoin and S&P 500 daily returns.

- Correlation: **0.47**
- R-squared: **0.22**
- Regression coefficient: **1.61**

The regression explained about 22% of the variation in Bitcoin's daily returns. This suggests that the stock market provides some useful information for understanding Bitcoin's movements, but most of the variation remained unexplained.

### Inflation and Interest Rates

The analysis found a moderate positive relationship between Bitcoin's monthly returns and the inflation measure, but the result was not statistically significant.

Daily changes in the Effective Federal Funds Rate showed almost no correlation with Bitcoin's daily returns.

These results suggest that Bitcoin's relationship with inflation and interest rates was less conclusive during the period I studied.

### Model Testing

I also tested the regression model using data outside the training sample to see how well it could predict Bitcoin's returns.

The model showed limited improvement compared with a simple historical-average baseline. Although the relationship between Bitcoin and the S&P 500 was statistically significant, the model was not reliable enough to use as a standalone trading strategy.

## Limitations

There are a few limitations to this analysis.

First, the research only covers October 2025 through September 2026, so the results may be different during other market conditions.

Second, Bitcoin trades 24/7, while the S&P 500 follows regular stock market trading hours. This creates some differences when comparing daily returns.

The inflation analysis also had only 11 monthly observations, and the Effective Federal Funds Rate rarely changed from day to day.

Finally, the analysis identifies relationships between variables, but it does not prove that changes in the stock market or the broader economy directly cause Bitcoin's price movements.

## Conclusion

This project found that Bitcoin's daily returns were partly connected to movements in the stock market during the period studied. However, the regression explained only about 22% of Bitcoin's daily return variation, and its predictive performance was limited.

Overall, this project helped me better understand how Bitcoin responds to broader financial markets and the risks that come with its volatility. It also gave me experience using Python to work with financial data, run statistical tests, and interpret the results.

## Repository Files

- `Bitcoin_Market_Macroeconomic_Analysis.ipynb` — Python notebook containing the analysis, calculations, and charts
- `Abrar Abdullah Bitcoin Macro Analysis.pdf` — Full research paper
- `btc-usd-max.csv` — Bitcoin historical data from CoinGecko
- `SP500.csv` — S&P 500 data from FRED
- `DFF.csv` — Effective Federal Funds Rate data from FRED
- `CPIAUCSL.csv` — Consumer Price Index data from FRED

## How to Run the Notebook

1. Download the Python notebook and the four CSV files.
2. Open the notebook in Google Colab.
3. Upload the four CSV files into the Colab session.
4. Run the notebook from top to bottom.

The notebook contains the Python calculations, regression results, statistical tests, and visualizations used in the research paper.

## Next Steps

There are a few areas I would like to explore further:

1. Test whether Bitcoin reacts to S&P 500 movements with a one-day lag.
2. Examine Bitcoin returns around Federal Reserve announcements.
3. Study how Bitcoin responds to CPI release dates and unexpected inflation results.

---

*This project is for educational and research purposes only and should not be considered financial advice.*
