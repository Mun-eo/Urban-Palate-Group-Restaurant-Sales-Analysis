# Urban Palate Group Restaurant Sales Analysis

<h2>Description</h2>

This project works with a hypothetical UK restaurant company "The Urban Palate Group" a growing chain of casual dining restaurants, with locations in Lisbon, London, Madrid, Berlin, and Paris known for offering modern British cuisine with international twists.

Amira, the head of regional operations of The Urban Palate Group, contacted me with concerns about inconsistent revenue performance across city locations. While the restaurant group has been expanding steadily, their internal reporting lacks the clarity needed to guide decisions on which locations are thriving, which products are performing best, and how sales are evolving over time.

She requested support in cleaning and analyzing recent order data to answer critical business questions such as:
  - Which city is generating the most revenue?
  - Is revenue increasing or decreasing over time?
  - What are the average quantities sold and average revenue per product?
  - Which product is the top-seller by quantity and by revenue?
  - What is the overall average revenue? 

Goals of the Analysis:
  1. Identify top-performing cities for potential expansion
  2.  Spot underperforming locations that may need strategic changes
  3. Optimize their menu by focusing on high-performing products
  4. Share performance metrics in their quarterly business review

<h2>Technical Tools Used</h2>

- Excel

<h2>Understanding the dataset:</h2>
The dataset consisted of 255 order transactions of products purchased per day from each city location(Lisbon, London, Madrid, Berlin, and Paris). This included the quantity, method of payment, and purchase type. This dataset was chosen as it provides the information needed to answer the critical business questions that have been requested to solve. I used Excel to clean, analyze and visualize the data as it allowed me efficiently calculate the revenue specific products were bringing in per day and which location were generating the most revenue.

<h2>Data Cleaning walk-through:</h2>

  1. First, I removed the manager column within the dataset as that column would not be relevant to answer the business questions at hand.
  2. I changed the order date values into a mm-dd-yyyy format(07-20-2022) from a dd-mm-yyyy(20-07-2022) format to see a clear progression of revenue per day
  3. Some products had variety of prices, to find the true price of each product I filtered the dataset by the product and used conditional formatting to highlight outliers in the price column.
  4. Then I used find and replace to replace the outlier values with the common price value in the price column for some of the products.
  5. When attempting to create the revenue column the returned values were not the accurate revenue number from multiplying the price of the product by the quantity number of the order to receive the revenue.
  6. I discovered the issue was with the quantity column. The values had it's decimal points even when it’s removed by the remove decimal points by function on the home page.
  7. To resolve this issue I used the =Round() formula to return the number without its decimal points, ultimately creating the accurate revenue number

This process of data cleaning improved the quality of my analysis by clearing outliers within the dataset, allowing me to create an accurate representation of revenue generated per order transaction. This ultimatly allows me to visualize the data to view the sales trends for The Urban Palate Group.

<h2>Data Analysis & Visualization:</h2>
<p align="center">
IDENTIFYING REVENUE TRENDS AND BOTTLENECKS <br/>

My first step was to map the sum of revenue on a line chart to represent the trend over time. This analysis revealed revenue increased by **24%** over time with the average revenue being $14,181.26.

The two dips in the line chart highlights a potential revenue issue for business: When all products ( Burgers, Chicken Sandwiches, Fries and Sides) are not sold in a day, revenue decreases by **36%** compared to the prior day.

<p align="center">
  <img width="472" height="603" alt="Revenue Trend Line Chart" src="https://github.com/user-attachments/assets/a690e15d-ed2d-410d-b565-7c4fd0263033" />

 <p align="center">
REVENUE AND QUANTITY DISCREPANCIES BETWEEN PRODUCTS <br/>

After I discovered the revenue trend at The Urban Palate Group, I dug deeper to see the revenue discrepancies between each product the restaurants offer. 

It came out that the product bringing the most revenue on average were burgers with fries, chicken sandwiches and beverages bringing a similar amount of revenue but not a substantial amount when compared to burgers. However, when it came to quantity, beverages and fries had the highest quantity among all the products. Suggesting that customers prefer their burgers over the other products

<p align="center">
<img width="519" height="646" alt="Products Bar Chart" src="https://github.com/user-attachments/assets/7bf65562-1743-4798-b670-3459cc53eb7a" />

<p align="center">
REVENUE DISCREPANIES BETWEEN CITIES <br/>

Using a column chart, I discovered that their restaurant in Lisbon is the company's best performer bringing in 29.79% of the total revenue, with the Paris location not performing well bringing in 10.61% of the total revenue. 

Digging deeper, the reason for this vast discrepancy in revenue between locations is due to the companies best product (burgers) being purchased more at locations such as Lisbon and London compared to Madrid, Berlin, and Paris 

<p align="center">
<img width="549" height="646" alt="Cities Bar Chart" src="https://github.com/user-attachments/assets/41844951-038c-457c-9590-b30da7379996" />

<h2>Reccomendations</h2>  

Considering The Urban Palate Groups most profitable product is burgers and when they aren’t purchased theirs a massive decrease in revenue across locations. I have listed a couple of recommendations

  1. Develop a new product to add to the menu that will generate more revenue to allow locations that are low on burger purchases to increase their revenue split
  2. With locations in london and portugal generating the most revenue, the company should potentially look further to expand in these regions compared to their other restaurant locations
  3. To optimize more purchases of products, restaurant should develop deals and combos that increases the quantity of products purchased
