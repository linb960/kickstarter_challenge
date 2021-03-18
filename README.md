# Kickstarter Analysis of Outcomes Based on Goals and Launch Date
### This project determines how well Kickstarter Campaigns for theatre projects did based on their launch date.  It also includes outcomes based on funding goals for play productions within the theatre category.
## Analysis and Challenges
The <a href="Kickstarter_Challenge.xlsx">dataset</a> that was analyzed for this project is a subset of Kickstarter challenge data dated from 2009 to 2017.  Although this data contains many different categories the analysis is based spefically on the "theatre" category and the "plays" subcategory.  The initial set of data contained information for each campaign about the following:
**Name**, **Blurb**, **Goal**, **Pledged**, **Outcomes**, **Country**, **Currency**, **Deadline**, **Launched At**, **Staff Pick**, **Backers**, **Spotlight**, 
**Category/Subcategory**, **Percentage Funded** and **Average Donation**. <br><br>
The **Deadline** and **Launched At** dates were provided as Unix timestamps.  Two new columns were created **Date ended conversion** and **Date created conversion** and the Unix times were converted to the format Month, Day, Year and added to the two new columns respectively. A **Year** column was also added which pulled out the year of the Launch date. <br><br>
It was also necessary to split **Category/Subcategory** into two new columns one for **Category** and one for **Subcategory** in order to be able to look at the Theatre category for one analysis and the Play subcategory for the other.<br>

### Analysis of Outcomes Based on Launch Date
In order to properly provide an analysis of the theatre outcomes by launch date a pivot table was used.   A filter was added for category, theatre, and the year.  The next step is to determine if the Kickstarter campaign is a success, failure or canceled. The **Outcomes** column of the main spreadsheet contains this information and is used.  This measurement is based on whether the amount pledged met the goal desired.  The total number of successes, failures and canceled theatre campaigns are calculated by the month the campaign was launched and each month is a row in the pivot table.  Here is the table with these parameters.
<p align="center">
  <img src="Screenshots/Outcome_on_date.png" width="350" height="300"><br>
</p>This line chart is then created to visulize the output.  Herecan the blue line is for successes, the red line represents failures and the yellow line shows those that were canceled.  By looking at the chart it is easy to see that the month of May was the most successful for theatre campaigns, while the month of December was the least successful.
<p align="center">
  <img src="Resources/Theater_Outcomes_vs_Launch.png" width="620" height="333">
  
### Analysis of Outcomes Based on Goals
Another part of the analysis was to determine the number of successful, failed, and canceled theatre projects that were specifically play productions.  Instead of looking at launch date for this analysis the **Goal** column from the dataset was used.  The dollar amount is broken down into 12 rows.  Starting with goals less than 1000 and moving up in increments of 5000 all the way to goals greater than 50000.  The total number of successful, failed and canceled projects are then calculated based on the parameters of the goal.  To find, for example, how many successful play projects there were in the goal range from 1000 to 4999, a **COUNTIF** statement is used that is as follows.<br>
=COUNTIFS(Kickstarter!F:F,"successful",Kickstarter!D:D,">=1000",Kickstarter!D:D,"<=4999",Kickstarter!R:R,"plays")<br><br>
This says that from the primary sheet "Kickstarter" count based on the **Outcomes** is "successful", the **Goal** is "greater than 1000 and less than 4999" and the **SubCategory** is "plays".   Here is a screenshot of the spreadsheet for all the calculations.
<p align="center">
  <img src="Screenshots/Outcome_on_goal.png" width="675" height="262"><br>
  </p>
  The line chart was then created from looking at the total number of projects and calculating the precentage successful, precentage failed and precentage canceled.
  For example for 388 successful projects in the 1000-4999 range, there were a total of 534 total projects and a precentage of successful of 388/534 which equals 73%.  Based on the output of all the data into the chart it is easy to glean that projects asking for less money are more successful.  More on conclusions below.
<p align="center">
  <img src="Resources/Outcomes_Based_on_Goals.png" width="668" height="333">

### Challenges and Difficulties Encountered
## Results
### Conclusions about Theatre Outcomes by Date
### Conclusions about Outcomes Based on Goals
### Limitations of Dataset
### Other possible information that could be included
