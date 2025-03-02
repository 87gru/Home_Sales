# Module_022 Challenge - SparkSQL
## Background
**Per BCS:**
> In this challenge, you'll use your knowledge of SparkSQL to determine key metrics about home sales data. Then you'll use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Instructions

Once I created a `home_sales` temporary table after reading in the data, I used PySpark SQL functions to answer the following questions:
* What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
 * What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
 * What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
 * What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

I then cached `home_sales` temporary table and ran the same query (average price per "view") to determine the difference in run time. The cached table was faster by **0.61** seconds.
Lastly, I partition the date_built filed on formatted parquet home sales data. I created a temporary table for the parquet data and ran the same query again. The query ran **0.72** seconds longer on the parquet home sales table vs the cached table.

## Included in this Repository
* `Home_Sales_starter_code_colab.ipynb`