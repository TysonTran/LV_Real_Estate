# Las Vegas Real Estate Portfolio Analysis

The main goal for investors is to grow their money over the long term. While the goal is to pick the best investments, there will always be some that out perform others. The main goal of this analysis is to perform a comparative analysis of two investment properties located in Las Vegas, Nevada and understand how they fare against each other. Also to understand how turnover affects a real estate investment.


### Facts:
#### Bright Leaf
 - Located in North Las Vegas
 - Purchase 1/2013
 - Purchase Price: 109k
 - Currently rented below market rent: $1,400
 - Assumed value: $395,900 - from Zillow
 - Rent raised between 3-5% each year
 - 1 turn over in 2019 but new tenant was old tenant's sister, so rent was not pushed to market rent
 
#### Fort Pike
 - Located in South West Las Vegas
 - Purchase 2/2013
 - Purchase Price: 187k
 - Currently rented at market rent: $2,149
 - Assumed value: $527,500 - from Zillow
 - Rent raised between 3-5% each year if tenant renewed
 - 3 turn overs in the period of 2015-2022 and each time rent was listed for market rent (2018, 2020, 2021)

#### How does a move out affect profit?
 - When the home is relisted, it is pushed up to market rent giving more income
 - Each move out requires cleaning and repairing the home for a new tenant
 - More expenses incurr because the time it takes to repair home and get it rerented out takes about a month
 - Also have to pay administrative fees to property management to find new tenants
 - New tenants usually have a lot of maintenance request the first 6 months of tenancy because they find broken things that the old tenant lived with

### Overview of Data

The data consist of 651 transactions relating to the business portfolio. Although most expenses are relating to a specific property, there are a few expenses that are a expense of the business such as the LLC tax. This data is exported from Quickbooks which provides accurate expenses for the properties and the business from January 2015 - September 2022. The data consist of 10 columns, while a few are unnecessary, it provides data of when the transaction occurred, if the transaction was an expense or income, where the money came from or is going, what the transaction is relating to, and how much was sent.

<img src="./uncleaned_data.png" width=1000 height=400>

### Data Cleaning / Preprocessing

To get the data into a form that is useable to perform an analysis on, we must make sure the final form of the data specifies which property the transaction is relating to, what the transaction was for, the amount of the transaction, and the year the transaction occurred. We are able to get an idea of which transaction is related to which property by looking at the memo and label the transaction based off of the information given in the memo.

<img src="./clean_data.png" width=700 heigh=400>

### Visualization - Capital Growth

In real estate investing, there are two types of ways to invest: cash flow or appreciation. Cash flow investing allows you to have the extra cash right away after using the rent money to pay the mortgage and expenses. Appreciation investing is a long game that is less guaranteed, but many times out performs cash flow investing. The types of investing depends on where the properties are located because in many places like California, it is very difficult to cash flow a property because of the high property values.

In this case, it is important to account for appreciation when looking at how properties fare against each other because it is growth on the money invested that would be received when selling the property. It also shows how the areas the properties are in have changed because appreciation comes from mostly external factors such as the neighborhood becoming nicer or more people are moving to the area.

<iframe src='./PCT-Growth.html' width=1000 height=600 frameBorder=0></iframe>

### Visualization - Annual Revenue from January 2015 - September 2022

Annual revenue is an important part of the investment because it isn't investing if there is no return on the money. Annual revenue comes from rent

<iframe src='./Revenue.html' width=1000 height=600 frameBorder=0></iframe>

### Visualization - Repairs and Maintenance Compared to Revenue from January 2015 - September 2022

Repairs and Maintenance is important because it takes away from the profit

<iframe src='./Repairs and Maintenance Rev.html' width=1000 height=600 frameBorder=0></iframe>

### Visualization - Net Operating Income from January 2015 - September 2022

<iframe src='./NOI.html' width=1000 height=600 frameBorder=0></iframe>

### Visualization - Cap Rate from January 2015 - September 2022

Capitalization rate is an important metric because it describes the risk of a property. The lower cap rates tend to mean a lower risk investment, but it comes with not as high returns because it is a more desireable area with higher home values. While the home values grow higher, rent follows but at a slower pace because renters tend to be more limited in income compared to someone buying a home in the area. The higher cap rates correspond to a higher risk investment, but the higher risk comes with higher return. Like all investments, this follows the principles of "high risk, high reward."

The reason why I chose to use compare the cap rate with operating expenses and without is because the Fort Pike property has higher turnover which means that it has more maintenance request. To get a better comparison of the properties if there wasn't a difference in turnover.


<iframe src='./CapRate.html' width=1000 height=600 frameBorder=0></iframe>

### Visualization - Cash on Cash Return from January 2015 - September 2022

Looking for return on money each year. S&P500 averages 7% as a baseline

<iframe src='./COC.html' width=1000 height=600 frameBorder=0></iframe>

### Takeaways

 - While Bright Leaf 
 - Cap rate does not account for the fact that the Bright Leaf property's rent could be raised about $600 to market rent


### Conclusion

Does not make sense for turnover often because maintenance are often high the first year of move in. It is better to raise rent each year close to market rent but still below to give the tenant an incentive to stay.

While the Bright Leaf property has opportunity to significantly outperform the Fort Pike property if the rents were raised closer to 