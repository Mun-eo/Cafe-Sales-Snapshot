# Roger's Ultimate Cafe Sales Snapshot

This project works with sales data from a food company "Roger's Ultimate Cafe" a growing cafe restaurant. The ownwer of the cafe contacted me with the goal of gaining clarity on the cafe's performance after one year of being open and potential decisions to improve sales for their second year of operations.


### Goals of the Analysis:
1. Identify customers preferred order items
2. Uncover how many sales were tracked in year 1
3. Identify which items generate the most revenue
4. Identify how revenue fluctuates throoughout the year
5. Whats the average revenue per month?
6. What acquistion method do customers prefer?
7. What payment method do customers prefer?

<h2>Understanding the dataset:</h2>
The dataset consisted of 10,001 order transactions of products purchased per day at Roger's Ultimate Cafe. This included the Item, Quantity, Price of the item, Total spent, Method of payment and Method of Acquistion. I used Excel to clean, analyze and visualize the data as it allowed me efficiently calculate the revenue specific products were bringing in per day and how much revenue the shop was generating per month.


<h2>Data Cleaning walk-through:</h2>

1. Before starting the cleaning process, I created a new sheet labeled "Cleaned_Cafe_Sales"
to clean the raw data while keeping the keep the raw data intact in a separate sheet labled "Dirty_Cafe_Sales".
2. Noticed there were blanks, missing values labled "ERROR" for the item, quantity, price per unit, total spent, payment method, location and transaction date columns. Decided to first transform the blanks and "ERROR" in the item column into the accurate item name for the recorded transaction data using the IFS() function to correlate the unknown values in the item column with the price per unit that matched that specifc item. Example: Coffee = $2 and Cookie = $1, IFS(B:B = 2, "Coffee", B:B = 1, "Cookie").
3. Then transformed the blanks and "ERROR" in the Quantity column into the accurate quantity utilizing the function ([@Revenue]/[@Price per unit]) to obtain the accurate quantity purchased in each transaction.
4. Moved onto using the Find and Replace fucntion to replace the "Error" Values in the price per unit column ensuring that each item had their respective item prince. Unfortunally 4 items had the same item price so items that weren't able to be deduced from the quanity and revenue generated for that order were removed from the dataset instead of choosing random items for unknown prices. This was to ensure that the values needed for insights were fair and consistent.
5. To handle blanks and errors within the Payment and Acquistion Method columns, it was best to create a new category to fill in the missing information. Such as blanks and errors being categorized under "other method" instead of deleting the data from the payment method column. Then blanks and errors within the acquisiton method column were categorized under "Delivery" as this an common method for the acquistion of orders. 
6. The blanks and errors within the Transaction Date were turned into blanks as any assumption of transaction dates would influence the visualization of revenue performance.

<h2>Data Analysis & Visualization:</h2>
<p align="center">
IDENTIFYING CUSTOMER TRENDS AND BOTTLENECKS <br/>

Analysis of 9,424 order transactions from January 2023 to December 2023 using a visualizational model reveals findings on customer preferences. Among items offered by Roger's Ultimate Cafe, customers typically prefer to order Coffee, Salads, and Cookies. Howeever, the items that generate the most revenue for the cafe are salads, sandwiches and smoothies makimg up 55% of the items that generate revenue. This showcases that the cafe is performing well in its first year but also shows a weakness in revenue with half of the generated revenue held by the performance of three items out of eight.

<p align="center">
  <img width="316" height="73" alt="Year 1 Sales" src="https://github.com/user-attachments/assets/f9e1cf6c-a710-4497-b44d-e2a32f1a06f3" />
  <br />
  <img width="648" height="651" alt="Bar chart of Items copy" src="https://github.com/user-attachments/assets/5a5e1c69-b8f4-47ee-a4a0-333cb83aefe0" />
</p>


  

