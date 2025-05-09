<img width="377" alt="Tech-Moms Logo Vertical" src="https://github.com/user-attachments/assets/b98d7ed8-150c-4a2a-9102-c4cfa4e91d01">

# Tech-Moms Annual Alumni Survey Analysis 

In this hands-on project, you will help Tech-Moms analyze their annual survey data in order to complete their annual non-profit report.

## Project Overview

Tech-Moms Leadership team is preparing to release their Annual Report. Annual reports are typically data-driven. They are important for non-profits because they provide transparency and demonstrate impact, which are crucial for sustaining donor support. The team needs to know the updated statistics and insights from their annual survey to effectively showcase their progress and outcomes. This includes key metrics such as the percentage of graduates who found jobs, transitioned into technical roles, received promotions, or continued their education. Additionally, the leadership team seeks to highlight testimonials that illustrate the program’s value. 

Your deliverable will be a “Tech-Moms Annual Survey 2024” Dashboard built in the spreadsheet software of your choice - Excel or Google Sheets. 

## Complete the Following Steps: 

### Step One: Get to Know Your Data 

- [x] Review the [Tech-Moms 2023 Annual Report](https://www.tech-moms.org/_files/ugd/0e6ea4_4aa4f371aaaf4b2c81a1e384dfdfec02.pdf?index=true) - payment special attention to the survey results section
- [x] Open the [Tech-Moms Survey Data 2024](https://docs.google.com/spreadsheets/d/1Rf9-nhBHtUWr0t4c0paNZaaJhFpDMU8lAIbeBR_uk0Q/edit?gid=0#gid=0) spreadsheet in Google Sheets
- [x] If working in Google Sheet, make a copy & add your name at the end - i.e. "Tech-Moms Survey Data 2024 - Alyson La" 
- [x] If working in Excel, download to Excel
- [x] Start by evaluating the columns to understand what data you're working with.
- [x] Create a new tab,  “Data Dictionary” and copy the columns -> go to new tab -> paste “transposed”. This will paste the columns vertically.
- [x] Add a row at the top of the Data Dictionary tab. In A1, type “Column Column Name” & in B1, type “Column Description”. Write a short description of each column based on your best-educated guess (you can also use ChatGPT to help with this).
- [x] Add a tab “Questions” as you come across questions about the data. You can add them here. These are questions you can ask the data owners (aka leadership team) to help clarify any questions you may have about the data set.

### Step Two: Clean the Data 

- [x] Make a copy of the “raw” data by duplicating the tab & rename it to “analysis”. Rename the original tab to “raw”.
- [x] Format the analysis table as follows: 
  *  Highlight column names and fill background color with the color of your choice
  * Add a filter
  * Freeze top row      
- [x] Review each column to understand the available options in each
- [x] Reformat the "Registered" Column to be formatted as a date without a timestamp - example: 8/13/2024
- [x] Preform any additional data cleaning tasks as needed
- [x] Do you notice any data quality issues to make a note of? 

### Step Three: Start Analyzing (aka Asking Questions of the Data)

In a survey like this, it is often best to systematically analyze each question starting from the first column & working all the way to the last column. You can either do this using function or pivot tables, it is up to you to decide what is best for each column depending on the data type. 

For example: 

- [x] What month did the most surveys get filled out? (create a pivot table using 'Registered' & counting the Contact ID values, grouped by month) 
- [x] What is the count and ratio of survey respondants that answered via computer vs phone?
- [x] What is the % of Alumni that were working vs not working at the time they started Tech-Moms
- [x] What is the average number of years respondants had been out of the workforce?
- [x] What was the average starting pay at the time of starting Tech-Moms?
- [x] What percentage of respondants are currently employed?
- [x] Among those that received a raise, what is the average % increase?
- [x] What percentage of respondant's received a promotion since starting Tech-Moms? 
- [x] What percentage of respondant's have taken a new position since starting Tech-Moms?
- [x] What is the ratio of respondant's that are working Full-Time vs Part-Time vs Not Currently Employed
- [x] How many hours are respondant's working each week? (binned by hours)
- [x] What percentage are currently seeking employment?
- [x] etc 

The last 4 questions are self-evaluation of alumni's growth since participing in the Tech-Moms program. Find the average of each coulumn to know it's rating out of 5 stars. 

Evaluate the open ended replies for themes that stand out. You could do a key word search for "community" and pull out quotes that highlight the positive replies. Also see if you can find replies that include negative sentiments or constructive critizim. You will want to highlight both the positive and negative feedback to leadership. 

#### Advanced Excel Skill: XLOOKUP

We also want to know what % of applicants that were "Assigned Cohort" in the [Tech-Moms Application Data](https://docs.google.com/spreadsheets/d/1BhskpHGoHSl2fuXY3qjnqSpgI2imWB2Ng7OYP-pWslI/edit?usp=sharing) filled out a survey. Use the Contact ID column in each table to "join" the tables together and find out if the student completed the survey or not. Write down the tasks below you would need to do to find this out. 

> 1 - make sure I have both sheets. 
Application data: Contact ID, Applicant Status: Assigned Cohort
Survey Data: Contact ID (yes or no?)
→ Make sure the data is clean in applicable columns

> 2 – Combine both sheets into one workbook. 
(I made a new copy of my survey data specifically for this so I don’t “break” something from my prior copy. I used Chat GPT to refine my approach with some questions I had, and I learned that in excel you can use xlookup in sheets in different workbooks, but it might not work if the sheets/workbooks aren’t all open. In GoogleSheets, there is an alternate method to Xlookup that allows multiple workbook lookup called “importrange,” but given the assignment I’m merging the files into one workbook. I chose to filter for “assigned cohort” first and only copy those into the merged file. 

> 3 - Identify the contactID column in both sheets. 

> 4 - in the Application data sheet, add a new column that answers the assigned question. Survey Completed? 

> 5 - use xlookup to match the contact IDs between the sheets and answer the question in the newly created column
=IF(XLOOKUP(TRIM(CLEAN(A2)), ARRAYFORMULA(TRIM(CLEAN('Survey Data for Analysis'!A:A))), 'Survey Data for Analysis'!B:B, "") = "", "No", "Yes")
Note: I cleaned the data here (thanks for the troubleshooting ChatGPT) because I didn’t have it clean initially, but then went back and cleaned it initially. 

> 6 - copy and paste the column as values so you can calculate a percentage 

> 7 - write a formula to figure out the percentage OR do a pivot table. I’m going to do a pivot table so I can practice that skill more (and the idea that it would update with changing data)


### Step Four: Validate Your Data 

Before polishing and presenting your data, you will want to validate that the results are correct so your stakeholders can trust it.
- [x] Compare your results against the [survey kiwi](https://github.com/Tech-Moms/data-analytics-winter-2025/blob/main/module_2/assignments/survey_kiwi.md) output. 

### Step Five: Create Charts & Build a Dashboard 

- [x] For each question answer, create a visualization that best conveys the data. As much of the responses are shown in % of total form, try out different types of charts - pie chart, vertical bar chart, and horizontal bar chart. Is there a certain visualization you like best?

### Step Six: Make it Aesthetic 

- [x] Evaluate the current dashboard and make some decisions on what would make the dashboard more aesthetically pleasing.
- [x] Create some new columns either in the “analysis” tab or in the “pivot tables” tab to consolidate data into the minimal number of categories in order to best visually represent it in the dashboard.
- [x] Upload the Tech-Moms logo to the dashboard.
- [x] Update the Dashboard theme to use Tech-Moms’ brand colors.

### Step Seven: Ask for Feedback 

- [x] Ask a study buddy or data mentor for feedback on your dashboard / visualizations 
- [x] Incorporate the feedback
- [x] Do a little happy dance - you're crushing it! 💃

**Note:** In a future assignment we will practice our data storytelling skills by putting our visualizations and insights into a slide presentation for Share & Tell + Tech-Moms leadership. ✨ 


![Dashboard Screenshot Excel Sheets Survey Data Module 2](https://github.com/user-attachments/assets/75df31ee-34ce-474f-bd87-d4d417972f6b)
