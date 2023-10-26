# Home_Sales

This challenge uses SparkSQL to determine key metrics about home sales data and utilises temporary views, partitions, caching and uncaching a temporary table, and verifying that the table has been uncached.  In addition time trials are run on the processing time for each of the views.  Metric outcomes and time trial results are included below. 

#### Average price for a four bedroom house sold in each year rounded to two decimal places
![image](https://github.com/VioletRogue12/Home_Sales/assets/130148039/8945a4fd-36b8-4bef-b8b2-ec5e08ce600c)


#### Average price of a home for each year the home was built that have 3 bedrooms and 3 bathrooms rounded to two decimal places
![image](https://github.com/VioletRogue12/Home_Sales/assets/130148039/8da8dadc-1f7f-45b2-8b26-6e868413420f)


#### Average price of a home for each year built that have 3 bedrooms, 3 bathrooms, with two floors, and are greater than or equal to 2,000 square feet rounded to two decimal places
![image](https://github.com/VioletRogue12/Home_Sales/assets/130148039/1eef9e70-722f-430a-ab9a-5a410552c840)


#### The "view" rating for the average price of a home, rounded to two decimal places, where the homes are greater than or equal to $350,000? Although this is a small dataset, including the run time for this query
![image](https://github.com/VioletRogue12/Home_Sales/assets/130148039/5b2f0d55-fce5-48be-9570-a563654e86bf)


#### Using cached data, run the previous query that filters view ratings with average price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime (see below).
![image](https://github.com/VioletRogue12/Home_Sales/assets/130148039/5b2f0d55-fce5-48be-9570-a563654e86bf)


#### Partition by 'date_built' on formatted parquet home_sales data. Run the same query that filters view ratings with average price of greater than or eqaul to $350,000 with the parquet DataFrame. Round your average to two decimal places. Compare the run time to that of the cached version (see below). 
![image](https://github.com/VioletRogue12/Home_Sales/assets/130148039/5b2f0d55-fce5-48be-9570-a563654e86bf)


### Comparison of run times
|Uncached|Cached|Partitioned (parquet|
|--------|------|--------------------|
|0.36sec |0.21sec |0.26sec|

In this instance, the cached data performed with the fastest processing time.  

