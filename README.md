# Using PostgreSQL To Filter and Manage Employee Information
## Overview
The goal of this analysis is to use our datasets to filter out the employees of a company that are due to retire, as well as newer/younger employees and their eligibility for mentorship. Because we’re dealing with multiple, large datasets that all share information in one way or another, PostreSQL is an effective tool to route the information efficiently so we can extract the data we need to execute our analysis.
## Results
### The following information was found from our datasets once filtered through PostgreSQL:
-	Numerous employees (due to retire) held multiple titles throughout their employment
-	We could filter through our datasets to display just those individual employees
-	From there we can find the number of employees due to retire from each department
-	And lastly display which of said employees are eligible for the company’s mentorship program (born in the year 1965)
## Summary
### Numbers of Employees Due for Retirement
Displayed below, we can see the number of employees per department that are due to retire, which is important going forward to determine what course of action the company must take in terms of pensions, hiring, etc. We can see a noticeable skew in how few mangers are due to retire compared to the rest of the fields. This may warrant further investigation into the validity of our Data, however this may in fact be truthful. Perhaps the title of “Manager” does in fact exist sparsely in the company, and can just be viewed as an outlier in further analysis.

![image](https://user-images.githubusercontent.com/79726572/114057411-89233380-9860-11eb-9a06-f60314dc0f10.png)

### Employees Eligible for Mentorship Program
Below is the above information filtered by employees born specifically in 1965 done so by:
```
WHERE (e.birth_date BETWEEN '1965-01-01' AND '1965-12-31')
```
![image](https://user-images.githubusercontent.com/79726572/114057489-993b1300-9860-11eb-9669-2827950ccdcc.png)

We can see the size of this dataset just by scrolling, so just solely from the year of 1965 we can determine there’s an ample number of employees due for retirement that would qualify. Now it’s a question of who to select and why, which can be done in a further analysis. As the company must determine how many new hires will be required, the numbers of mentors is dependant on this.


