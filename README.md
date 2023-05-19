![](https://github.com/FilippoGuardassoni/uk_house_market/blob/main/img/headerheader.jpg)

# Housing Market, Money, and the Effect of Monetary Policy in UK

![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/pragyy/datascience-readme-template?include_prereleases)
![GitHub last commit](https://img.shields.io/github/last-commit/FilippoGuardassoni/spotify_hitsong)
![GitHub pull requests](https://img.shields.io/github/issues-pr/FilippoGuardassoni/spotify_hitsong)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![contributors](https://img.shields.io/github/contributors/FilippoGuardassoni/spotify_hitsong) 
![codesize](https://img.shields.io/github/languages/code-size/FilippoGuardassoni/spotify_hitsong)

# Project Overview

When people buy or sell houses, either to live in or as an investment, we refer to this as the housing market. A house is the most valuable thing many people will ever own. The house market is one of the biggest in any developed country and therefore one of the most impactful.
Previous studies had been conducted using the different models and variables, however, to our knowledge at the moment, none has considered the best theoretical approach to the inherent structure of the data. In fact, most models we based on our research used mostly VAR models. The purpose of this study is to in- vestigate key aspects of the UK house market. Our main objective is to understand the relationship be- tween the house prices and the monetary policy. This is done using quarterly data from 1975 to 2020 and developing a time series Vector Error Correction Model. This approach allows us to distinguish between statistical correlation and economic causation.
From our final model, we find that the effect of a GDP on house prices is large, and the monetary policy shock is existent but not so relevant in the short-medium period while it increases in the long run but not as much as we would have expected. Shocks to the CPI and the interest rate are in turn found to have signifi- cant effects on house prices.
Due to the large confidence bands of the impulse responses this result is, however, in general not statistically significant. Further research should be conducted in order to better understand the effect of a market targeting monetary policy used to mitigate the economic uncertainty and unbalances.


# Installation and Setup

## Codes and Resources Used
- EViews 11

# Data
We have collected data in the form of Time Series at UK level from Federal Reserve Bank of St. Louis, Bank of England and Nationwide quarterly from year 1975 to 2020.

## Sales
The variables collected are the following:

- Real GDP
- Unemployment Rate
- Fixed Mortgage Rate
- Euro Interbank Rate
- Interbank Rate (3 months)
- Population

We considered different interest rates. The Fixed Mortgage Rate describes the interest rate of a fully amortizing mortgage loan from banks which remains the same throughout the term of the loan. The Euro Interbank Rate which describes the interest rate at which the banks lend and borrow money from other banks in the euro zone. Finally, the interbank rate describes the interest rate at which the banks lend and borrow money from other banks in UK (dealing with quarterly data, we opted for 3-months period rate).
From the graphs we can see that GDP drops down steeply in 2020 which is clearly due to uncertainty caused by the economic shocks, namely Covid-19 & Brexit. Interbank Rate & Euro Interbank Rate have decreased during the time 2015 – 2020. The unemployment rate has also increased during the year 2020.

## Indexes
We collected data as:

- House Price Index
- CPI (Consumer Price Index)
- Economic Uncertainty Policy Index (EPUI)

Nationwide is one of UK’s largest mortgage providers and has the longest unbroken run of house price data from 1952 on quarterly basis. Even though actual data would be better, the indexes serve as a good proxy. As you can see from the graph, it is the case of the House Price Index, which captures very well the instability of the economy.

## Source Data & Data Acquisition
The dataset can be reconstructed downloading data from Federal Reserve Bank of St. Louis, Bank of England and Nationwide.

## Data Pre-processing
The dataset has both continuous and discrete (sex and sports) variables. As the continuous variables were measured and expressed with different value scales, standardization with the scale function is applied in order to correctly learn about the variable interactions. This function centered the dataset with mean approximately 0 and standard deviation 1. The dataset was already prepared to work on it without missing data and outliers.


# Project structure
```bash
├── dataset
│   ├── CFQB3RT  Bank of England  Database.xlsx
│   ├── GBRCPIALLQINMEI.xls
│   ├── dataset.csv
│   ├── hpimonthlyandqtlytables1to19.xls
│   ├── series-230621.csv
│   ├── series-230621.xls
├── report
│   ├── uk_house _market_report.pdf
├── img
│   ├── headerheader.jpg      
├── LICENSE
└── README.md
```

# Results and evaluation
As per the results obtained from Cointegration Test, we chose to use Vector Correction Model. From Johansen Test we found that the rank is 8 which implies that 8 cointegrating equations are present in the model. For the sake of interpretability, we performed the VECM with 1 cointegrated equation. Through Johansen Nor- malization Restriction, we can infer the long run relationship between the independent variables and the home price index. The most unexpected results from our model were that GDP was not significant as well as the CPI, the Fixed Mortgage Rate and the Population. All the other variables were significant. In particular, the interbank rate and the euro interbank rate affect positively the home prices in the long run.


# Future work
An ideal model to understand the impact of exogeneous variable on Housing market would include a series of variables that we omitted. For example, a dummy variable could help to capture the crises effect. We performed our analysis considering the general landscape of the UK Housing Market. An improved version should divide the Housing Market into the owner-occupied market and rental market in addition to considering the regional
analysis. Another limitation of our model was the use of Housing Price Index instead of actual values. Lastly, to be more accurate, discretionary income, which is the money that an individual or a family has to invest, save, or spend after taxes and necessities are paid, would be a better variable to predict the sales trend.


# Acknowledgments/References
See report/song_hit_prediction.pdf for references.

# License
For this github repository, the License used is [MIT License](https://opensource.org/license/mit/).
