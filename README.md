# Roger's Ultimate Cafe Sales Snapshot

<h2>Description:</h2>
This project works with sales data from a food company "Roger's Ultimate Cafe" a growing cafe restaurant. The ownwer of the cafe contacted me with the goal of gaining clarity on the cafe's performance after one year of being open and potential decisions to improve sales for their second year of operations.

**Goals of the Analysis:**
1. Identify customers perfered order items
2. Uncover how many sales were tracked in year 1
3. Identify which items generate the most revenue
4. Identify how revenue fluctuates throoughout the year
5. Whats the average revenue
6. What acquistion method do customers prefer
7. What payment method do customers prefer?

<h2>Understanding the dataset:</h2>
The dataset consisted of 255 order transactions of products purchased per day from each city location(Lisbon, London, Madrid, Berlin, and Paris). This included the quantity, method of payment, and purchase type. This dataset was chosen as it provides the information needed to answer the critical business questions that have been requested to solve. I used Excel to clean, analyze and visualize the data as it allowed me efficiently calculate the revenue specific products were bringing in per day and which location were generating the most revenue.

<h2>Data Cleaning walk-through:</h2>
First, I removed the manager column within the dataset as that column would not be relevant to answer the business questions at hand.
I changed the order date values into a mm-dd-yyyy format(07-20-2022) from a dd-mm-yyyy(20-07-2022) format to see a clear progression of revenue per day
Some products had variety of prices, to find the true price of each product I filtered the dataset by the product and used conditional formatting to highlight outliers in the price column.
Then I used find and replace to replace the outlier values with the common price value in the price column for some of the products.
When attempting to create the revenue column the returned values were not the accurate revenue number from multiplying the price of the product by the quantity number of the order to receive the revenue.
I discovered the issue was with the quantity column. The values had it's decimal points even when it’s removed by the remove decimal points by function on the home page.
To resolve this issue I used the =Round() formula to return the number without its decimal points, ultimately creating the accurate revenue number
This process of data cleaning improved the quality of my analysis by clearing outliers within the dataset, allowing me to create an accurate representation of revenue generated per order transaction. This ultimatly allows me to visualize the data to view the sales trends for The Urban Palate Group.

