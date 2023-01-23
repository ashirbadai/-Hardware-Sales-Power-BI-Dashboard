
# Computer Hardware Sales Power BI Project

This Power BI dashboard provides an overview of sales performance for a computer hardware company in different regions of India. I have taken data from internet. The dashboard includes visualizations such as stacked bar charts, line charts, slicers,card to showcase key metrics such as revenue by markets, sales quantity markets by region. It also includes a map visualization to show the distribution of sales across top customers and products types. Additionally, the dashboard allows users to filter the data by date range and year wise revenue and sales quantity to gain a more detailed understanding of the sales trends. Overall, this dashboard provides valuable insights into the company's sales performance in India and can assist in decision-making and strategic planning.


## Data Analysis Using SQL-:
### Show all customer records


```bash
`SELECT * FROM customers;`
```
## Show total number of customers

```bash
`SELECT count(*) FROM customers;`
  
```
## Show transactions for Chennai market (market code for chennai is Mark001)

```bash
`SELECT * FROM transactions where market_code='Mark001';`
```
### Show distrinct product codes that were sold in chennai
```bash
`SELECT distinct product_code FROM transactions where market_code='Mark001';`
  
```
### Show transactions where currency is US dollars
```bash
`SELECT * from transactions where currency="USD"`
  
```
### Show transactions in 2020 join by date table
```bash
`SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`
  
```
### Show total revenue in year 2020, January Month
```bash
`SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR" or transactions.currency="USD");`
  
```
###  Show total revenue in year 2020 in Chennai
```bash
 `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


## Dashboard


![QR Code](https://user-images.githubusercontent.com/122656938/214122624-769a6270-5edd-45d6-9e65-06ec7b5f72c9.jpg)
![Power BI dashboard](https://user-images.githubusercontent.com/122656938/214121654-7b087426-aa3b-4e29-a4e5-4a1ce79d257e.gif)

## Tech Stack


**Tech:** Power BI, MySQL Workbench


