# Cryptocurrency Price Prediction with Sentiment Analysis

This repository contains a collection of notebooks and scripts aimed at predicting cryptocurrency prices using both historical data and sentiment analysis from multiple sources, including news, Google Trends, Tweets, Reddit, and Wikipedia.

## Project Structure

- **Data_Collection.ipynb**  
  This notebook handles the collection of cryptocurrency price data, focusing on Bitcoin, Ethereum, and Litecoin. Data is fetched daily and updated regularly to ensure accurate and up-to-date predictions.

- **Data_Source_Identification.ipynb**  
  This notebook focuses on identifying and collecting price data for cryptocurrencies. It leverages the `Historic-Crypto` API to gather features such as `low`, `high`, `open`, `close`, and `volume` on a daily basis. Data is updated hourly due to API limitations.

- **Data_Updating.ipynb**  
  This notebook automates the process of updating cryptocurrency prices. It ensures that data is refreshed every 5-6 hours to keep the prediction models well-informed.

- **Price_Prediction.ipynb**  
  This notebook implements the model to predict cryptocurrency prices. It integrates historical price data along with features derived from sentiment analysis on news and social trends.

## Data Sources

- **Cryptocurrency Prices**  
  Historical data for Bitcoin, Ethereum, and Litecoin is fetched using the `Historic-Crypto` API. The key features used for analysis are:
  - `Low`: The lowest price of the cryptocurrency within a specific time period.
  - `High`: The highest price of the cryptocurrency within a specific time period.
  - `Open`: The price at the beginning of a specific time period.
  - `Close`: The price at the end of a specific time period.
  - `Volume`: The total amount of cryptocurrency traded during the given timeframe.

- **Sentiment Data**  
  Price movements in cryptocurrencies are not just driven by historical data but also by public sentiment. The following sources of text data are used for sentiment analysis:
  - News articles
  - Google Trends
  - Tweets
  - Reddit posts
  - Wikipedia updates

  By analyzing the sentiment from these sources, we aim to add new features to the dataset that reflect the influence of public opinion on cryptocurrency prices.

## Implementation Details

- **Data Update Frequency**  
  As the `SerpAPI` only provides data for the past 7 days, data must be updated every 5-6 hours to ensure the most recent information is available.

## Requirements

- `pandas`
- `numpy`
- `Historic-Crypto`
- `SerpAPI`
- `nltk` (for sentiment analysis)
- `scikit-learn` (for building predictive models)
