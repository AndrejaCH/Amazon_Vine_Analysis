# Amazon Vine Review Analysis
*Analysis with Pyspak and AWS*

Note: Password from Amazon_Reviews_ETL.ipynb file is deleted for safety reason. File needs pgAdmin password in order to run. 

## Project Overview
For this project I am using Amazon’s cloud service AWS, Google Colab and Pyspark to analyze Amazon’s reviews for outdoor products. The purpose of this analysis is to determine if there is any bias toward favorable reviews from Vine members. Amazon Vine program is a service that allows manufactures, for additional fee, to have review posted on Amazon for their pre-release items.  

## Resources
Data Source

-	[Amazon Vine Reviews for outdoors items](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Outdoors_v1_00.tsv.gz)

Software:

-	Google Colab [Vine_Review_Analysis.ipynb](Vine_Review_Analysis.ipynb)
-	PgAdmin
-	AWS [Amazon_Reviews_ETL.ipynb](Amazon_Reviews_ETL.ipynb)

Languages:

-	pySpark

## Results
In this analysis we analyzed reviews that have more than 20 total votes and the percentage of helpful votes is equal or greater than 50.

***How many Vine reviews and non-Vine reviews were there?***

There were
- **107 Vine** reviews and 
- **39,869 non-Vine** reviews.

<p align="center">
<img src="Graphics/TotalRevievs.PNG" width="50%" height="50%">
</p>

<p align="center">
<i>(Figure 1: Total Vine and non-Vine reviews.)</i>
</p>


***How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?***

There were
- **56** five stars **Vine** reviews and 
- **21,005**  five stars **non-Vine** reviews.

<p align="center">
<img src="Graphics/5stars.PNG" width="50%" height="50%">
</p>

<p align="center">
<i>(Figure 2: 5-star Vine and non-Vine reviews.)</i>
</p>

***What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?***

- **52.34 %** of **Vine** reviews were 5 stars and 
- **52.69 %** of **non-Vine** reviews were 5 stars.

<p align="center">
<img src="Graphics/Percentage.PNG" width="60%" height="60%">
</p>

<p align="center">
<i>(Figure 3: Percentage of 5-star Vine and non-Vine reviews.)</i>
</p>


## Summary

The purpose of this analysis is to analyze if there is any bias toward favorable reviews from Vine members in the dataset. We analyzed reviews that have more than 20 total votes and the percentage of helpful votes is equal or greater than 50. We made this selection in order to pick reviews that are more likely to be helpful.

**Positivity bias for reviews in the Vine program**

In the analysis we analyze 5-star reviews within conditions mentioned above. Calculations show that there is **no positivity bias for reviews in the Vine program**. The results show that percentage of 5 stars Vine reviews is 52.34% and percentage of 5 stars non-Vine reviews is 52.69%. **Non-Vine reviews** have slightly **higher percentage** of the of the 5 stars reviews, **0.35% percentage points** to be exact.

**Additional analyses and suggestions**

We could expand this analysis by calculating percentage for all stars reviews. Based on the results (Figure 1), there is a larger difference in percentage for 1-star reviews than for 5-stars reviews. Vine reviews have only 0.93% of 1-star review, while non-Vine reviews have 13.35 % 1-star reviews within conditions mentioned above. Similarly, there are less 2-stars Vine reviews (1.87%), than for non-Vine reviews (6.05%).  
<p align="center">
<img src="Graphics/Percentageallstars.PNG" width="60%" height="60%">
</p>

<p align="center">
<i>(Figure 4: Summary table for all star reviews.)</i>
</p>

The results show that there could be positivity bias for reviews in the Vine program, when looking from 1 and 2-star perspective. 
Additionally, I would suggest another analysis beyond the given dataset. Non-vine reviews outnumber Vine reviews for 37,260 % (in this dataset, within certain conditions). In this case Vine reviews won’t affect the overall rating of the item. On Amazon site for Vine reviews (https://www.amazon.com/gp/vine/help)[https://www.amazon.com/gp/vine/help] we can find explanation about the Vine program. The first sentence states: “Amazon Vine invites the most trusted reviewers on Amazon to post opinions about new and pre-release items to help their fellow customers make informed purchase decisions (1).” Vine reviews could have impact on newly released items sold on Amazon. For the manufacturer and their newly released products might be beneficial to have some reviews posted. At this point I would suggest to perform analysis on items that are similar (one with a Vine reviews and one without) and measure sales increase over time. Based on that we could observe if Vine reviews contributed to faster increase of the sales of newly released items. 

# References
-	(1) Amazon.com https://www.amazon.com/gp/vine/help , Web 31 Oct 2020.
