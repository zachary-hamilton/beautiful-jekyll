---
layout: post
title: Are Stocks Fair Coins?
image: /img/scrooge.png
---

According to the Efficient Market Hypothesis, the stock market is “efficient” and all relevant information is already incorporated into a stock’s price. This leads to the random walk hypothesis in which it is impossible to know whether a stock’s price will go up or down. One of the most prominent supporters of the random walk hypothesis is Burton Malkiel.
![alt text](/img/firstmalkielquote.png)
Burton Malkiel decided to test the random walk hypothesis by performing a series of coin flips. A head was considered a gain and landing on tails was considered a loss. He then charted the series of results as if they were stock returns. He then showed this chart of coin flips to a technical analyst or “chartist” who proclaimed he should buy the stock immediately. Malkiel then determined that “ this indicates that the market and stocks could be just as random as flipping a coin.”

I decided to repeat the same test as Malkiel but in reverse. Instead of taking a coin and making it look like a stock, I took stocks and made them look like coins. In order to accomplish this I put together a data set consisting of daily returns of stocks currently in the S&P 500 for the last 20 years. This resulted in over 2.3 million observations. I then encoded all of the gains as a 1 for heads and 0 for tails. A fair coin is one that is just as likely to land on heads as it is tails.

It turns out that the stock returns landed on “heads” 50.265% of the time. At first glance you might assume that that is pretty close to an even 50/50 split but a baseline test for a computer generated fair coin with the same number of observations as our data set landed on heads 50.019% of the time.

A t-test used to determine if the average of our data set was indeed .5 produced a p-value with 15 leading zeros. We could therefore reject the hypothesis that stocks are fair coins. But does that mean that Malkiel is wrong about stocks?

Absolutely not! The chart he produced from coin flips was of a single stock so it is necessary for us to separate out and test the individual stocks. By testing all the stocks in the S&P 500 at the same, we were essentially diversifying and “buying the index” of which Malkiel himself is a huge fan. He was even a director of Vanguard, one of the biggest champions of indexing, for 28 years!

I then performed a t-test at the individual stock level which showed that about 70% of stocks are fair coins.

This is much more conclusive than the first simple test showed but I felt that the percentage of stocks which are fair coins was still too low. Since it is rare for active managers to hold every stock for a 20 year period, it would be much more enlightening to look at this data over a shorter time horizon so I then tested the daily returns after separating them by both stock and year. The roughly 10,000 t-tests produced the following:

This shows that individual stocks act like a fair coin almost 90% of the time when aggregated by year! I would expect the percentage of stocks which are “fair coins” to increase as the unit of time used to aggregate them increases. A follow up to this analysis is to aggregate the data by month, day or even hour.

A caveat of this analysis is that even if you know for a fact that a stock is not a fair coin, this does not mean that you know if it will a gain or a loss.

In conclusion, Malkiel is right about the random walk hypothesis and individual stocks can be compared to coin flips. Perhaps the most surprising insight from this has been the unexpected support for diversification.
