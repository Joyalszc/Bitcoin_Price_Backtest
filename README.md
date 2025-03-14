# Bitcoin_Price_Backtest

In this project, I’m showing some basics of how to backtest Bitcoin data in Excel in order to understand the market, find trends and to place smarter orders.

We are taking 1 year (06-03-2024 to 06-03-2025) historic data of Bitcoin from coinmarketcap. We do the test once in every month to understand the market movement.

The downloaded csv file is imported to excel, and we clean the data. We remove all the columns except Date, Open, High, Low, Close, Volume and Marketcap.
	
We now created few more columns to do our calculations. 

The first one if ‘Diff’ were we find the difference between the Close price and Open price. 

Gain Loss -> (Close price by Open price)-1, we calculate this in percentage.

Previous Day Gain Loss -> Gain Loss value of the previous day.

Previous 7 Day Average -> By calculating the average of previous 7 days price.

Previous 7 Day Average by Close Price -> Calculating the Previous 7 days average by Close price. ( Previous 7 days average/Close Price)-1. We calculate this in percentage.

Volume Change -> We check the difference of last 2 volume.

Test Gain Loss -> We set a filter on Gain Loss column.

Now we do the test; 
First we the check the average of gain loss. Now we add a filter on previous day. Add a condition, is greater than 0.1. Check the total columns filtered under this. We can figure out that the ’n’ number of columns had 10% or more big gain. Now we compare the gain loss and previous day gain on filter. In the same way we check 15% and 20% gain.

To check Loss, add a custom filter ‘is less than 0.1’, which displays less than 10% gain. Check the gain loss average. In the same way add filter and try calculating the percentage increment or decrement, calculate the average of gain loss in sorted columns. We can also play on with the volume flow and calculate the trend as well. 
This is a simple back test method. We can try this on any cryptocurrencies.
