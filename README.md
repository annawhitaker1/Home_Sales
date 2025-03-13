# Home_Sales
I started off by created the Spark Session, read the CSV file into a PySpark Dataframe, and created a temporary dataframe to read the CSV file into.

I created a query of average price for a four bedroom house sold per year. The average prices are as shown below. The year with the highest average price is 2021.
+----+---------+
|year|avg_price|
+----+---------+
|2019| 300263.7|
|2020|298353.78|
|2021|301819.44|
|2022|296363.88|
+----+---------+ 

I created a query of average price of a home for each year the home was built that have 3 bedrooms and 3 bathrooms. The average prices are as shown below. The year built with the highest average price is 2013.
+----------+---------+
|year_built|avg_price|
+----------+---------+
|      2010|292859.62|
|      2011|291117.47|
|      2012|293683.19|
|      2013|295962.27|
|      2014|290852.27|
|      2015| 288770.3|
|      2016|290555.07|
|      2017|292676.79|
+----------+---------+

I created a query of average price of a home for each year the home was built that have 3 bedrooms and 3 bathrooms, with two floors, and are greater than or equal to 2000 square feet. The average prices are as shown below. The year built with the highest average price is 2012.
+----------+---------+
|year_built|avg_price|
+----------+---------+
|      2010|285010.22|
|      2011|276553.81|
|      2012|307539.97|
|      2013|303676.79|
|      2014|298264.72|
|      2015|297609.97|
|      2016| 293965.1|
|      2017|280317.58|
+----------+---------+

I created a query of the average price of home per "view" rating having an average home price greater than or equal to $350,000. This took .916 seconds to run.
I cached the home sales table. From the cached data, I ran the same query as above. This took 1.766 seconds to run.
I partitioned by the "date_built" field on the formatted parquet home sales data and created a temporary table. With this parquet data, I ran the same query as above. This took .907 seconds to run.
Out of all the data sets, the parquet data ran the quickest.

At the end, I uncached the home_sales temporary table.
