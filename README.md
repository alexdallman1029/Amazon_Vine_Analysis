# Amazon Vine Analysis
## Overivew
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies can pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

The purpose of this analysis was to look at reviews of tools on Amazon and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Finally, PySpark will be used to determine if there is any bias toward favorable reviews from Vine members in the dataset.

## Results

<b>Vine and Non-Vine Data</b>
```
+----+-------------+--------------------+-----------------+
|vine|Total_Reviews|Total_5_Star_Reviews|%_5_Star_To_Total|
+----+-------------+--------------------+-----------------+
|   Y|          285|                 163|57.19298245614035|
|   N|        31542|               14614| 46.3318749603703|
+----+-------------+--------------------+-----------------+
```

* How many Vine reviews and non-Vine reviews were there?
  * There were 285 Vine reviews and 31,542 non_Vine reviews.<br><br>

* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
  * There were 163 5-star Vine reviews and 14,614 5-star non-Vine reviews.<br><br>

* What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
  * About 57% of Vine reviews were 5-star reviews, and about 46% of non-Vine reviews were 5-star reviews.<br><br>

## Summary
According to the table, Vine members did show slight positive bias when rating their products, but there was only about a 10% difference between Vine and non-Vine members. We could assume that Vine members are slightly more likely to rate a tool on Amazon with five stars.

For additional analysis, if you were to run the same analysis on different catergories of products, you could better understand if reviews made by Vine members are bias.
