# Uploaded the Kickstarter.xlxs

# Kickstarting with Excel

## Overview of Project

The purpose of our Kickstarter Analysis was to measure how different campaign outcomes performed in relation to their launch dates and funding goals for Louise. Louise had previously fallen short of her funding goal for her play ‘Fever’ and wanted to know where other campaigns measured up with the parameters.


### Purpose

Using the data from the kickstarter worksheet we wanted to visualize the relationship between theater outcomes based on their launch dates and funding goals.

## Analysis and Challenges

Some of the challenges I faced during this analysis was converting our ‘years’ data in the ‘Theater Outcomes by Launch Date’ pivot table. This was tricky at first because it took some cunning maneuvers within the table filters to get the table to report it. To do this I dragged the ‘date created conversion’ data into the rows column and then removed the quarters and years from the table.  After this it was smooth sailing, I took the data and converted it into a line chart which can be viewed below: 

![Theater_Outcomes_Based_vs_Launch](https://user-images.githubusercontent.com/101610050/159551193-92b7f1dc-568f-4347-b107-fd4fd1443064.png)


 In the second portion of my analysis, where we were measuring outcomes based on goals, I had to create a formula to count the number of successful, failed, and canceled plays based on their funding goals.  Creating this formula took some patience, but ultimately came up with the following syntax which was adjusted according to each rows parameters, and each outcomes key word (successful,failed,canceled) **: =COUNTIFS(Table1[goal],">=0",Table1[goal],"<=999",Table1[outcomes],"Successful",Table1[Parent Category],"theater",Table1[Subcategory],"plays").** 


### Analysis of Outcomes Based on Launch Date

If we look at the line chart Theater_Outcomes_Based_on_Launch_Date.png
We can see the relationship between launch dates and success/failure rate.  Theater campaigns had a consistent success rate between the months of Jan-April, and then a steep increase in the month of May before steadily decreasing through the summer and leveling out in the fall. The launch date didn’t seem to affect the failure rate of theater campaigns as we see a consistent failure rate year-round. Lastly, it can be inferred that launch date had little to no effect on whether theater campaigns were canceled or not.

 
![Theater_Outcomes_Based_vs_Launch](https://user-images.githubusercontent.com/101610050/159551336-8b859acd-2485-4575-a56c-9dc75747539c.png)



### Analysis of Outcomes Based on Goals

My analysis of Outcomes Based on Goals yielded some interesting results in comparison to our first analysis based on launch date.  As we can see in the Outcomes_Based_on_Goals.png chart below: There is a direct inverse relationship between success and failure rates when a play meets its funding goal or not.  This would make perfect sense as we would expect a project to fail without proper funding.  Funding goals, however, had no effect on whether the play was canceled. 
 
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/101610050/159551385-9b2d7db0-8611-4c5c-ac55-36c126d5620a.png)


### Challenges and Difficulties Encountered

Some of the challenges I ran into during this analysis were outlined in the “Analysis and Challenges” section: but to quickly summarize them: 1.) Converting the years to months in the pivot table used for outcomes based on launch date. 2.) crafting the initial formula for counting successful;,failed,canceled plays based on their funding goals. The syntax can also be found in the “Analysis and Challenges” section. 


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

Two outcomes that could be drawn from the Outcomes based on Launch Date analysis are:
1.)	Based on the Data we can infer that theater campaigns launched in the month of May are more successful than any other month of the year
2.)	Theater campaign cancellations have no significant correlation to the launch date


- What can you conclude about the Outcomes based on Goals?

It can be inferred that when a play campaign does not meet its funding goal that it directly correlates to the probability that the play will fail.


- What are some limitations of this dataset?

Some of the limitations of this dataset are that we don’t have an equal number of units per month to confidently say which months are better for release than others.  If we had an equal sample size of theater campaigns released in each month, we could fairly analyze the trends more accurately.  So, we could be skewing the data in that regard.

- What are some other possible tables and/or graphs that we could create?

Another chart that would be useful is Outcomes based on Backers_count, this way we could visualize the importance of getting donations and measuring their success rate against this, I would imagine this would reflect our Outcomes Based on Goal chart.

