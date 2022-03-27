# Kickstarting with Excel

## Overview of Project
This project is a data analysis of Kickstarter campaigns for our client Louise. We mainly focused on US theater Kickstarter campaigns, with a brief look into the Great Britain theater Kickstarter market. The data has been filtered and organized into several charts and tables to provide Louise the most releveant information to make her decision.

### Purpose
Louise contracted us for this analysis to determine what her Kickstarter goals should be for her upcoming play Fever. She had estimated she needed about $10,000 for her play but was unsure how realistic reaching that goal would be. Our job was to analyze the data of relevant Kickstarter campaigns from 2009-2017 to help Louise create a successful campaign that would get fully funded. 

## Analysis and Challenges
![row number](https://user-images.githubusercontent.com/100237685/160289864-c1ee1550-9c60-42fa-88b1-638be0bbba88.png)

![column number](https://user-images.githubusercontent.com/100237685/160289913-a5db9f72-2d20-4bb1-847b-e1681bfb6254.png)

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/100237685/160289920-94d79418-43ba-4c8f-807e-e22c23c269dd.png)

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/100237685/160289933-22f99658-0f8d-47dd-a763-8466ff3451d0.png)

![theater outcomes v goals](https://user-images.githubusercontent.com/100237685/160290178-3cb20f8f-8e7e-4515-a7c6-553ef0c94c5b.png)

![outcomes launch date pivot table issue](https://user-images.githubusercontent.com/100237685/160290635-19010a91-3880-4a00-8c15-015d301cabdb.png)



### Analysis and Challenges of Outcomes Based on Goals
Completing this analysis was challenging because there were 4113 campaigns and 21 descriptive data columns those campaigns were sorted into. As such, I would often run into errors when attempting to filter and sort the data. For example, when trying to sort the Outcomes based on Goals, I had a hard time finding the correct formula that would meet all of the criteria I needed. On my first attempt I tried using =COUNTIF(Kickstarter!F:F,"successful",Kickstarter!D:D,">=1000","<=4999". However, it quickly returned an error message letting me know I didn't input enough criteria. After a quick Google search I realized that each criteria needed its own reference point. This meant that I couldn't have "Kickstarter!D:D" just for ">=1000", I also needed it for "<=4999". Once I corrected the formula to =COUNTIF(Kickstarter!F:F,"successful",Kickstarter!D:D,">=1000",Kickstarter!D:D"<=4999" it was able to output the information I needed. Once that correction was made, I was able to adjust the formula for each row until I had my entire table filled out. I would like to add that the instructions told me to first add a filter to the Outcomes column seperating "failed", "successful", and "cancelled" each time I wrote the forumla, but I was worried that data would be excluded or mixed up if I did this so I applied no filters to the Outcomes column when writing my formula. 

### Analysis and Challenges of Outcomes Based on Launch Date
Analyzing the Outcomes based on Launch Date was fairly starightforward, if not tedious. The data from the main Kickstarter sheet had to be filtered and modified a few times before I was able to create a pivot table and chart. I had to translate the Unix Timestamps to a traditional date format, and then again filter that out to just the years. Additionally, I had to filter the Category and Subcategory column into seperate Parent Category and Subcategory columns. Once all of that was completed, I was then able to create my pivot table and chart. Unfortunately, when I went to create the pivot table, the Row Lables were organizing by the year and not the month like the directions requested. It took messing with the pivot table features for a few minutes before I realized I could just delete the Quarters and Years lables to have it display only the months. Once those corrections were made it was easy to create the chart from the table.  

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  
  From the data gathered, it would appear that May or June is the best month to start a theater Kickstarter campaign. The worst month appears to be December.  

- What can you conclude about the Outcomes based on Goals?

  Based on the data, it would appear campaigns that have a goal of less than $1,000 have the highest success rate at 71%. For Lousie's goal of $10,000, there's a 48% chance she will be successful. 

- What are some limitations of this dataset?

  This analysis only looks at quantitative data, not qualitative data. The success of these campaigns aren't just dictated by their amount; their success/failure could have also been related to the public interest in the premise of the campaigns, the popularity of the campaign founders, the economic state at the time of the campaigns, how much marketing went into advertising the campaigns, etc. Looking at the numbers alone does not give us a clear picture of why these campaigns met their goals or not. 

- What are some other possible tables and/or graphs that we could create?

  I believe another table/graph that could be added is one that is an intersection of the Outcomes Based on Goals and the Outcomes Based on Launch Date data sets. I want to know: does the goal amount matter depending on the time of year? For example, did December have a high fail rate because campaigns were asking for too much money during the holiday season? For Louise's goal of $10,000 which month has had the most success for campaigns similar to that goal amount? 
