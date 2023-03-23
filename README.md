Module 5 Challenge

In this program I analyzed the value of a portfolio which contained two different cryptocurrencies, stocks, and bonds. The prices in my analysis were pulled from an api for the cryptos and the stocks/bonds prices were pulled using the alpaca SDK. After finding these values I evalutaed if the portfolio was viable as an emergency fund and then using monte carlo simulations created forecasts for retirement. 

Details:

I imported these libraries first and called the load_dotenv(), then I created an .env file in the starter code file with my alpaca and secret alpaca key:


Then the first step to analyze the portfolio I pulled the current prices of bitcoin and ethereum using api endpoints and making requests. After making the requests I navigated the JSON response to the prices and stored them as variables:

It was simple math using the number of coins to find the value of the cryptos next:

Moving on to the stocks and bonds, to use the SDK I created variables for my keys and created a REST object:

To finding the closing prices, I set tickers, timeframe, and dates to use with the get_bars function and then concatenated the tickers into one dataframe:

After some math we can find the value of the stocks/bonds portion of the portfolio:

Next I visualized the portfolio using a pie chart:

After pulling the data for the last three years of the stocks/bonds closing prices I ran a Monte Carlo simulation for 30 years 500 times and visualized it:

Then using 95% confidence intervals we found the range in which the portfolio could be in:

This was all done again for a ten year simulation:

