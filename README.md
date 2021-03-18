# Kickstarter Analysis of Outcomes Based on Goals and Launch Date
### This project determines how well Kickstarter Campaigns for theatre projects did based on their launch date.  It also includes outcomes based on funding goals for play productions within the theatre category.
## Analysis and Challenges
The <a href="Kickstarter_Challenge.xlsx">dataset</a> that was analyzed for this project is a subset of Kickstarter challenge data dated from 2009 to 2017.  Although this data contains many different categories the analysis is based spefically on the "theatre" category and the "plays" subcategory.  The initial set of data contained information for each campaign about the following:
**Name**, **Blurb**, **Goal**, **Pledged**, **Outcomes**, **Country**, **Currency**, **Deadline**, **Launched At**, **Staff Pick**, **Backers**, **Spotlight**, 
**Category/Subcategory**, **Percentage Funded** and **Average Donation**. <br><br>
The **Deadline** and **Launched At** dates were provided as Unix timestamps.  Two new columns were created **Date ended conversion** and **Date created conversion** and the Unix times were converted and added to the two new columns respectively. A **Year** column was also added which pulled out the year of the Launch date. <br><br>
It was also necessary to split **Category/Subcategory** into two new columns one for **Category** and one for **Subcategory** in order to be able to look at the Theatre category for one analysis and the Play subcategory for the other.<br>

### Analysis of Outcomes Based on Launch Date
<p align="center">
  <img src="Resources/Theater_Outcomes_vs_Launch.png" width="620" height="333">
  
### Analysis of Outcomes Based on Goals
<p align="center">
  <img src="Resources/Outcomes_Based_on_Goals.png" width="668" height="333">

### Challenges and Difficulties Encountered
## Results
### Conclusions about Theatre Outcomes by Date
### Conclusions about Outcomes Based on Goals
### Limitations of Dataset
### Other possible information that could be included
