# Amazon_Vine_Analysis

## Overview of the Analysis

The purpose of this analysis was to utilize various softwares in conjunction in order to make summarizations about a dataset. 

Amazon's S3 data storage was used to gather a dataset on products reviewed by Amazon. Google Collab was used for PySpark. In the PySpark file, a driver was connected in order to link our Spark Session to Postgres SQL. A database was created in Postgres that linked to a RDS database from AWS. With all of our softwares now linked, the data was imported into our PySpark file. 

The data was cleaned and 4 new dataframes were created to match the schemas we created in Postrgres. Using the driver, the cleaned dataframes were written into Postgres into our empty tables schemas. From here, we selected one table for further analysis. 

This table was exported as a CSV and loaded into a jupyter notebook. Using pandas, more data filtering occured so that we could answer a few questions about the data. 

This final dataframe was a table that showed each reveiw id, with the associated star rating, number of helpful votes, total number of votes, whether it was a verified purchase, and finally whether they were a apart of the paid Vine review program. 


## Results

After some filtering to ensure we were working with good data, the dataframe was split into reviews by paid Vine reviews and non paid Vine reviews...



## Summary 
