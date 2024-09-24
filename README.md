# Stock Market Prediction using Natural Language Processing

## Overview
This project uses Machine Learning and Natural Language Processing (NLP) to predict stock market trends by analyzing historical stock data and global news. The model autonomously buys and sells stocks based on its predictions, with no human intervention. By leveraging NLP techniques, the model aims to make more informed trading decisions based on the sentiment of current events and news articles. The primary goal is to increase the accuracy of stock market predictions through sentiment analysis and probability-based decision-making.

## Introduction
Natural Language Processing (NLP) enables computers to analyze, understand, and derive meaning from human language. In this project, I applied NLP techniques to evaluate stock market data and global news to predict stock trends.

A core component of this project is **Sentiment Analysis**, which assesses the sentiment of news headlines—whether they are positive, neutral, or negative—and determines their influence on stock prices. The project's hypothesis is that news sentiment directly correlates with stock price movements. Sentiment analysis provides an "emotional" understanding of the data, helping us gauge whether a stock is likely to rise or fall based on external factors.

## Data Collection & Preprocessing
I used the **Combined_News_DJIA.csv** dataset, which spans from 2008 to 2016 (courtesy of Aaron7sun, Kaggle). I extended this dataset to cover the period from 2000 to 2008 using news data collected from The Guardian's Restful News API. The extended dataset includes the 25 most popular headlines for each day, alongside stock data for the **Dow Jones Industrial Average (DJIA)**, which was sourced from Yahoo Finance.

- **News Data**: Historical headlines from Reddit’s World News Channel (top 25 headlines per day).
- **Stock Data**: DJIA data for the same period used to label the news data (rise = 1, fall = 0).

The combined dataset is used to predict whether stock prices will rise or fall on a given day based on the sentiment of the previous day's headlines. Labels are applied as follows:
- **0**: Stock price declines or stays the same.
- **1**: Stock price rises.

### Data Cleaning
The raw data from news headlines was cleaned and preprocessed using **Python**:
1. **HTML Tags & Punctuation**: Removed all HTML tags and punctuation from the text.
2. **Stop Words**: Eliminated common words like "the", "is", and "and" that don’t contribute to the sentiment.
3. **Lowercase Conversion**: Converted all text to lowercase to standardize the data.

### Word Embeddings
To convert the text data into a numerical format suitable for machine learning models, I used **Word2Vec**—a model that maps words and phrases to vectors of real numbers. These word embeddings allow us to build training and testing datasets for model development. The cleaned and tokenized news headlines serve as the primary input for our prediction model.

## Machine Learning Model
The core of this project is a predictive model that uses past stock data and news sentiment to forecast stock trends. Our approach involves:
- **Training** the model on historical stock data and corresponding news sentiment.
- **Predicting** future stock movements based on the processed input data (headline sentiment).

The ultimate goal is to create an intelligent system capable of making profitable trading decisions without human input.

## Conclusion
This project demonstrates the potential of combining Natural Language Processing with financial data to predict stock market trends. By analyzing the sentiment of daily news headlines, the model aims to predict stock price movements with greater accuracy, offering a data-driven approach to stock market forecasting.

---

**Created with ❤️ by Kajal Mahajan**