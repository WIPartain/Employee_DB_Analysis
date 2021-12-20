# Employee_DB_Analysis
## Overview
Pewlett Hackard has hired us to do an analysis on the company's employee database.  They are using our skillset to help them prepare for a potential upcoming staffing issue.  Many of the company's staff are approaching retirement age, and we need to determine how many employees fit in that category.  We also need to determine how many of PH's employees qualify for a mentorship program to prepare less tenured staff to assume roles vacated by future retirees.  We utilized PostgreSQL to group various csv's of employee data to determine the answers to challenges presented by Pewlett Hackard.

## Results
### Number of Employees Retiring by Titles
* Retirement Titles
![](https://github.com/WIPartain/Employee_DB_Analysis/blob/main/Images/retirement_titles.png)
In this first table, we collected a list of all employees and their titles if they were qualified to retire in the next few years.  However , it is unrefined as it contains all titles each employee collected during their time with Pewlett Hackard.  It retrieved over 133,000 rows, and it is not a consice view of the upcoming surge of potential employee retirements.
* Unique Titles
![](https://github.com/WIPartain/Employee_DB_Analysis/blob/main/Images/unique_titles.png)
This is the same table as before, however it only contains the most recent title for all employees. By omitting the extra titles, we are able to narrow the field to 90,398 rows of employees up for retirement in the coming years.
* Retiring Titles
![](https://github.com/WIPartain/Employee_DB_Analysis/blob/main/Images/retiring_titles.png)
This is the most concise table based on the results of our analysis of employees eligible for retirement in the coming years. By grouping by titles, we were able to narrow the results down to 7 rows with the above data representing the potential retirements by titles. 
### Mentorship Program
* Mentorship Eligibility
![](https://github.com/WIPartain/Employee_DB_Analysis/blob/main/Images/mentorship_eligibility.png)
We created a seperate table in order to determine which employees would qualify for a mentorship program in order to help prepare the next generation for the positions vacated by the silver tsunami. To retrieve this data, we merged the employees, titles and dep_emp with the inner join. Similar to the previous tables, we filtered by birth date over a certain range, but we made sure to only include current employees. This turned in 1,549 results, meaning only a very small percentage of retired or retiring employees would qualify for this mentorship program.
## Summary
It is important for Pewlett Hackard to get ahead of the upcoming "silver tsunami."  We need to determine how many vacancies will be created by this event, and how many positions they should fill internally or externally.  Based on the results of our table, we determined there are over 90,000 potential vacancies resulting from the silver tsunami. The table retirement titles csv contains all of this information, and it just needed to be grouped by department. To get the number of positions that will be open in next four years I ran an additional query that breaks down how many staff will retire per department. 
![](https://github.com/WIPartain/Employee_DB_Analysis/blob/main/Images/Vacancies.png)

We were also able to narrow down the amount of staff qualified to fill these positions by sorting mentors by position, and keeping the seniorn leader, and manager positions.
![](https://github.com/WIPartain/Employee_DB_Analysis/blob/main/Images/Qualified.png)
