# CRM-CW1: Segmenting S&P 500 stocks using weekly returns, beta and adapted RFM

6BUIS017W CRM & CM with Business Intelligence - Individual Coursework

## Abstract
A business intelligence analysis of the stocks that make up the S&P 500. The stocks have been represented using return and risk metrics (weekly mean returns and weekly beta), and using adapted RFM metrics (Recency, Frequency and Monetary) for trading activity. 
Using Ward and K-Means clustering on the stocks that are clustered on these metrics. 
Then, carrying out analysis in relation to correlation with RFM, and the sensitivity to removing the Monetary metric.

## Project Details
- Data snapshot (CSV files) retrieved 2026-11-20 03:19 UTC. The notebook was rerun on 2026-11-22 00:42 UTC and reproduced the same 488 shares and results
- Data period: 2021-01-01 to 2025-01-01 (exclusive end date)
- Observation date: 2024-12-31
- Index used: ^GSPC (S&P 500 price index)
- Data retrieved from yfinance
- Ticker information retrieved from wikipedia
- Date retrieved can be found in 'SP500_tickers.csv'
- Weekly returns are calculated using complete weeks that end on Fridays. 'Adj Close' is used and there are 207 complete weeks of data
- After data cleaning, there were 488 stocks remaining
- Removed tickers can be found in 'exclusion_log.csv'. This includes the first data date is available and number of missing trading days
- K-means and Ward clustering was used. Both used standardised data. K-means : n_init = 10 and random_state = 42. Ward: used Euclidean distance.
- For monetary, log1p transformation was applied.
- k was tested from 2 to 8
- Python version: 3.13
- numpy used: 2.4.6
- pandas used: 2.2.3
- yfinance used: 0.2.66

## Files
File | Description
--- | ---
SP500_RFM_Analysis_2021_2024.ipynb | Stores all the code and outputs from Tasks 1 & 2. Carried out using Google Colab
SP500_RFM_2021_2024.csv | Feature table
SP500_RFM_2021_2024.xlsx | Excel version of the feature table
SP500_close.csv | Daily closing prices
SP500_cluster_assignments.csv | Cluster assignments 
SP500_prices.csv | Daily prices
SP500_tickers.csv | Contains the tickers for S&P 500
SP500_volume.csv | Daily volume
exclusion_log.csv | Removed tickers with the first data date and number of missing trading days
figure_crm_cw | Charts used in the report

## How to run
Open the notebook and select run all. The notebook downloads live data from Wikipedia and Yahoo Finance, so results may vary if Yahoo revises its data. Saved CSV files are the snapshot used in the report
