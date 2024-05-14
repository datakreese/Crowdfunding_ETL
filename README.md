# Crowdfunding_ETL

# Context & Analysis
In this project we analyzed crowdfunding campaigns. The goal was to clean and consolidate information from multiple sources for efficient future queries.
We used pandas, numpy, and json to clean the data and that resulted in four updated csv files. Those files are called contacts, campaign, category, and subcategory. Normalizing the data included creating id's for each category and subcategory. We also dropped staff pick and spotlight columns because we did not have data identifying how those were selected. From there we created a ERD which can be viewed through the crowdfunding_db_schemas file. 

We used the ERD file to create a crowdfunding database with a table for each of our csv files. You'll notice there are different data types for the columns in the ERD vs database. Through trial and error we realized the strings needed to be replaced with varchar and text, while a couple integers needed to be changed to float8. 

# Further Analysis Potential
Now that the information is in a database custom SQL queries could be written to analyze the data as well as identify outliers. 
- Find someone to inteview about a recent success story
- If campaigns being funded by different currency types had a higher success rate
- Analyze which category/subcategory has a high failure rate
- Average number of backers to reveal the scaling potential for this form of funding
- Average pledge by each backer to create incentives/reward tiers that are realistic 

Information that wasn't included that could provide additional insight would be:
- The date the goal was reached (along with the start and end date of the campaign)
- How many campaigns each contact/company has launched previously (outside of the dataset)
- Budget spent on marketing across platforms
- Long term data for the success of an endeavor after it was initally funded
- A larger sample size would help us avoid skewing results of categories, subcategories with fewer campaigns
