# Financial_Planning_for_Retirement

## Part 1 - Personal Finance Planner
In this section I created a personal finance planner application. In devloping the planner, I took into account the following assumptions:

The average household income for each member of the credit union is $12,000.

Every union member has a savings portfolio composed of cryptocurrencies, stocks and bonds:

The following amount of crypto assets: 1.2 BTC and 5.3 ETH.

The following amount of shares in stocks and bonds: 50 SPY (stocks) and 200 AGG (bonds).


Created two variables called my_btc and my_eth. Set them equal to 1.2 and 5.3, respectively.

Used the requests library to fetch the current price in US dollars (USD) of bitcoin (BTC) and ethereum (ETH). 

Parsed the API JSON response to select only the crypto prices and store each price in a variable.

Computed the portfolio value of cryptocurrencies and print the results.

Collected Investments Data Using Alpaca: SPY (stocks) and AGG (bonds)

Created two variables named my_agg and my_spy and set them equal to 200 and 50, respectively.

Set the Alpaca API key and secret key variables, then create the Alpaca API object using the tradeapi.REST function from the Alpaca SDK.

Formatted the current date as ISO format. 

Retrieved the current closing prices for SPY and AGG using Alpaca's get_bars() function. Transform the function's response to a Pandas DataFrame and preview the data.

Picked the SPY and AGG close prices from the Alpaca's get_bars() DataFrame response and store them as Python variables. Printed the closing values for validation.

Computed the value in dollars of the current amount of shares and print the results.

### Savings Health Analysis
In this section, I assessed the financial health of the credit union's members.

Created a variable called monthly_income and set its value to 12000.

Created a DataFrame called df_savings with two rows. Stored the total value in dollars of the crypto assets in the first row and the total value of the shares in the second row.


Used the df_savings DataFrame to plot a pie chart to visualize the composition of personal savings.

Used if conditional statements to validate if the current savings are enough for an emergency fund (3x monthly income). 

Based on calculations propmted one of three responses. 

If total savings are greater than the emergency fund, display a message congratulating the person for having enough money in this fund.

If total savings are equal to the emergency fund, display a message congratulating the person on reaching this financial goal.

If total savings are less than the emergency fund, display a message showing how many dollars away the person is from reaching the goal.

## Part 2 - Retirement Planning
In this section, I used the Alpaca API to fetch historical closing prices for a retirement portfolio and then used the MCForecastTools toolkit to create Monte Carlo simulations to project the portfolio performance at 30 years. 


### Monte Carlo Simulation
Used the Alpaca API to fetch five years historical closing prices for a traditional 40/60 portfolio using the SPY and AGG tickers to represent the 60% stocks (SPY) and 40% bonds (AGG) composition of the portfolio. Converted the API output to a DataFrame and previewed the output.


Configured and executed a Monte Carlo Simulation of 500 runs and 30 years for the 40/60 portfolio.

Plotted the simulation results and the probability distribution/confidence intervals.


### Retirement Analysis
Fetched the summary statistics from the Monte Carlo simulation results.

Given an initial investment of $20,000, calculated the expected portfolio return in dollars at the 95% lower and upper confidence intervals.

Calculated the expected portfolio return at the 95% lower and upper confidence intervals based on a 50% increase in the initial investment.

### Early Retirement

Tried adjusting the portfolio to either include more risk (a higher stock than bond ratio) or to have a larger initial investment and rerun the retirement analysis to see what it would take to retire in 5 or 10 years instead of 30! Ran simulations to get results. 
