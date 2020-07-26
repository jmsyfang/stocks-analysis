# stocks-analysis
Module 2: VBA

## Overview of Project

The purpose of this project is to help Steve sort through a large amount of stock data, centered around volume and starting/ending prices. We are evaluating the performance of the green stock DQ against the rest of the data, and building a macro that can help him easily digest the data given a year input.
## Results

We began with source code that would loop through the dataset and compare to each ticker we are interested in for matches. If there is a match, it records data (volume, price) otherwise it moves to the next entry. Once the data table has been scanned, it moves to the next ticker. We refactored the process so that it looks at the table once, and once we have identified the ending price (last entry for a ticker) it moves on to the next ticker to compare to.

From the results, you can see DQ did fine in 2017 but did not perform well in 2018 (most of the tickers we look at performed poorly in 2018) With only 2 years of data, we can get an average return, which DQ is actually doing fine in (due to 2017 results). However, given that it's a retirement fund, a less volatile stock would be more beneficial even at the cost of lower expected return. RUN has similar return with  postive returns in 2017 and 2018.

2018 results
https://github.com/jmsyfang/stocks-analysis/blob/master/2018.png

2017 results
https://github.com/jmsyfang/stocks-analysis/blob/master/Annotation%202020-07-26%20094254.png



## Summary


Refactoring lowers the amount of code fabrication needed, as an existing body of work can be modified. Also, it implicity forces you to think about how you plan to build the code and whether any previous projects are similar enough to be refactored. However, it can be frustrating or even a detriment of time/effort to refactor code if you aren't open to other ideas that could ha ve a better runtime/performance, hwich is why you need to think about process and your experiences while being agnostic to any direct route at the beginning.

Refactoring did improve the speed of the process though. Without refactoring, it took aprox 14 seconds and the PC was locked up, while after refactoring it took a few seconds and the PC can be used during analysis. Unfortunately, because of how our code works, the data and list of tickers are interested in have to be in alphabetic order (or some sort of order that follows each other). This is because we are looping through the table only once, so we have to be sure when we move to the next ticker there is no way any previous part of the table could have matching data

