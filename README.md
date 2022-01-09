# Amazon Vine Analysis
## Purpose:
---
Extracting data to perform an ETL process before loading into a AWS RDS.  
Then examine data to determine if any biases exist from Vine reviews. 

### Overview of the analysis: 
---
The exercise has two technical deliverables.  The first was and ETL processes, 
to extract Amazon reviews from 50 different product areas.  I chose to use 
review for outdoor equipment.  The data contained almost 45,000 products and 
over 2,300,000 reviews.  After extracting the data from AWS S3 storage, I 
cleaned and transformed the data into 4 different tables before loading to 
a PostgreSQL Database also hosted in AWS RDS to be used for further analysis. 
The second deliverable was to determine if any of the paid Vine reviews makes 
a difference in the percentage of 5-star reviews. To do this I needed to capture 
the Vine reviews and non-Vine reviews.  To complete the analysis, I used PySpark 
to filter the reviews.     
### Results: 
---
•	There were 107 Vine reviews for products with more than 20 ‘helpful reviews’ 
and 38869 reviews from non-Vine participants. 

![Count of Reviews by Type](/images/count_reviews.png)
•	There were 56 5-Star reviews from Vine members and 21005 5-start reviews from 
those who are not part of the Vine program.

![Count of 5-star Reviews by Type](/images/5-star_review.png) 
•	The percentage of Vine Reviews that were 5-star ratings is  52.69% and the 
percentage of non-vine reviews is 52.34%

![Percentage of 5-star Reviews by Type](/images/percent.png)


### Summary: 
My analysis showed there was not any positivity bias for reviews in the Vine 
program because there was not any significant different in the 5-star rating 
between members of the Vine program and those that are not members.
