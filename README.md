# Home_Sales

Home-Sales-Big-Data-with-PySpark-SQL

In this challenge, you'll use your knowledge of SparkSQL to determine key metrics about home sales data. 
Then you'll use Spark to create temporary views, partition the data, cache and uncache a temporary table, 
and verify that the table has been uncached.

Instructions
1.Rename the Home_Sales_starter_code.ipynb file as Home_Sales.ipynb.

2.Import the necessary PySpark SQL functions for this assignment.

3.Read the home_sales_revised.csv data in the starter code into a Spark DataFrame.

4.Create a temporary table called home_sales.

5.Answer the following questions using SparkSQL:

   5.1.What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

|YEAR|AVERAGE_PRICE|
+----+-------------+
|2022|    296363.88|
|2021|    301819.44|
|2020|    298353.78|
|2019|     300263.7|


   5.2.What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

+----------+-------------+
|YEAR_Built|AVERAGE_PRICE|
+----------+-------------+
|      2017|    292676.79|
|      2016|    290555.07|
|      2015|     288770.3|
|      2014|    290852.27|
|      2013|    295962.27|
|      2012|    293683.19|
|      2011|    291117.47|
|      2010|    292859.62|
+----------+-------------+

   5.3.What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.


+----------+-------------+
|YEAR_Built|AVERAGE_PRICE|
+----------+-------------+
|      2017|    298855.99|
|      2016|    297595.75|
|      2015|     298521.3|
|      2014|    290131.71|
|      2013|    305310.69|
|      2012|    305637.43|
|      2011|    296642.44|
|      2010|    301208.84|
+----------+-------------+

   5.4.What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.


+----+-------------+
|view|AVERAGE_PRICE|
+----+-------------+
|  99|   1061201.42|
|  98|   1053739.33|
|  97|   1129040.15|
|  96|   1017815.92|
|  95|    1054325.6|
|  94|    1033536.2|
|  93|   1026006.06|
|  92|    970402.55|
|  91|   1137372.73|
|  90|   1062654.16|
|  89|   1107839.15|
|  88|   1031719.35|
|  87|    1072285.2|
|  86|   1070444.25|
|  85|   1056336.74|
|  84|   1117233.13|
|  83|   1033965.93|
|  82|    1063498.0|
|  81|   1053472.79|
|  80|    991767.38|
+----+-------------+
only showing top 20 rows

--- 1.0915367603302002 seconds ---

6.Cache your temporary table home_sales.

7.Check if your temporary table is cached.

8.Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.


+----+-------------+
|view|AVERAGE_PRICE|
+----+-------------+
|  99|   1061201.42|
|  98|   1053739.33|
|  97|   1129040.15|
|  96|   1017815.92|
|  95|    1054325.6|
|  94|    1033536.2|
|  93|   1026006.06|
|  92|    970402.55|
|  91|   1137372.73|
|  90|   1062654.16|
|  89|   1107839.15|
|  88|   1031719.35|
|  87|    1072285.2|
|  86|   1070444.25|
|  85|   1056336.74|
|  84|   1117233.13|
|  83|   1033965.93|
|  82|    1063498.0|
|  81|   1053472.79|
|  80|    991767.38|
+----+-------------+
only showing top 20 rows

--- 0.9863462448120117 seconds ---


9.Partition by the "date_built" field on the formatted parquet home sales data.

10.Create a temporary table for the parquet data.

11.Run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

+----+-------------+
|view|AVERAGE_PRICE|
+----+-------------+
|  99|   1061201.42|
|  98|   1053739.33|
|  97|   1129040.15|
|  96|   1017815.92|
|  95|    1054325.6|
|  94|    1033536.2|
|  93|   1026006.06|
|  92|    970402.55|
|  91|   1137372.73|
|  90|   1062654.16|
|  89|   1107839.15|
|  88|   1031719.35|
|  87|    1072285.2|
|  86|   1070444.25|
|  85|   1056336.74|
|  84|   1117233.13|
|  83|   1033965.93|
|  82|    1063498.0|
|  81|   1053472.79|
|  80|    991767.38|
+----+-------------+
only showing top 20 rows

--- 1.2856545448303223 seconds ---

12.Uncache the home_sales temporary table.

13.Verify that the home_sales temporary table is uncached using PySpark.

14.Download your Home_Sales.ipynb file and upload it into your "Home_Sales" GitHub repository.


CONCLUSION: 

We noticed that there is a difference in the execution time between one technique and another. The time to run the SQL before caching was 1.09 seconds.
This time decreased to 0.98 seconds after we cached our table. However, the same job takes more time after we partitioned the data and read our table using the Parquet format. 
The new time is 1.285 seconds."

