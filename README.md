# Indian Startup Funding EDA ( 2015 - 2020 ) 

### Project Overview:

Indian startup ecosystem is expanding and many innovative startups are coming up in the country. This has caught the eye of the investors and VCs. This project explores the Indian Startup Fundings over the last 5 years and draw insights from the collected data.

<p align="center"><img src="https://stvp-static-prod.s3.amazonaws.com/uploads/sites/2/2018/04/startup_funding_2-960x540.jpg"/></p>

### Resources Used:
- **Python Version:** 3.7
- **Packages:** pandas,numpy,sklear,matplotlib, bokeh

### Data Source: https://trak.in/india-startup-funding-investment-2015/

- We have details of 3044 funding details from 2015-2020
- The data needs to be cleaned properly for our analysis 

### Data Cleaning: 
- **'Date' columns** has few dates in the wrong format with missing '/' or contains '//', '.' 
- **'Amount in USD'** has funding amount as numbers as text. We need to convert it into numerical format for our analysis. 
- Other categorical columns have missing values as 'nan' or 'undisclosed'. Also, many rows contain characters like "\\\\xc2\\\\xa0". We need to clean these strings. 
- **'City Location'** column contains same states with different names like - Bangalore and Bengaluru. We need to treat them as same for our analysis. **'Industry Vertical'** column has similar issues
- Discrepancies in currency conversions. For example: According to [this news](https://yourstory.com/2019/08/startup-funding-bike-taxi-app-rapido-series-b-westbridge-capital#:~:text=Its%20valuation%20has%20now%20reached%20Rs%201%2C005%20crore.&text=Bengaluru%2Dbased%20bike%20taxi%20app%20Rapido%20has%20raised%20funding%20of,Limited%2C%20and%20a%20few%20others), Rapido actually got a funding of Rs. 391 crores and not USD 391 Billion. That means, it only got a funding of $51.7 

### EDA: 
Based on the analysis, we can observe following: 

1. Number of Fundings increased from 2016 to 2017 but since then there has been a steady decrease in the number of fundings.Though 2016 is the year with most number of funding deals, it is the year with the lowest sum 
![](https://github.com/yashica95/startup_funding/blob/master/images/overall_trend.png)
2. Flipkart and Paytm were the top startups to receive the highest funding till date. Flipkart got the maximum one-time funding of ~ $250 Billion in 2017 from Softbank in a Private Equity deal.
![](https://github.com/yashica95/startup_funding/blob/master/images/facebook%26paytm%20.png)
3. While 2016 had the most number of fundings, 2017 saw highest total funding received by indian startups. Since then the trend has been downward.
4. Consumer Internet tops the most number of Fundings received whereas E-commerce industry saw the highest total funding amount received to date.
5. Bengaluru seems to be the top choice for startups and investors in India. But its popularity is on a decline now.
![](https://github.com/yashica95/startup_funding/blob/master/images/fundings_by_location.png)
6. Seed Funding is the most common type of funding, followed by Private Equity. Other funding deals like Debt Funding, Series A,B and C form only ~2.5% of all deals. This suggest most startups in India are quite young. 
![](https://github.com/yashica95/startup_funding/blob/master/images/investment_types.png)


### Major Drawbacks:
1. The data misses many startups fundings like - [Swiggy raised 1 Billion(USD)](https://techcrunch.com/2018/12/20/swiggy-raises-1-billion/) and some of the funding deals were 'Undisclosed' and therefore,we didn't have exact funding amount for few funding deals. Hence, our insights might be incorrect.
2. Similar to Rapido's amount, the funding amount noted can be wrong because of not taking currency conversions in account.

