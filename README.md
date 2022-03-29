# Amazon_Vine_Analysis

## Overview of the Analysis

The purpose of this analysis was to utilize various softwares in conjunction in order to make summarizations about a dataset. 

Amazon's S3 data storage was used to gather a dataset on products reviewed by Amazon. Google Collab was used for PySpark. In the PySpark file, a driver was connected in order to link our Spark Session to Postgres SQL. A database was created in Postgres that linked to a RDS database from AWS. With all of our softwares now linked, the data was imported into our PySpark file. 

The data was cleaned and 4 new dataframes were created to match the schemas we created in Postrgres. Using the driver, the cleaned dataframes were written into Postgres into our empty tables schemas. From here, we selected one table for further analysis. 

This table was exported as a CSV and loaded into a jupyter notebook. Using pandas, more data filtering occured so that we could answer a few questions about the data. 

This final dataframe was a table that showed each reveiw id, with the associated star rating, number of helpful votes, total number of votes, whether it was a verified purchase, and finally whether they were a apart of the paid Vine review program. 


## Results

After some filtering to ensure we were working with good data, the dataframe was split into reviews by paid Vine reviews and non paid Vine reviews...

Paid Vine Reviews
![alt text](https://raw.githubusercontent.com/KitWilliams07/Amazon_Vine_Analysis/main/Challenge/y.png)

Non-Paid Vine Reviews
![alt text](https://raw.githubusercontent.com/KitWilliams07/Amazon_Vine_Analysis/main/Challenge/n.png)

Breaking down the Statistics:

Number of Paid Vine Reviews: 94
Number of 5-Star Paid Vine Reviews: 48
Percentage of 5-Star: 51.06%


Number of Non-Paid Vine Reviews: 40,471
Number of 5-Star Non-Paid Vine Reviews: 15,663
Percentage of 5-Star: 38.7%


## Summary 

Ultimately we are trying to answer the question whether there is bias in the reviews based on whether the review was a Vine Paid Review or not. 

Based on the results, there does seem to be bias. The Vine Paid reviews had nearly 14% more 5-Star Reviews was suggests they are more likely to provide a higher grade for a product compared to the non-paying. 

To further identify the bias, the average star rating should be determined to see if the reviews are higher for those that payed. After calculations, the average star rating of Paid Vine Reviews is 4.2 out of 5 while for Non-Paid Vine Reviews is 3.3 out of 5. This further shows that there is bias in the ratings.
