# Pizza Store Sales Dashboard

## Project Aim:
- Build a monthly sales and KPI dashboard for a fictional pizza restaraunt
- Use Python to analyze data check accuracy of dashboard
- Find insights in sales data for December 2015 and recommend business decisions based on the data
- Sales data are for full year 2015

## Resouces
- Data stored in four separate CSV files
    orders.csv
    order_details.csv
    pizzas.csv
    pizza_types.csv

- Tools Used:
    - Tableau Public - [Dashboard here](https://public.tableau.com/app/profile/michael.hertel/viz/PizzaStoreDashboard/Dashboard2)
    - Python - Exploraty Analysis and Dashboard Data Validation

## Questions to Answer:
- Find monthly totals for KPIs with percentage change from previous month
    Total Sales Dollars
    Total Units Sold
    Total Orders
- At what times and days are sales the strongest and weakest?
- Which pizza sizes are the strongest and weakest?
- Which pizza types are the strongest and weakest?
- What opportunities are there to capitalize on strong sellers and cut costs on weak sellers?

## Findings:
- Total dollars sold, total orders, and total units sold are all down in December from November
- Total dollars and units sold are down more than number of orders
    - Fewer people are ordering multiple pizzas on an order
![dollars](/images/dollars_card.png) ![units](/images/units_card.png)![orders](/images/orders_card.png)
- Total dollars are strongest at lunch time hours than dinner hours
- Total dollars are stronger on weekdays than weekends
- Avg units sold per order is highest during lunch time hours, as seen on the tooltips in these to images:
![lunch](/images/heat_map_lunch.png) ![dinner](/images/heat_map_dinner.png)
    - Recommendation: offer buy-one-get-one 50% off or some similar offer in the evening hours to increase pizzas per order and thus total dollars in evening
- Very few orders are being placed before 11:00 am and after 10:00 pm, as can been seen in the above images
    - Recommendation: reduce business hours to 11:00 am to 11:00 pm to cut down labor costs during low-sales times
- Very few XL or XXL pizzas are being sold
![sizes](/images/sizes.png)
    - Recommendation: eliminate  these sizes from the menu, cutting down on inventory costs and inventory spoilage
- Items such as Bree Carre pizza sell far fewer units than other types in the same category
    - Recommendation: eliminate Brie Carre and other pizza types from the menu, cutting costs for specialty ingredients

## Techniques Used
Tableau Techniques:
- Used Perameters to allow users to select the month of sales to view for the whole dashboard and which category to view for one chart
- Used Calculated Fields to display total dollars, units, and orders for the user's chosen month, to calculate month-over-month changes in the KPIs, and create up and down arrows for KPI cards

Python Techniques:
- Read in csv files with pandas
- checked for null values and duplicates in columns where values should be unique
![null/duplicates](/images/nulls_duplicates_check.png)
- converted strings to datetime object for time series analysis
- merged dataframes
- used groupby to aggregate data
- 


    

    
    