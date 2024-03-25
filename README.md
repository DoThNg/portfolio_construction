## Construct investment portfolios based on PE and PB ratios

---
### Disclaimers
This small research is not an investment advice and should not be relied upon in any investment decisions. Please be also noted that past performance information is given for illustrative purposes only, and it is not an indication of future performance. In conducting this research, many factors (e.g., transaction fees, capital gain tax, survivorship bias, investment risks, etc.)  have not been taken into account and it will, therefore, not be applicable to an individual's objectives or financial situation.

### Introduction
This is an experiment and a small research on performances of investment portoflios from 2020 to 2023, constructed by stock selections from Australian stock universe and based on rankings of **PE** or **PB** ratios among stocks.

The investment universe used in this research contains 100 companies which have the largest market capitalization at the time when the list of ASX Listed Companies was downloaded (The list, containing 2001 companies was downloaded on 14 March 2024 at ASX website - [Link](https://www.asx.com.au/markets/trade-our-cash-market/directory)

The research and experiment were run on Google Colab, and the financial and price data derive from Yahoo Finance.  

## Methodology for Portfolio Construction
The steps to build the PE-based and PB-based portfolios in this research are as follows:
- **Step 1**: ranking companies by market capitalization in the downloaded list of ASX Listed Companies. The top 100 companies will be selected for the [investment universe]().
- **Step 2**: running the [portfolio_construction.ipynb]() on Google Colab (Please also store the [investment universe file]() on Google Colab).
    
    - Data on financials (Diluted EPS and Tangible Book Value) and stock prices will be downloaded from Yahoo Finance, using yfinance library. (**Note**: the stock prices were downloaded from the 1st to the 7th of September from 2019 to 2023 - and the reasoning for this is to ensure when PE and PB ratios are computed, most companies in ASX release their full-year results, so the ratios will best reflect these results)  
    - PE and PB ratios for 100 companies will be computed based on the downloaded data (In this research, since 2019 data was not available, the portfolio will be only selected in 2020, 2021, and 2022).
    - Filter out all negative PE and PB, and select 10 companies (each represents 10% of investment portfolio value) with the lowest PE and PB ratio in each investment year.
    - 10 companies selected in each investment year will form the portfolio investment in that year - This also means the rebalancing period of portfolio is annual).    

- **Step 3**: Computing the PE-based and PB-based portfolio performances and comparing with index performances (S&P/ASX 100, S&P/ASX 200, and All Ordinaries) over 2020-2023 period. 

Summary of portfolio performances in this research are as follows:

[Portfolio_performance]()


| Portfolio       | 2020-2023 CAGR |
| --------------- | -------------  |
| PE-based        | 29.01%         |
| PB-based        | 37.43%         |
| S&P/ASX 100     | 7.33%          |
| S&P/ASX 200     | 6.64%          |
| All Ordinaries  | 6.54%          |


[Portfolio_overview]()