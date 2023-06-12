# scr2
Signs of Consecutive Returns

# Introduction

Signs of Consecutive Returns (scr) is a collection of five functions that are designed to analyse several aspects of stock market behaviour.
The highlight of this package is being able to identify consecutive returns of the same sign that can help you analyse the historical patterns of a specific stock over a selected time horizon. 

The functions contained in the package are tools that offer a deeper understanding of a stock's historical volatility and provide insights on future trends.


# Installation instructions

The package is available on GitHub and can be installed using the remotes library with the following command:

remotes::install_github("https://github.com/marazf/scr2")

The "devtools" package from CRAN is necessary to install this package and can be installed with:

install.packages("devtools")

# Dependencies

scr makes use of $quantmod$, $xts$ and $zoo$, which are available on CRAN and can be installed with
install.packages().

# The functions

## count_last_consecutive_signs()

The count_last_consecutive_signs() function calculates the absolute number of the latest consecutive returns, either positive or negative, for a specific stock over a specified time frame.

The function accepts the following parameters:

- ticker: This is the ticker symbol for a stock.

- start and end: These parameters set the time frame for the analysis. The function will only consider returns within this period.

- frequency: This parameter allows to specify the frequency of returns. For example, if you set frequency = "daily", the function will consider daily returns.

## number_consecutive_returns()

The number_consecutive_returns() function is designed to calculate and return the absolute number of n consecutive positive or negative returns for a specific stock, represented by its ticker symbol, within a defined time horizon.

The function accepts the following parameters:

- n: This parameter represents the number of consecutive returns of interest. For example, if n = 3, the function will look for occurrences where the stock had 3 consecutive positive or negative returns.

- ticker: This is the ticker symbol of a stock of your choice.

- start and end: These parameters define the time horizon for the analysis. The function will only consider returns that occurred between these dates.

- frequency: This parameter represents the frequency of returns that should be considered. For instance, if frequency = "daily", the function will consider daily returns.

- positive: This parameter determines whether the function should count positive or negative returns. If positive = TRUE, the function will count consecutive positive returns; if positive = FALSE, it will count consecutive negative returns.

## prices_consecutive_returns()

The prices_consecutive_returns() function returns rounded stock prices associated with instances where n consecutive positive or negative returns occurred for a specific stock within a defined time frame.

The function accepts the following parameters:

- n: This parameter defines the number of consecutive returns of interest. For example, setting n = 3 will prompt the function to identify occurrences where the selected stock had 3 consecutive positive or negative returns.

- ticker: This is the ticker symbol of a stock of your choice.

- start and end: These parameters set the time horizon for the analysis. The function will only consider returns that fell within this time-frame.

- frequency: This parameter lets you set the frequency of returns that should be taken into account. For instance, with frequency = "daily", the function will consider daily returns.

- positive: This parameter determines whether the function should consider positive or negative returns. Setting positive = TRUE will cause the function to look for instances of consecutive positive returns, whereas positive = FALSE will make it look for instances of consecutive negative returns.

## probability_consecutive_returns_change()

The probability_consecutive_returns_change() function is designed to calculate the historical probability of experiencing a change of sign after n consecutive positive or negative returns for a specified stock within a given time frame.

The function accepts the following parameters:

- n: This parameter represents the number of consecutive returns of interest. For example, if n = 3, the function will compute the historical probability of the selected stock experiencing a change of sign after 3 consecutive positive or negative returns.

- ticker: This is the ticker symbol of a stock of your choice.

- start and end: These parameters set the time horizon for your analysis. The function will only consider returns that happened within this time period.

- frequency: This parameter represents the frequency of returns that should be considered. For example, if frequency = "daily", the function will calculate the probability based on daily returns.

- positive: This parameter determines whether the function should consider positive or negative returns. If positive = TRUE, the function will compute the probability of a sign change after consecutive positive returns; if positive = FALSE, it will compute the probability of a sign change after consecutive negative returns.

## probability_consecutive_returns()

The function probability_consecutive_returns() provides the historical probability of experiencing n consecutive positive or negative returns for a specified stock within a given time frame.

The function accepts the following parameters:

- n: This represents the number of consecutive returns of interest. For example, if you set n = 3, the function will compute the historical probability of the selected stock experiencing 3 consecutive positive or negative returns.

- ticker: This is the ticker symbol of a stock of your choice.

- start and end: These define the time period for the analysis. The function will only consider returns that occurred between these dates.

- frequency: This parameter represents the frequency of returns to consider. For example, if frequency = "daily", the function will compute the probability based on daily returns.

- positive: This parameter determines whether the function should consider positive or negative returns. If positive = TRUE, the function will compute the probability of consecutive positive returns; if positive = FALSE, it will compute the probability of consecutive negative returns.


