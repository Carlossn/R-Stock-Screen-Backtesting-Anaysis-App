# R Shiny App for Stock Screen Backtesting Anaysis App
R Shiny app created to analyze stock returns from a specific stock screen data input. 

## Purpose
Analyze data from my proprietary backtesting stock screen "Wounded Wolves" backtested stock screen based on turnaround stories. 
This app allows to understand much better the downside risk of turnaround picks as this a very risky deep-value stock screening criteria.

## User Input
Users need to enter the same input per column as in the csv file. I used Bloomberg "total return" excel blp fields to obtain total absolute and alpha returns for different investment horizons for the "Wounded Wolves" stock screen.

## CSV File columns required
**name:** stock name
**ticker:** stock ticker
**sector:** GICS Sector name
**industry:** GICS Industry name
**cyclicality:** proprietary index (1 to 5) to measure cyclicality (the higher number, the more cyclical)
**rel_index:** stock-related local broad index (Bloomberg field)
**start_date:** dd/mm/yyyy when the stock entered the portfolio
**tr_0.5y**: total absolute return for the first 6 months. The other "tr_xxy" columns read similar but changing the holding period.
**alpha_0.5y**: total abnormal return vs local benchmark for the first 6 months. The other "alpha_xxy" columns read similar but changing the holding period.
**tr_an_0.5y**: total absolute return annualised for the first 6 months. The other "tr_an_xxy" columns read similar but changing the holding period.
**alpha_an_0.5y**: total annualised abnormal return vs local benchmark for the first 6 months. The other "alpha_an_xxy" columns read similar but changing the holding period.

## Notes:
- In the example ("Wounded Wolves") stock screening is a deep value screen that is meant to screen candidates for the long term/
- For this reason, the app measures a stock performance during different holding period, including even those where the stock no longer is screened by the criteria. 
- If the user wants to work with a more short-term minded stock screening criteria and wants to measure peformance only for those periods where a particular stock is screened, it shall add another column "exit_date" and change the code.



