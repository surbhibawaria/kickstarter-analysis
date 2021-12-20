# Kickstarting with Excel

Performing analysis on Kickstarter data using Excel to uncover trends.

## Overview of the Project
Louise, who wanted to start a crowdfunding campaign to help fund her play _Fever_ estimated a budget of over $10,000 and was understandbly hesitant about jumping into her first fundraising campaign. So to help Louise kickstarting her production, crowdfunding data was analyzed and organized to make the campaign successful and help her gain a better undderstanding of the campaigns from start to finish.

In a short amount of time, Louise's play _Fever_ came close to reaching its fundraising goal, and now she wanted to know how different campaigns performed in terms of their launch dates and funding goals.

### Purpose
The purpose of this analysis is to visualize campaign outcomes based on their launch dates and their funding goals and help Louise understand the trends in order to help her kickstart her production.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To analyze outcomes based on launch date, first a new column "Years" was created. In the "Years" column, used the _YEAR()_ function to extract the year from the “Date Created Conversion” column. A pivot table from the _KickStarter_ worksheet was created in a new sheet and filtered based on "Parent Category" and "Years". The column labels were filtered to show only "successful", "failed" and "canceled". Then the "Parent Category" was filtered for the "theater" data. 


![Screen Shot 2021-12-18 at 11 24 24 PM](https://user-images.githubusercontent.com/95826875/146663816-7015da33-c556-443d-aee1-a98f45ee3fd7.png)



A line chart was then created based on the pivot table to visualize the data for a better understanding, showing the trends of successful, canceled and failed outcomes through January to December for _theaters_.



![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/95826875/146661822-5390724d-ba24-4f2a-8687-166f4b3afb86.png)





### Analysis of Outcomes Based on Goals
To analyze outcomes based on goals, a new sheet was created with eight columns holding the data for,
1. Goal
2. Number Successful
3. Number Failed
4. Number Canceled
5. Total Projects
6. Percentage Successful
7. Percentage Failed
8. Percentage Canceled

In the “Goal” column, created the following twelve rows for dollar-amount ranges so projects can be grouped based on their goal amount,
1. Less than 1000
2. 1000 to 4999
3. 5000 to 9999
4. 10000 to 14999
5. 15000 to 19999
6. 20000 to 24999
7. 25000 to 29999
8. 30000 to 34999
9. 35000 to 39999
10. 40000 to 44999
11. 45000 to 49999
12. Greater than or equal to 50000

Used _COUNTIFS()_ functions to populate the "Number Successful", "Number Failed", and "Number Canceled" columns by filtering on the Kickstarter "outcome" column, on the "goal" amount column using the ranges created and on the "Subcategory" column using "plays" as the criteria. Then used the _SUM()_ function to populate the "Total Projects" column with the number of successful, failed, and canceled projects for each row and calculated the percentage of successful, failed, and canceled projects for each row. 



![Screen Shot 2021-12-18 at 11 24 45 PM](https://user-images.githubusercontent.com/95826875/146663834-6d52214a-6b00-4c09-9b97-04d041f69586.png)


A line chart was then created with the goal-amount ranges, the percentage of successful, failed, or canceled projects, displaying the rate of success and failure within the various ranges.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/95826875/146662539-e2d05e42-594f-4fa1-9479-ea16861627e3.png)


### Challenges and Difficulties Encountered

The challenge here was to guide Louise in her campaign only on the basis of launch date, and dollar-amuont of goal/pledged didn't predict rate of success. The dataset has some outliers which were not specifically representing the data required to analze for Louise's play. Hence, to overcome outliers were identified.


![Screen Shot 2021-12-19 at 4 55 59 PM](https://user-images.githubusercontent.com/95826875/146692189-60ea3b7e-7e37-4400-860a-c8b777739b20.png)



## Results

### Conclusions about the Theater Outcomes by Launch Date


![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/95826875/146666721-549acb16-1402-4f22-a79b-989c4f016f72.png)


After analyzing the data of _theater outcomes by launch date_ , following conclusions can be drawn.

1. Based launch date, the campaigns have higher success rate trends in the months of May, June, July and lower success rate trends in January, March, September, November. Hence, starting a _theatre_ campaign in May, June, July suggests the highest success rate over the other months of the year.
2. The month of December have lowest success rate and seems to have similar outcomes for both the success and the failure of the campaigns.

### Conclusions about the Outcomes based on Goals


![Outcomes_vs_Goals](https://user-images.githubusercontent.com/95826875/146667358-f2c13d33-7e72-47c2-8e63-b0336344857f.png)

After analyzing the data of _outcomes based on goals_, the success rate of plays seems to be 75% if the goal is $1000, it is 60% if the goal is $5000. But, if the goal is increased to say upto $19000 to $20000 the success rate will drop to 50%. And with the further higher campagin goal range of $25000, $45000 or above there is higher chances of campaigns to be a failure. Therefore, it can be concluded that theatre play campaign might have a higher chance for becoming a success if the campaign goals are kept as limited as possible.

### Limitations

Although the dataset represented good contribution to analysis, but there are limitations to the kickstarter data. 

There was no recent data available for the past few years which could have helped with a better analysis of the current trends. 
Additional data from the social media platforms and public reviews would have also helped. 

Categorizing the theater plays even further like Romance, Thriller, Comedy etc, would have helped in a deeper analysis. 
Also, the data is sourced from multiple countries with their corresponding currency, so data normalization of the different currencies for a better outcome.

### Recommendation

For a better analysis of data, additional tables and graphs would have been more helpful. Like, outcomes based on _staff_pick_ can be analyzed to visualize if that affects the success or failure rates of the campaigns. 

Another one could be the outcomes based on the _country_ or _backers_count_. Would these affect the success and failure of the campaign? Would backers count affect the outcomes? Is there any country specific trend which can contribute to success or failure of the campaigns? 

Creating a table and graph visualizing average donation across campaign outcomes.

Box plot would have been created for successfully funded plays.


