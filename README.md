
# **Pizza Sales Comprehensive Analysis**

## Introduction

The target of the project is to provide a comprehensive analysis and presentation of pizza sales data. This includes examining various aspects such as total revenue, average order value, etc. This project aims to identify key trends and insights, such as best-selling pizza categories, sales performance by day and month, and the contribution of different pizza sizes to overall sales.
By visualizing this data through charts and graphs, the project seeks to offer actionable insights that can help in making informed business decisions to boost pizza sales and improve customer satisfaction.

## Data

I utilized sample pizza sales data from the year 2015. The key variables I focused on include total price, order ID, quantity, order date, and total orders. 

## Research Objective

The research objective is to evaluate business performance using key performance indicators to increase sales and hence 

## Plan of Analysis

Given the requirement documents by the client, I plan to analyze the data first by computing some metrics and then prepare some chats that will provide insight into the performance of the business.
The metrics that I plan to compute are: 

- Total Revenue
- Average Order Value
- Total Pizzas Sold
- Total Orders
- Average Pizzas Per Order

Next, I want to analyze the followings:

- Daily and monthly trend for total orders
- Percentage of sales by pizza category and pizza size
- Total pizza sold by pizza category
- Top 5 and bottom 5 pizza sellers by revenue, total quantity and total orders

![image](https://github.com/user-attachments/assets/afe7227c-da3c-461a-87d2-242d1d72ac06)


## Steps of Analysis 

- Part I

  - Imported data into MySQL Server.
  - Created data base ‘Pizza DB’ in My SQL Server.
  - Imported the necessary files.
  - Wrote queries on My SQL Server based on the requirements provided by the client.
  - Created a word document with the used queries and outputs that works as a supporting document, matching SQL outputs with PowerBI.

- Part II

  - Connected My SQL server with Power BI.
  - Did some data cleaning using some power queries and employing functions like Transform Data.
  - Did some data processing by using DAX functionalities to get custom/conditional columns in the power report.
  - Worked on data visualization, built dynamic dashboard with charts and diagrams and used advanced formalities for formatting the charts.

## Analysis 

- **KPI Computation**

To compute Total Revenue, in SQL, I took sum of the total Price; to compute Average Order Value, I summed up the total price and divided it by the count of the distinct order ids. Next, to compute the total pizzas sold, I took the sum of the quantity; to find out the total orders, I took the count of the distinct order ids. And finally, to calculate the average pizza per order, I took the sum of the quantity and divided it by the count of the distinct order ids.
To get a clear visualization of the key performance indicators, I conducted the same analysis in Power Bi and generated the dynamic visualization cards.

![image](https://github.com/user-attachments/assets/d459b784-17a2-44aa-b83a-e567deebc730)

- **Charts**

To find the Daily Trends for Total order, in SQL, I used the function DATENAME with interval of DW from the field ‘Order_id’and named it as order_day. Next to find the total orders, I aggregated the distinct order ids and named it as Total_orders. For visualization, I used column charts in Power BI. On the x-axis I have the Order Days, and, on the y-axis, I have the total orders.

![image](https://github.com/user-attachments/assets/ae68f2cc-7aca-4e58-9b1c-6ff4aac4bd26)

To find the Monthly Trend of Total Orders, I again used the DATENAME function for the field order_date and names it as Month_Name. Then, I grouped it by Month and Order_date and presented the total orders in descending order. For visualization, I used a line chart in which, on the x-axis I have the months and, on the y-axis, I have the Total Orders.

![image](https://github.com/user-attachments/assets/a8f68c12-3f32-4664-ae5e-ead2a416d13e)

Now, to calculate the Percentage of Sales by Pizza Category, in SQL, I have selected the pizza category column; ultimately took the ratio of the revenue of each pizza category and the total revenue and multiplied by hundred. For visualization, I used a donut chart.


![image](https://github.com/user-attachments/assets/25f4d403-c301-4846-922c-2d375689c8b8)

Next, to compute the Percentage of Sales by Pizza Size, I have divided the total sales of each size of pizza and divided it by the total sales of all sizes of pizza. For visualization, like before, I have used a donut chart in Power BI.

![image](https://github.com/user-attachments/assets/6dadffc5-35bc-485c-8bad-daab65400d82)

To calculate the Total Pizza Sold by Pizza Category, I have taken the sum of the quantity sold for each pizza category, grouped by the pizza category and ordered it by the total quantity sold in descending order. For visualization, I have used Funnel chart where, for Category, I have taken the pizza category and for the values, I have taken the total pizzas sold.

![image](https://github.com/user-attachments/assets/adeaf45a-c224-4928-8a8a-2f44e0e73fe9)

To compute the Top 5 Pizzas by Revenue, I took the total revenue for each pizza Names using group by function and then used the Top function to select the top 5 pizza names. I also ordered the total revenue in descending order. Next, to visualize this, I used a stacked bar chart, where, in the x-axis, I have used the pizza names and, in the y-axis, I have used the total revenue generated. I used the same procedure to get the bottom 5 results, except I ordered the total revenue in an ascending order.

![image](https://github.com/user-attachments/assets/71f5606a-81f3-45e2-a1b1-b53f2d89bf62)

To find the Top 5 Sellers by Quantity, I grouped by the sum of the quantity by pizza name and then used the top function to select the top 5 sellers. Next, I ordered the total quantity in a descending order. For visualizing this, I have used bar charts with total quantity sold on the x-axis and pizza names on the y-axis. For getting the bottom 5 seller, I have followed the same steps, except ordering the total quantity in an ascending order.

![image](https://github.com/user-attachments/assets/bc3dab38-181a-4d3a-a713-0115eb6fbe34)

Finally, to calculate the Top 5 Pizzas by Total Orders, I first aggregated the order ids to get the total order. Thereafter, I grouped the data by pizza name and then used the top function. Ultimately, I ordered the total orders in descending order. For visualization, I have once again used the stacked bar charts with total orders on the x- axis and the pizza names on the y-axis. Next, to get the Bottom 5 pizzas by Total Order, I followed the same steps, except ordering the total order in an ascending order.

![image](https://github.com/user-attachments/assets/8bc4fc0d-553e-4c44-9ace-de589fbae176)

## Result

- **Key Insights from KPIs**

    - For the year of 2015, the store generated a total revenue of $730.74K.
    - On average, each order placed was of $ 38.31.
    - The total number of pizzas sold in 2015 was 49, 574.
    - Total number of orders were 21, 350.
    - On average people ordered 2.32 pizzas

- **Key insights for the charts**

    - Based on the daily trend chart, the number of total pizzas ordered is highest during Fridays, followed by Saturdays and Thursdays.
    
    - According to the monthly trend chart, the highest number of pizzas ordered was in July (1,935), followed by May (1,853) and January (1,845). 
    
    - Among the categories, Classic pizzas had the highest sales percentage at 26.91%, closely followed by Supreme pizzas at 25.46%. 
    
    - In terms of size, Large Pizzas led with a sales percentage of 45.89%, with Medium Pizzas coming next at 30.49%.

    - The Thigh Chicken Pizza generates the highest revenue at $43,434.25, followed by The Barbecue Chicken Pizza at $42,768. On the other hand, the Brie Carree Pizza brings in the lowest revenue at $11,588, with the Green Garden Pizza slightly higher at $13,955.75.
    
    - The top two best-selling pizzas by quantity are The Classic Pizza with 2,453 orders, followed closely by The Barbecue Chicken Pizza with 2,432 orders. Conversely, the bottom two sellers are The Brie Pizza with 490 orders and The Mediterranean Pizza with 934 orders.
    
    - By total orders, The Classic Deluxe Pizza rank the highest 2329 followed by The Hawaiian Pizza 2280 and The Brie Carrie Pizza 480 and the Mediterranean Pizza 912 ranks the lowest and the second lowest.
    
    - In terms of total orders, The Classic Deluxe Pizza ranks the highest with 2,329 orders, followed by The Hawaiian Pizza with 2,280 orders. On the lower end, The Brie Carree Pizza has 480 orders, and The Mediterranean Pizza ranks just above it with 912 orders.

![image](https://github.com/user-attachments/assets/d7604c73-acdb-42a3-86af-3c39741f010a)

![image](https://github.com/user-attachments/assets/3abcb13d-7d8b-48da-b6ea-1e0a09db5c61)



##  Managerial Implications

Based on the insights gathered, here are some managerial implications and recommendations:

**Revenue and Order Insights**
    
- **Revenue Generation**:

    - Focus on High Revenue Pizzas: Since Thigh Chicken Pizza and Barbecue Chicken Pizza generate the highest revenue, consider promoting these items more aggressively through marketing campaigns and special offers.
        
    - Revamp Low Revenue Pizzas: Evaluate the Brie Carree Pizza and Green Garden Pizza to understand why they generate lower revenue. Consider revising their recipes, pricing, or marketing strategies to boost their sales.

- **Order Value**:

    - Increase Average Order Value: With an average order value of $38.31, explore upselling and cross-selling strategies. For example, suggest complementary items like drinks, sides, or desserts to increase the total order value.

- **Order Quantity**:

    - Encourage Larger Orders: Since people order an average of 2.32 pizzas, create bundle deals or family packs to encourage customers to order more pizzas per transaction.


**Sales Trends**

   - **Daily Trends**:

       - Peak Days: With the highest number of pizzas ordered on Fridays, followed by Saturdays and Thursdays, consider offering special promotions or discounts on these days to maximize sales.
       - Staffing and Inventory: Ensure adequate staffing and inventory levels on peak days to meet the higher demand and maintain customer satisfaction.

 - **Monthly Trends**:

    - Seasonal Promotions: Since July, May, and January see the highest number of orders, plan seasonal promotions or limited-time offers during these months to capitalize on the increased demand.

**Product Mix**

  - **Category Performance**:

    - Promote Popular Categories: Classic and Supreme pizzas are the top-selling categories. Highlight these categories in your marketing materials and menu placements to attract more customers.
    - Innovate with Low Performers: For categories with lower sales, consider introducing new flavors or limited-time offers to spark interest and boost sales.

 - **Size Preferences**:

    - Large Pizza Promotions: Since Large pizzas account for the highest sales percentage, offer deals on large pizzas to encourage customers to choose this size.
    - Medium Pizza Strategies: Develop strategies to increase the sales of Medium pizzas, such as combo deals or targeted promotions.

**Product-Specific Insights**

- **Top Sellers**:

    - Leverage Best Sellers: The Classic Pizza and Barbecue Chicken Pizza are the top sellers by quantity. Use these popular items in marketing campaigns and consider creating special editions or variations to maintain customer interest.

- **Low Sellers**:

    - Revise or Replace: For low-selling pizzas like The Brie Pizza and The Mediterranean Pizza, consider revising their recipes, offering limited-time discounts, or even replacing them with new options based on customer feedback.

By implementing these strategies, you can optimize your product offerings, enhance customer satisfaction, and ultimately drive higher sales and revenue for the pizza shop. 

## Conclusion
In conclusion, focusing on high-revenue and popular pizzas, leveraging peak sales days and months, and optimizing product offerings based on customer preferences can significantly boost sales and revenue for the pizza shop. Implementing targeted promotions and revising low-performing items will further enhance customer satisfaction and drive growth.




   
