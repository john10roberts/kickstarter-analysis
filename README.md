# Kickstarting with Excel

## Overview of Project
Data analysis on crowdfunding projects to uncover hidden trends. 

### Purpose
The purpose of this analysis is to provide some clarity to our friend Louise on what kickstarter projects are successfull.  By providing this information it should prepare Louise to be able to set up her kickstarter campaign to help her new project get off the ground.

## Analysis and Challenges
The initial spreadsheet of the data had 4115rows and 14Columns (columns break down is as follows: ID - Numeric, Name - String, Blurb - String, Goal - Numeric, Pledged - Numeric, Outcomes - String Categorized, Country - String Categorized, Currency - String Categorized, Deadline - DateTime Unix Format, Launched_at - DateTime Unix Format, Staff_Pick - String Categorized, Backers_Count - Numeric, Spotlight - String Categorized, Category and Subcategory - String Categorized).  To begin we will need to convert the deadline and launched_at fields to be a usable date field so added two additional date conversion fields named Date Created Conversion and Date Ended Conversion where we converted the Unix formatted date fields into something that excel can properly display. In addiiton we added a years field by taking the Year of the Date Created Conversion field.  Added another calculated column for Percentage Funded using the Pledged/Goal fields * 100 to show the percentage of the kickstarted that was funded. Also calculated the average donation using Pledged/Backers_Count.  Created two sub fields from the Category and Subcategory field to create a Parent Category and a Subcategory field by splitting category field on "/". Because Louise is specifically looking to create a kickstarter for a theater the analysis was focused on that category. Created a pivottable and chart to explore the theater category in detail in the us.  It showed that there were 525 Successful campaigns (100% Funded), 349 Failed campaigns, 26 Cancelled and 12 live.  Next, we looked closer at the subcategory for just plays from theater kickstarters in the UK.  It showed 238 successful kickstarters, 70 failed and 6 live. Next, we looked at the outcomes of Theater campaigns by launch date.  We were able to determine that campaigns launched in may seemed to be the most successful, while december had the least number of successful campaigns. Lousie at this point wanted a little more information on the Edinburgh Plays all 5 where successful in thier kickstarters.  We then took some measures of central tendency and the mean for successful campaigns was $5049 compared to $10,554 for failed campaigns.  Louise's request is much higher than the mean of a succesful campaign.  In conclusion Louise's project by it being theater project/specifically a play it has a higher likelyhood of success than other categories.  However, the amount of funding sshe is requesting could put her at risk for failure.  If possible, she should look to reduce the amount of funding being requested and plan to launch her kickstarter in May for optimal success. 
### Analysis of Outcomes Based on Launch Date
For the analysis based on launch date we used the year column to allow us to filter the data based on the year the kickstarter was started.  Created a pivot table to show all the successfull, failed and canceled kickstarters.  Then we filtered that by the parent category of theater.  That data showed us again that most successful kickstarters for theaters are at their peak in May.  The successful campaigns start to trail off the following months and hit a low in december.  

### Analysis of Outcomes Based on Goals
For the outcomes based on goals we created a table that would calculate the outcomes of a particular kickstarter based on a range of goals.  The ranges started at under 1000 - greater than 50000.  We then used these groupings to calculate the percentage of kickstarters that suceeded/failed/cancelled.  The data shows that lower goal kickstarters are successful at a much higher rate than.  And while the line chart associated with the data shows that there was an increase in the percentage successful for campaigns from 35-45k the total number of those campaigns are so low that it might be a little misleading just looking at the chart.  It appears that for kickstarters with goals of less than 5k they have the highest odds of success.  

### Challenges and Difficulties Encountered
There didn't appear to be any difficulties or challenges with this data set.  Everything was presented in a logical manner.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
Kickstarters launched in May have the best chance of success.  
Kickstarters launched in December have the smallest chance of success

- What can you conclude about the Outcomes based on Goals?
Kickstarters of less than 5k are the most successful
Kickstarters greater than 5k are the least successful

- What are some limitations of this dataset?
We don't know much information about the kickstarters other than a name and blurb, more information on what it was would be beneficial.  It would also be nice to be able to see the type of donor and maybe some information on the donors to be able to classify the type of person donating. 

- What are some other possible tables and/or graphs that we could create?
Backers to success it would be nice to know if there is any correlation between the number of backers and a projects success. 
Backers Descriptive Statistics 


