# Kickstarting with Excel: A Written Analysis for the "Kickstarter Analysis" Project
## Overview of Project
### Purpose:
The purpose of this project was to help Louise, the owner of a successful Kickstarter campaign for her play "Fever", figure out how different campaigns for similar projects ended up. I was able to take a sample of over 4000 different Kickstarter campaigns to provide her with ample detail on campaigns with varying data points for the projects name/description, pledged funds vs. goals, outcomes, country/currency, deadline, launch date, whether it was a staff pick or not, number of backers, spotlight status, parent categories and subcategories, percentage funded, and average donations. These data points are filled into multiple columns on the excel sheet and allowed me to come up with two major findings. The first was for Theater Outcomes based on Launch Date and the second was for Outcomes Based on Goals so that, should Louise launch another campaign, she will know the most optimal way to do so in order to get her project funded.
## Analysis and Challenges
### Analysis of Outcomes Based on Launch Date:
When working on Outcomes Based on Launch Date, I was able to form a pivot table. Before going ahead and forming the table, I had to use the formula =YEAR(@S:S). This formula allowed me to pull the year out of the Date Created Conversion column on the data spreadsheet. This was crucial for the formation of the pivot table. The table was set up using Years and Parent Category as the Filters, Outcomes for the Columns, Date Created Conversion for the Rows, and Count of Outcomes for the Value. Since we were looking at completed campaigns, the Live option for values was filtered out and the Outcome columns were arranged descending to show Successful campaigns first followed by failed, canceled, and grand total. The data rows were laid out by months, this was achieved by getting rid of the years and quarters options in the Row field when originally adding Date Created Conversion to the field. The chart can be seen below. 
    ![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/111014191/184519347-b21fd496-3505-4dc7-9d64-1bed3cc36df0.png)
### Analysis of Outcomes Based on Goals: 
When working on the Outcomes Based on goals, I ended up using a few formulas that would end up creating a table of data to pull from when creating a chart. To start off, I created a table with columns for Goals, quatity successful/failed/canceled, total amount of projects, and the percentage successful/failed/canceled. The rows were arranged for less than 1000, 1000-4999, 5000-9999, 10000-14999, 15000-19999, 20000-24999, 25000-29999, 30000-34999, 35000-39999, 40000-44999, 45000-49999, and greater than 50000 (these categories are the cost in dollars for each campaign). In order to filter out the data for only finding successful plays in the given goal ammount, I used the line of code =COUNTIFS(Data!$D:$D,"<1000", Data!$F:$F,"successful",Data!$R:$R, "plays"). The first bit of that pulls data out that is less than 1000 in the goal column on the main sheet, the second portion filters out succesful campaigns from the outcomes column, and the final portion specifies that we only want to keep track of campaigns with the subcategory of play. Upon finishing this for all the rows, I moved on to the next two columns. Here is a line of code for example from each. =COUNTIFS(Data!$D:$D,">=20000", Data!$D:$D, "<=24999", Data!$F:$F,"failed",Data!$R:$R, "plays") and =COUNTIFS(Data!$D:$D,">50000", Data!$F:$F,"Canceled",Data!$R:$R, "plays"). Under the total projects column, I used the =SUM formula to add up all three outcomes from the previous =COUNTIFS formulas, an example of such would be =SUM(B2:D2). This total would serve as the base in calculating the percentages using simple arithmatic to find out the percentages rounded to the nearest whole integer for successful, failed, and canceled campaigns. This can be seen in the chart below.
    ![Outcomes_vs_Goals](https://user-images.githubusercontent.com/111014191/184519608-e8e45c2a-0de9-4d0d-8bcd-91a12a72f47a.png)
### Challenges and Difficulties Encountered: 
During my time on this sheet, I suffered a single small issue. I accidentally had based my pivot table in the first section off of the Date Ended Conversion. All the data in my Grand Total Row was accurate but the data points on the rest of the table were off. After reviewing the chart once again, I realized what mistake I had made and swapped in the right variable to get the correct table and graph. 
## Results
### What are two conclusions you can draw about the Outcomes Based on Launch Date?
You can draw that for the most part, successful and failed campaigns move up and down in count together. What this tells us is that there really isn't a bad time of the year to launch your campaign as long as you have a product that people will want to pay for. The outlier here is May - July where the funded campaigns are at a much higher mark than the failed ones. The second conclusion here is that the best time to launch your campaign is in the late spring/summer timeframe. Not only are there a large amount of campaigns being funded during this time, but there are a lower percentage of total campaigns failing. The best Month out of these is May followed by June. If Louise wanted to launch another campaign for a play, doing so in May or June would be the best time to do so.
### What can you conclude about the Outcomes based on Goals?
The data seems to trend down from the price category Less than 1000 being the highest to $25,000 to $29,999 being the lowest portion of this consistent negative decline. After that, the chart rises again and falls. To explain the end of the graph, there isn't much of a statistical trend to draw off of but, the beginning of the graph makes it pretty obvious that you have a better chance at getting your campaign funded based on cost. Projects less than $1,000 were funded 76% of the time while projects priced between $25,000 and $29,999 were only funded 20% of the time. Unless you can count on a wealthy donor or a wealthy market in general that may be willing to splurge on your campaign, you are best off keeping your project as cheap as possible.
### What are some limitations of this dataset?
The data here is limited by the nature that it was created in, crowdfunding. While this is a great way to generate funds for a project, there are other means that a creator could raise money for their project. One form of media could be really successful on crowdfunding while other forms could be better suited for a client based system. While the point of this research was to find information based on crowdfunding, one category's lack of performance could dissuade Louise from wanting to go that route for her next campaign when in reality, she could find an equal amount of success by raising the money in other ways. 
### What are some other possible tables and/or graphs that we could create?
Another useful graph that would be interesting to look at would be a pie chart showing all of the successfully funded projects broken down by their parent category and subcategory. This would be useful information to provide Louise with should she want to launch multiple different campaigns/work on multiple projects. This would allow her to figure out which formats would give her the best chance at success since she would be having to put in a lot of work in order to get the projects funded. 
