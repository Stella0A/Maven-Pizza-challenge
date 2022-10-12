# Maven-Pizza-challenge
For the Maven Pizza Challenge, you’ll be playing the role of a BI Consultant hired by Plato's Pizza, a Greek-inspired pizza place in New Jersey. You've been hired to help the restaurant use data to improve operations, and just received the following note:

Welcome aboard, we're glad you're here to help!

Things are going OK here at Plato's, but there's room for improvement. We've been collecting transactional data for the past year, but really haven't been able to put it to good use. Hoping you can analyze the data and put together a report to help us find opportunities to drive more sales and work more efficiently.

Here are some questions that we'd like to be able to answer:

1. What days and times do we tend to be busiest?
2. How many pizzas are we making during peak periods?
3. What are our best and worst selling pizzas?
4. What's our average order value?
5. How well are we utilizing our seating capacity? (we have 15 tables and 60 seats)

### About the dataset
  This dataset contains 4 tables in CSV format;
1. The "Orders" table contains the date & time that all table orders were placed
2. The "Order Details" table contains the different pizzas served with each order in the Orders table, and their quantities
3. The "Pizzas" table contains the size and price for each distinct pizza in the Order Details table, as well as its broader pizza type
4. The "Pizza Types" table contains details on the pizza types in the Pizzas table, including their name as it appears on the menu, the category it falls under, and its list of ingredients
https://www.mavenanalytics.io/blog/maven-pizza-challenge
### Tool used
Powerbi

### Data transformations
After loading the csv files into power query editor,I merged the pizza types and pizza table to order details table and expanded the queries to pick out relevant columns for analysis. A total of 48625 rows and 10 columns namely pizza_id, pizza_type_id,name,size,category, ingredients,price, order_details_id,order_id,quantity.I added a new column ("quantity" * "price") to ascertain the total sales.
I renamed the orders table to Date and extracted the month,month_name and day in order to see a breakdown of sales/orders per month and day. In order to sort the months in the right order(Jan-Dec) I navigated to the database tab, selected month name column from the calendar table. Select the modeling tab and then "Sort by Column" and select your month number column.  Month name should now appear in the correct order.
In order to clearly view, analyze, and explore data and trends in my visuals, I grouped my time data into time bins.

A brief explanation about grouping & bins in powerbi
"When Power BI Desktop creates visuals, it aggregates your data into chunks (or groups) based on values found in the underlying data. Often that's fine, but there    may be times when you want to refine how those chunks are presented. For example, you might want to place three categories of products in one larger category (one    group). Or, you might want to see sales figures put into bin-sizes of 1,000,000 dollars, instead of chunks of 923,983-dollar sizes.

In Power BI Desktop, you can group data points to help you more clearly view, analyze, and explore data and trends in your visuals. You can also define the bin        size to put values into equally sized groups that better enable you to visualize data in ways that are meaningful. This action is often called                  binning". https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-grouping-and-binning
     
### Data Modelling
![Screenshot (91)](https://user-images.githubusercontent.com/81259955/193908536-394ef37c-9b47-426d-8dc8-f5c989f4dd29.png)

### Insights
#### 1.KPIs
1. A total of 49,000 orders, Revenue is 818K
2. In the first quarter, a total of 12K orders was made and revenue was 205K. The month of january and March had high number of sales and the most busiest days Friday and Tuesday
3. In the second quarter, a total of 13K orders was made and revenue was 208K.The month of May had high number of sales and the most busiest day Friday around 12pm
3. In the third quarter, a total of 12K orders was made and revenue was 205K. The month of July had high number of sales and the most busiest days wednesday,Friday, Saturday around 12 to 1pm.
4. In the fourth quarter, a total of 12K orders was made and revenue was 199K. The month of November had high number of sales and the most busiest day Thursday around 12 to 1pm and 6pm.
5. Plato Pizza has more Large(L), Medium(M) and Small(S) size pizza orders than the Xtra-large(XL) and Xtra-xtra-large(XXL) size order. Classic pizza category has high number of orders than supreme, veggie and chicken.

#### 2. What days and times do we tend to be busiest?
In order to fully understand the days and time Plato pizza is the busiest I created an hierachy that drills down from the month to the days and time. This would help stakeholders to clearly see the time of the month sales are most,and the day and time.
Plato Pizza tends to be most busiest during the months of January, March, July and November. Friday, Saturday and Thursday are always busy with high number of orders around 12 to 1pm and 5 to 6pm.

#### 3. How many pizzas are we making during peak periods?
A total of 23,817 pizzas are made during peak periods with 13,189 pizzas around 12 to 1pm and 10,628 pizzas around 5 to 6pm.

#### 4. What are our best and worst selling pizzas?
##### Best selling pizzas
In order to fully answer this business question I created an hierachy that shows the best selling pizzas and further drills down to the particular pizza type and size  that sells the most. These helps stakeholders to clearly understand the particular pizzas & sizes to look out for which could aid efficient decision making.
The top five best selling pizzas are The Classic deluxe pizza, The Barbecue chicken pizza, The Thai chicken pizza, The California chicken pizza and, The Spicy italian pizza and the particualr pizza types are spicy_ital,cali_ckn,thai_ckn,bbq_ckn,classic_dlx.
##### Worst selling pizzas
The bottom five worst selling pizzas are The Green garden pizza, The Spinach pesto pizza, The Spinach supreme pizza, The Mediterrenean pizza and, The Brie Carie pizza and the particular pizza types are brie_carie,mediterrano,spinach_supreme,spin_pesto,green_garden.

#### 5. What's our average order value?(Average order value (AOV) is an e-commerce metric that tracks the average amount spent whenever a customer places an order.
The average order value is $17.
