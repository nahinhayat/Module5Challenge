Module 5 Challenge

In this program I analyzed the value of a portfolio which contained two different cryptocurrencies, stocks, and bonds. The prices in my analysis were pulled from an api for the cryptos and the stocks/bonds prices were pulled using the alpaca SDK. After finding these values I evalutaed if the portfolio was viable as an emergency fund and then using monte carlo simulations created forecasts for retirement. 

Details:

I imported these libraries first and called the load_dotenv(), then I created an .env file in the starter code file with my alpaca and secret alpaca key:
![screenshot1](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.09.38%20PM.png)

Then the first step to analyze the portfolio I pulled the current prices of bitcoin and ethereum using api endpoints and making requests. After making the requests I navigated the JSON response to the prices and stored them as variables:
![screenshot2](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.13.19%20PM.png)

![screenshot3](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.13.40%20PM.png)

It was simple math using the number of coins to find the value of the cryptos next:
![screenshot4](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.15.33%20PM.png)

Moving on to the stocks and bonds, to use the SDK I created variables for my keys and created a REST object:
![screenshot5](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.23.59%20PM.png)

To finding the closing prices, I set tickers, timeframe, and dates to use with the get_bars function and then concatenated the tickers into one dataframe:
![screenshot6](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.30.45%20PM.png)

After some math we can find the value of the stocks/bonds portion of the portfolio:
![screenshot7](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.33.15%20PM.png)

Next I visualized the portfolio using a pie chart:
![screenshot8](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.33.56%20PM.png)

After pulling the data for the last three years of the stocks/bonds closing prices I ran a Monte Carlo simulation for 30 years 500 times and visualized it:
![screenshot9](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.36.16%20PM.png)

Then using 95% confidence intervals we found the range in which the portfolio could be in:
![screenshot10](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.37.13%20PM.png)

This was all done again for a ten year simulation:
![screenshot11](https://github.com/nahinhayat/Module5Challenge/blob/main/Starter_Code%205/screenshotsmodule5challenge/Screen%20Shot%202023-03-22%20at%209.37.49%20PM.png)

Author

Nahin Hayat https://www.linkedin.com/in/nahinhayat/