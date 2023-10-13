# 400Project - Group 8 

#Week1:10.9-10.13


##Description:
Dillard’s is a major retail chain with several stores. Dillard’s has point-of-sales (POS) data over a period of time in 2004 and 2005 that includes their store information, stock-keeping-unit (SKU), and transactions. Over the recorded times, around half of all transactions happen with some discounts. The MLDS team believes that it would be beneficial to understand which components (product’s features, location, time of the year, etc.) contribute to the need to offer discounts within transactions.

Understanding the mechanics of transactions with discounts will allow Dillard’s to increase the production rate for products that can be sold without a discount. Moreover, Dillard’s can also accurately predict future revenue by predicting the discount (reduction of sales price).


##Findings and Analysis:
data size below:
Deptinfo: 59
Skstino: 39230146
Skuinfo: 1564177
Strinfo: 452
Transact: 120916896

Skstino:
First, I used python to explore the dataset.
Skstinfo_df.shape == (39230146, 5)
There are 39230146 rows and 5 columns.

Skuinfo:
There are 1,564,198 observations and 12 variables in the Skuinfo dataset. However, the last two variables are unknown variables (I named them "Unknown"), which contain numbers and text. For irrelevant variables, we decided to delete them.
Other variables in this dataset, such as "STYLE", "SIZE", which are purely numeric, purely textual, or a combination of numeric, textual, and symbolic, will need to be cleaned up and categorized in depth for further discussion.
Some numeric variables such as "DEPT", "UPC", "COLOR", "SIZE ", all of which contain unknown values, need to be cleaned up.
This is the summary of the Skuinfo dataset.


Transact:
The transactions dataset is the largest one out of the 5 datasets, it contains 120,916,896 million observations and 14 features. According to the database schema there are only 12 features in the transactions table. Therefore, for next week we are planning to delve deeper into the dataset to clean the data before we perform any further analysis.



Data thoughts:
1. We found that the the top 3 states that has the most stores are Texas, Florida, and Arizona. The top cities that has the most stores are LITTLE ROCK,GILBERT, SAN ANTONIO,OLATHE, HOUSTON.


2. What is the difference between Sales price, Original price, and Retail price 
There are five data sheets in the file with the relationship shown in the database diagram, and I think we could construct the data as the dataframe in sql.




##Plans for Next Week:

Ideas drafted for the first week(which need further discussion):
1. Can we predict customer purchase behavior based on transaction data including variables such as transaction amount (AMT), brand (BRAND), stock item classification (CLASSID), color (COLOR), cost (COST), department (DEPT), original price (ORGPRICE), quantity (QUANTITY), retail price (RETAIL), sale date (SALEDATE), size (SIZE), and other relevant factors
2. Can we optimize pricing and inventory management in retail stores by analyzing historical transaction data
including variables like transaction amount (AMT), retail price (RETAIL), sale date (SALEDATE), department (DEPT), and brand (BRAND)
3. In a CITY, there are different ZIPs, what is the effect of different ZIPs on COST? There may be some cities where the COST is higher, but the COST is lower in the suburban areas of the CITY. What is the effect of different ZIPs in different CITYs on COST?
4. Is there any relationship between CLASSID and COST? Is it that the higher the CLASS, the higher the COST? Also we need to control variables, for example, compare the relationship between CLASSID and COST under one same ZIP.
5. What is the relationship between PACKSIZE, RETAIL and QUANTITY? Is it that the larger the PACKSIZE, the smaller the RETAIL per unit? Because a large PACKSIZE indicates that a wholesale, such as Costco, can have lower prices for one unit, then isn't it true that QUANTITY will be larger? Because it's cheaper
6. What is the relationship between SIZE, COST, and RETAIL? A larger SIZE will have more COST, but a larger SIZE does not necessarily have a larger RETAIL
What is the relationship between SALEDATE and QUANTITY? Some products are seasonal and some can be sold year round. Determine what product it is based on the change in QUANTITY over the year
7. Can placing products with high QUANTITY, large RETAIL, and small SIZE in areas where people have high purchasing potential make it easier for them to buy them, and will this promote greater sales? Can cost and price be reduced by placing products with low QUANTITY, small RETAIL and large SIZE in remote areas?
8. Are there relationships between CITY, STYLE, and COLOR? Do different cities have different preferences?

Research Questions with team: 
Which item has the highest vs. lowest sales 
Which color from the items is in fashion? 
For that we will look at the highest sales or biggest production quantity. 
How much inventory is left or how much demand there is for certain products
We could do an analysis to see what affects demand for specific products (e.g. top 5) and predict if there is enough inventory to cover future demand. 
If not enough inventory we could make a suggestion of how much more needs to be produced. 
Or  which other products that have less demand we can supply less of, so we  can instead cover future demand shortages for the products that have higher demand. 
We can look and see which states have higher sales as well as which states. In addition to that we can look and see whether demand is met better in the states that have inventory locations.  

<<<<<<< HEAD

=======
>>>>>>> 7088453 (addd sth in title)
