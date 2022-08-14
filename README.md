Kickstarting with Excel: A Written Analysis for the "Kickstarter Analysis" Project
  
  Overview of Project
    
    Purpose:
    The purpose of this project was to help Louise, the owner of a successful Kickstarter campaign for her play "Fever", figure out how different campaigns for similar projects ended up. I was able to take a sample of over 4000 different Kickstarter campaigns to provide her with ample detail on campaigns with varying data points for the projects name/discription, pledged funds vs. goals, outcomes, country/currency, deadline, launch date, whether it was a staff pick or not, number of backers, spotlight status, parent categories and subcategories, percentage funded, and average donations. These data points are filled into multiple colums on the excel sheet and allowed me to come up with two major findings. The first was for Theater Outcomes based on Launch Date and the second was for Outcomes Based on Goals so that, should Louise launch another campaign, she will know the most optimal way to do so in order to get her project funded.
  
  Analysis and Challenges
  
    Analysis of Outcomes Based on Launch Date:
    When working on Outcomes Based on Launch Date, I was able to form a pivot table. Before going ahead and forming the table, I had to use the formula =YEAR(@S:S). This formula allowed me to pull the year out of the Date Created Conversion column on the data spreadsheet. This was crucial for the fomration of the pivot table. The table was set up using Years and Parent Category as the Filters, Outcomes for the Columns, Date Created Conversion for the Rows, and Count of Outcomes for the Value. Since we were looking at completed campaigns, the Live option for values was filtered out and the Outcome columns were aranged decending to show Successful campaigns first followed by failed, canceled, and grand total. The data rows were laid out by months, this was achieved by getting rid of the years and quarters options in the Row field when originally adding Date Created Conversion to the field. The chart can be seen below. 
    ![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/111014191/184519347-b21fd496-3505-4dc7-9d64-1bed3cc36df0.png)
    
    Analysis of Outcomes Based on Goals: 
    When working on the Outcomes Based on goals, I ended up using a few formulas that would end up creating a table of data to pull from when creating a chart. To start off, I created a table with columns for Goals, quatity successful/failed/canceled, total amount of projects, and the percentage successful/failed/canceled. The rows were arranged for less than 1000, 1000-4999, 5000-9999, 10000-14999, 15000-19999, 20000-24999, 25000-29999, 30000-34999, 35000-39999, 40000-44999, 45000-49999, and greater than 50000. In order to filter out the data for only finding successful plays in the given goal ammount, I used the line of code =COUNTIFS(Data!$D:$D,"<1000", Data!$F:$F,"successful",Data!$R:$R, "plays"). The first bit of that pulls data out that is less than 1000 in the goal column on the main sheet, the second portion filters out succesful campaigns from the outcomes column, and the final portion specifies that we only want to keep track of campaigns with the subcategory of play. Upon finishing this for all the rows, I moved on to the next two columns. Here is a line of code for example from each. =COUNTIFS(Data!$D:$D,">=20000", Data!$D:$D, "<=24999", Data!$F:$F,"failed",Data!$R:$R, "plays") and =COUNTIFS(Data!$D:$D,">50000", Data!$F:$F,"Canceled",Data!$R:$R, "plays"). Under the total projects column, I used the =SUM formula to add up all three outcomes from the previous =COUNTIFS formulas, an example of such would be =SUM(B2:D2). This total would serve as the base in calculating the percentages using simple arithmatic to find out the percentages rounded to the nearest whole integer for successful, failed, and canceled campaigns. This can be seen in the chart below.
    ![Outcomes_vs_Goals](https://user-images.githubusercontent.com/111014191/184519608-e8e45c2a-0de9-4d0d-8bcd-91a12a72f47a.png)
    
    Challenges and Difficulties Encountered: 
    During my time on this sheet, I suffered a single small issues. I accidentally had based my pivot table in the first section off of the Date Ended Conversion. All the data in my Grand Total Row was accurate but, the data poins on the rest of the table were off. After reviewing the chart once again, I realized what mistake I had made and swapped in the right variable to get the correct talbe and graph. 
  
  Results
    
    What are two conclusions you can draw about the Outcomes Based on Launch Date?
    
    What can you conclude about the Outcomes based on Goals?
    
    What are some limiations of this dataset?
    
    What are some other possible tables and/or graphs that we could create?
