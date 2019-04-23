## Chart Pattern Recognition
### Identifying stock chart patterns and evaluating predicted trade outcomes

This feature engineering example involves a method for chart pattern recognition. Stemming from the idea that voice recognition is basically looking for patterns in waveforms, it seemed plausible that this could apply to normalized stock returns. This example uses closing price data for Microsoft from January 2000 to April 2018 (data from Quandl).

The following approach takes a rolling one-month window of price data, normalizes the data by converting it to cumulative percent returns over the period, and then stores the pattern. Next, it steps the window forward by one day and repeats the process to collect all possible historical patterns.

Then we can compare the current period’s pattern to historical patterns, extract those patterns similar to the current pattern, and use the mean outcome of those similar patterns as the basis for the buy or sell recommendation. This is shown by the dots on the right-hand side of the chart — the green and red dots are the outcomes of the historical patterns, the yellow dot is the mean of those outcomes, which is the recommendation, and the purple dot is the actual outcome of the current pattern being evaluated.

![My image](https://github.com/footfalcon/Chart_Pattern_Recognition/blob/master/images/chart.png)

Initial testing across about 200 patterns to evaluate predictive strength generated a 64% accuracy rate.

![My image](https://github.com/footfalcon/Chart_Pattern_Recognition/blob/master/images/table.png
)
