# Pizza Store Sales Dashboard

## Project Aim:
- Use Python Pandas to read in and explore sales data for a fictional pizza store and determine if any data cleaning or transformation is required
- Build a monthly sales and KPI dashboard
- Used Python to analyze the data for confirming the accuracy of the calculations on the dashboard
- Find insights in sales data for December 2015 (most recent month in the dataset) and recommend business decisions based on the data


## Resources
- Data for year 2015 stored in four separate CSV files
    orders.csv
    order_details.csv
    pizzas.csv
    pizza_types.csv

- Tools Used:
    - Tableau Public - [Dashboard here](https://public.tableau.com/app/profile/michael.hertel/viz/PizzaStoreDashboard/Dashboard2)
    - Python 3.9.7, Pandas, Jupyter Notebook 
        - [Exploratory Analysis Notebook](https://github.com/mhertel278/pizza_store/blob/main/Pizza%20Sales%20EDA.ipynb)
        - [Dashboard Data Accuracy Check Notebook](https://github.com/mhertel278/pizza_store/blob/main/Pizza%20Dashboard%20Data%20Accuracy%20Check.ipynb)
    - Powerpoint - Dashboard wire frame background
## Questions to Answer:
- Find monthly totals for KPIs with percentage change from previous month
    - Total Sales Dollars
    - Total Units Sold
    - Total Orders
- At what times and days are sales the strongest and weakest?
- Which pizza sizes are the strongest and weakest?
- Which pizza types are the strongest and weakest?
- What opportunities are there to capitalize on strong sellers and cut costs on weak sellers?

## Findings:
- Total dollars sold, total orders, and total units sold are all down in December from November
- Total dollars is down a slightly more than number of orders and total units
    - Fewer people are ordering multiple pizzas on an order
![dollars](/images/dollars_card.png) ![units](/images/units_card.png)![orders](/images/orders_card.png)
- Total dollars are strongest at lunch time hours than dinner hours
- Total dollars are stronger on weekdays than weekends
- Avg units sold per order is highest during lunch time hours, as seen on the tooltips in these to images:
![lunch](/images/heat_map_lunch.png) ![dinner](/images/heat_map_dinner.png)
  
- Very few orders are being placed before 11:00 am and after 10:00 pm, as can been seen in the above images

- Very few XL or XXL pizzas are being sold
![sizes](/images/sizes.png)

- Items such as Bree Carre pizza sell far fewer units than other types in the same category
![type](/images/pizza_type.png)

### Recommendations
- Offer buy-one-get-one 50% off or some similar offer in the evening hours to increase pizzas per order and thus total dollars in evening
- Reduce business hours to 11:00 am to 10:00 pm to cut down labor costs during low-sales times
- Eliminate  XL and XXL sizes from the menu, cutting down on inventory costs and inventory spoilage
- Eliminate Brie Carre and other pizza types from the menu, cutting costs for specialty ingredients

## Troubleshooting
The coloring of the heat map initially did not update when the month parameter was changed, while the tooltips did update. Upon checking the dashboard against the data analysis done in python, I determined that the tooltips were correctly showing the sales data for the chosen month, while the coloring was summarizing the entire year. I changed fields for the heat map to use the Chosen Month Sales calculated field which fixed the problem.

## Techniques Used
### Tableau Techniques:
- Bar Charts, KPI Cards, Heatmap
- Parameters to allow users to select the month of sales to view for the whole dashboard and which category to view for one chart
![parameter](/images/parameter.png)
- Calculated Fields to display total dollars, units, and orders for the user's chosen month, to calculate month-over-month changes in the KPIs, and create up and down arrows for KPI cards
![calculated field](/images/sales_calc_field.png)
### Python Techniques:
- Read in csv files with pandas
- Checked for null values and duplicates in columns where values should be unique
![null/duplicates](/images/nulls_duplicates_check.png)
- Checked number of unique values in certain columns to validate foreign key columns
![unique validation](/images/unique_validation.png)
- Checked data types and converted strings to datetime object for time series analysis
![datetime](/images/datetime.png)
- merged dataframes
- used groupby to aggregate data
- 


    

    
    