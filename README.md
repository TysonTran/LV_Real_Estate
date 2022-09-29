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
 - More expenses incur because the time it takes to repair home and get it rerented out takes about a month
 - Also have to pay administrative fees to property management to find new tenants
 - New tenants usually have a lot of maintenance request the first year of tenancy because they find broken things that the old tenant lived with

### Overview of Data

The data consist of 651 transactions relating to the business portfolio. Although most expenses are relating to a specific property, there are a few expenses that are a expense of the business such as the LLC tax. This data is exported from Quickbooks which provides accurate expenses for the properties and the business from January 2015 - September 2022. The data consist of 10 columns, while a few are unnecessary, it provides data of when the transaction occurred, if the transaction was an expense or income, where the money came from or is going, what the transaction is relating to, and how much was sent.

<img src="./uncleaned_data.png" width=1000 height=400>

### Data Cleaning / Preprocessing

To get the data into a form that is useable to perform an analysis on, we must make sure the final form of the data specifies which property the transaction is relating to, what the transaction was for, the amount of the transaction, and the year the transaction occurred. We are able to get an idea of which transaction is related to which property by looking at the memo and label the transaction based off of the information given in the memo.

In the preprocessing step, I also looked at maintenance repairs that were greater than 3k because these usually are capital expenditures. In this case, there was one and it was for an ac condenser. I removed this item because it would skew the results and these are items that have a estimated lifespan that should be saved for over its life.

<img src="./clean_data.png" width=700 heigh=400>

### Visualization - Capital Growth

In real estate investing, there are two types of ways to invest: cash flow or appreciation. Cash flow investing allows you to have the extra cash right away after using the rent money to pay the mortgage and expenses. Appreciation investing is a long game that is less guaranteed, but many times out performs cash flow investing. The types of investing depends on where the properties are located because in many places like California, it is very difficult to cash flow a property because of the high property values.

In this case, it is important to account for appreciation when looking at how properties fare against each other because it is growth on the money invested that would be received when selling the property. It also shows how the areas the properties are in have changed because appreciation comes from mostly external factors such as the neighborhood becoming nicer or more people are moving to the area.

<iframe src='./PCT-Growth.html' width=1000 height=600 frameBorder=0></iframe>

While Bright Leaf has outperformed Fort Pike in appreciation, that doesn't show the full picture of the investment because it is only realized once sold. Real estate is a long term investment, so that figure could go down because appreciation is never guaranteed but over the long term, we expect it to appreciate further. This does hint towards Bright Leaf being a better investment in having more rent growth and more buyers in the area.

### Visualization - Annual Revenue from January 2015 - September 2022

To combat the problem with appreciation not being guaranteed, there is a second part to real estate investing. That is renting out the home. This provides a more secure way to generate some revenue to cover the expenses and bring some return to the money that was invested.

<iframe src='./Revenue.html' width=1000 height=600 frameBorder=0></iframe>

Fort pike has outperformed Bright Leaf in consistently providing a higher revenue. A higher revenue is good because it gives more room to remain profitable even when capital expenditures arise. Although the revenue of Fort Pike looks good, we are not sure how the high turnover rate will affect the profit because there are more repairs and maintenance request done.

### Visualization - Repairs and Maintenance Compared to Revenue from January 2015 - September 2022

Repairs and Maintenance is important because these are expenses that need to be paid and take away from the profit at the end of the year. If this is not accounted for, it can hide how a property is actually performing.

<iframe src='./Repairs and Maintenance Rev.html' width=1000 height=600 frameBorder=0></iframe>

We can see that for most years, Bright Leaf has a relatively low dollar amount of maintenance request. Fort Pike has the highest maintenance dollar amount on years where turnover happens. We can see in 2018 it is high but the year after is low. We can also see that turnover causes a higher $ amount of maintenance request in 2021 because that was the year when a tenant who was living there on their first year moved out and a new tenant moved in. The highest amount of maintenance request tend to be in the first year that a renter has lived there. 

### Visualization - Net Operating Income from January 2015 - September 2022

Net operating income (NOI) is an important metric because it factors in expenses which is a big part of maintaining a property. NOI is an important indicator of profitability and accounts for other factors such as turnover that revenue can not account for.

<iframe src='./NOI.html' width=1000 height=600 frameBorder=0></iframe>

While Fort Pike consistently had a higher revenue, we can see that it was not the case for the years a turnover happened. In 2018 and 2020, we can see that the NOI was much closer as compared to when there was no turnover such as 2015-2017. In 2021, we can even see that Bright Leaf had a higher NOI than Fort Pike even though Fort Pike has a higher annual revenue.

### Visualization - Cap Rate from January 2015 - September 2022

Capitalization rate is an important metric because it describes the risk of a property. The lower cap rates tend to mean a lower risk investment, but it comes with not as high returns because it is a more desireable area with higher home values. While the home values grow higher, rent follows but at a slower pace because renters tend to be more limited in income compared to someone buying a home in the area. The higher cap rates correspond to a higher risk investment, but the higher risk comes with higher return. Like all investments, this follows the principles of "high risk, high reward."

The reason why I chose to compare the cap rate with operating expenses and without is because the Fort Pike property has higher turnover which means that it has more maintenance request. Looking at the cap rate without operating expenses provides a better idea of how the property compares when there is not high turnover in the Fort Pike property.

<iframe src='./CapRate.html' width=1000 height=600 frameBorder=0></iframe>

As we can see from the visual, Bright Leaf tends to do better when accounting for operating expenses, but is more comparable to each other when only looking at revenue. This shows that a high turnover rate hurts investment properties potential because the higher expenses incurred from each turnover.

### Visualization - Cash on Cash Return from January 2015 - September 2022

Cash on Cash return is a term mostly used for real estate, but it is similar to looking at how much a stock has grown each year relative to how much you put in. This is a good metric to have to be able to compare it to other investments and see if the money could be used better elsewhere. For example, the S&P500 has a annual average return of around 9.87% from 2001 through 2021, so we can compare the cash on cash return to that and see how the property is performing.

<iframe src='./COC.html' width=1000 height=600 frameBorder=0></iframe>

We can see that the returns of Bright Leaf has done significantly better than Fort Pike. One thing that we can notice from this is that the years of turnover for Fort Pike seem to be hurting the returns even with the higher rent. When comparing Fort Pike on the years of turnover to the years of no turnover, the years of no turnover performed better than the years with turnover.

### Takeaways
 - High turnover leads to more $ amount spent on maintenance
 - Best to raise rent closer to market value at renewal while still staying below to give the tenant an incentive to stay
     - This allows us to bring in more revenue while not having the turnover eat up a lot of the extra revenue gained from the higher amount of maintenance request
 - Having back to back turnover will cost more than keeping the rent lower and having the tenant stay longer.
 - Bright Leaf outperformed Fort Pike even though the rent is below market rate


### Conclusion

My goal for this analysis was to understand the best way to maximize revenue while minimizing the amount of maintenance request. The two factors that directly affect that is the rent charged and turnover. By having rent too high at renewal, it can cause the tenants to leave and a turnover to occur. With each turnover, there are many expenses that come with it on both the administrative and maintenance side. Turnover contributes to a high amount of maintenance request for the first year that the tenants live in the home and there are fees charged to find a new tenants for the home. The best way to bypass the turnover to save on the maintenance and administrative expenses is by keeping the rent close to market rent but below enough where it gives the tenant an incentive to stay. This is a win-win for both sides because the turnover will eat up a large amount of the rent gained of being able to rerent at market rent

