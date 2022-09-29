# Amazon_Vine_Analysis



### Overview of the analysis:

Amazon has a paid Amazon Vine Program.  SellBy pays a small fee to Amazon and provides its products to Amazon Vine members to publish a review.

We use the reviews of Luggage products on Amazon website to analyze whether the reviews from the members of the Vine Program have the bias statistically.  

We use PySpark to do extract, transform and load data into an AWS Database service with postgresSQL DB.  The data can be accessed via pgAdmin.  After this, we use PySpark to find if the reviews show any bias between Vine program members and non-members.



### Results:

1. customers_table SQL

![customer_table_sql](Resources\customer_table_sql.png)



2. products_table SQL



![products_table_sql](Resources\products_table_sql.png)



3. review_id_table SQL



![review_id_table_sql](Resources\review_id_table_sql.png)



4. vine_table SQL

![vine_table_sql](Resources\vine_table_sql.png)



#### Using PySpark, we find the answers for following questions:



vine program member                                                              non member

![image-20220928214826777](Resources\image-20220928214826777.png)                                                      ![image-20220928214850095](Resources\image-20220928214850095.png)



- How many Vine reviews and non-Vine reviews were there?

​		The number of Vine reviews is 932;

​		The number of non-Vine reviews is 380179.



- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

​		The 5-star Vine reviews is 50;

​		The 5-star non-Vine reviews is 16325.



- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

​		The percentage of 5-star Vine reviews is 5.36%;

​		The percentage of 5-star non-Vine reviews is 4.29%;



### **Summary:** 

The percentage of 5-star Vine reviews is higher than non-vine reviews.  So, there is a positivity bias for Vine reviews.

Due to the fact that the total Vine reviews is much smaller that non-Vine reviews, we need to do a t-test to see if the percentage of 5 stats is within the standard deviation to further support or reject our conclusion.





