# Students-analysis-performance-analysis
Cleaning,Analysis and Visualization of a students data using Excel and Power query.
##  Project Overview
Analyzed, Cleaned and Visualized a student enrollment data to identify which courses drive the highest revenue, admission trends by year, and student demographics. Project demonstrates end-to-end data cleaning in Excel, Power Query and visualization using Pivotcharts.
### Business issues
The institution needed to answer;
courses that generates the most revenue
yearly revenue of course enrollment
What is the gender and age distribution of students?
#### Dataset
- **Source:** Delmich dataset (Uncleaned_students_data)
- **Original Rows:** 130 records
- **Key Columns:** Student_ID, First_Name, Last_Name, Age, Gender, Course, Enrollment_Date, Total_Payments
- **Files in this repo:**
    - data/raw/ - Original dirty file (pipe-delimited, mixed currencies $, ₦,irrelevant spaces)
    -data/cleaned/ - Final cleaned file after Power Query
##### Tools Used
- **Excel** Text to columns, Data cleaning, pivot table, pivotcharts
- **Power Query:** Data cleaning, splitting, type transformation,
######  Data Cleaning Process
This was the main work. The raw file had:
- All data stuck in one column with `|` delimiter - **Fixed by:** Split Column > By Delimiter `|`
- Duplicate header row inside data (Row 12) - **Fixed by:** Filtered out Student_ID = "Student_ID"
- Total_Payments` had mixed symbols: `$1200`, `?20,000.00` (? is corrupted ₦),
- **Fixed by:** Trim > Clean > Replace Values ($, ?, ₦, ,) > Changed to Currency Type
- Duplicate column `Gender` and `Gender2` - **Fixed by:** Removed Gender2
- Typo in Course: `Web Developmet` -> `Web Development` - **Fixed by:** Replace Values
- `Enrollment_Date` had `NA` and mixed formats - **Fixed by:** Replace NA with null, changed to Date type
- Removed duplicates
###### Key Insights
 **Revenue Driver:** Web devops, Data analysis and Cybersecurity contributed about 90% of total revenue with cybersecurity generating the highest.
- **Payment range by gender:** Data shows that there were more payments from the male than the female
- **Enrollment Trend:** 2022 had the highest enrollment count
- **Demographics:** Age group 20-25 dominates admissions

