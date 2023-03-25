# Big Data Analytics Challenge: 

## **Overview:**
The current project determines the software reviews from the US and more importantly determines the contribution of the vine program. The Amazon vine program invites insightful reviewers who give unbiased honest reviews of on all amazon products. The percentage of vine reviewers are considerably small compared to the overall count of reviewers. The following results are evaluated.

1.	Total number of reviewers or members in the vine program compared to non-members.
2.	Total number of 5-star reviews given by vine program members compared to non-members.
3.	Percentage of 5-star reviews given by vine program members compared to nonmembers.

## **Data preprocessing:**

The vine.csv is extracted from the aws server in postgres sql. The csv file is imported into pandas datafram and the preprocessed on the following conditions:
1.	The ratio of total reviews is first filtered to be greater than 20.
2.	The ratio of helpful_reviews to total_reviews is calculated. The first step in preprocessing is to prevent division errors and to set the minimum threshold to 20. 
3.	The ratio of helpful to total reviews >= 50% is filtered. Essentially only reviewers who provide atleast useful reviews atleast 50% of the time are chosen for both vine program members and non-members. 
4.	Based on these preconditions, two separate dataframes one of vine member and the other for vine nonmembers are created.
Finally, the three results listed in the overview are determined.

## **Total number of reviews:**

The vine program members are considerably smaller(231) compared to non-vine members(16,464). It makes sense because, vine membership is only upon invitation by Amazon who are assessed based on their ability to give useful reviews. 

## **Total number of 5-star reviews:**

The number of 5-star reviews by vine members totals to 93 compared to 4867 for non-vine members. Though the actual numbers are small, it stems from the variable sample size of each group, hence its important to calculate the percentage 5-star reviews for both the groups.

## **Percentage 5-star reviews:**

The percentage of 5-star reviews by vine members is about 40% compared to 30% by non-vine members. Now it becomes clear that vine members offer 10% more 5-star reviews than non-vine members.

## **Pitfalls of the study:**

This is very broad analysis and like any other research demands further scrutiny of the data. Some of the follow up studies are:

1.	To evaluate the usefulness of the reviews by a vine non-member: 5-star review does not automatically mean they are useful. A review which describes the pros and cons of a product is more useful than just saying “great product.”
2.	Scrutinize the vine members: Though vine members almost have a prerogative in decisively giving a review, this can lead to complacency as well. Again further evaluating the usefulness of the review is vital. 
