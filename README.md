# Pewlett_Hackard_Analysis

## Overview
We were asked by our client at Pewlett-Hackard to help them prepare for their upcoming "silver tsunami," which is what they've dubbed the massive amount of employees who will likely be retiring in the next few years. We were given two objectives: 
  * To provide the number of retiring employees based on title the currently hold, and 
  * To identify employees who are eligible to participate in a mentorship program that Pewlett-Hackard is going to pilot, where near-retirees will be able to move into part-time positions and help train employees for their roles after they retire.

## Analysis
Utilizing data they had already provided, and queries we'd already created, we created:

* A "Retirement Titles" table that holds all the current employees who were born between January 1, 1952 and December 31, 1955 and their corresponding titles. Then, we counted how many were near retirement by title.
* An "Employees Eligible for the Mentorship Program" table that holds the current employees who were born between January 1, 1965 and December 31, 1965. 

## Results
<Provide a bulleted list with four major points from the two analysis deliverables.> 
<Use images as support where needed.>

### Employees Near Retirement
#### Titles Included
 * Using the data provided, we found that the list of employees who were born between 1952 and 1955 was nearly 134,000 rows long. Upon short review, however, we recognized that some of the employees on the list were on multiple times. Further review showed that employees received new titles throughout their tenure at Pewlett-Hackard (promotions, etc.). So, we sought to further refine this list to make it more valuable.
 
 ![Employees Near Retirement, Titles Included](https://github.com/andeevosters/Pewlett_Hackard_Analysis/blob/main/Visuals/retirement_titles_133776.png) 
 
#### Only Most Recent Title Included
 * We queried only the most recent job title for each employee, and the result decreased the list by 1/3, down to approximately 90,000.
 
 ![Employees Near Retirement, Only Most Recent Title Included](https://github.com/andeevosters/Pewlett_Hackard_Analysis/blob/main/Visuals/unique_titles_90398.png)
 
### Employees Eligible for the Mentorship Progam
 * We took a simliar two-step approach to determine which employees would be eligible for the mentorship program. We first filtered the employee information to determine which current employees were born in 1965 (ten years from retirement), of which any title that employee held was tabulated. We then filtered the list to only include each employee's most recent job title. In the end, 1,549 employees are roughly 10 years from retirement.
 
 ![Employees Eligible for the Mentorship Progam](https://github.com/andeevosters/Pewlett_Hackard_Analysis/blob/main/Visuals/mentorship_eligibility_1549.png) 

 * It's worth noting that the silver tsunami, those within a few years of retirement, account for 30% of the 300,000-employee workforce. That's roughly 30,000 born each year between 1952 and 1955, compared to only 1,549 born in 1965, just ten years later. That's a 2,000% difference in "graduating class" size.
  
## Summary
 * Of Pewlett-Hackard's 300,000-person workforce, roughly 90,000 are or will be at retirement age in the next few years. Nearly 2/3 of them (57,668) hold senior positions. That's a lot of employees to be potential mentors. But is it enough? We looked at employees born in 1965 (ten years from retirement, so still growth potential) as those eligible to be mentees. There are just over 1,500 employees born in 1965, so at that rate, each mentee could have 30-60 mentors!
 
![Number of Retirees By Title](https://github.com/andeevosters/Pewlett_Hackard_Analysis/blob/main/Visuals/retiring_titles_7.png)
  
 * The Development department will be the most significantly impacted by the "silver tsunami" (9,281), followed by Production (8,174).
 
![Number of Retirees by Department](https://github.com/andeevosters/Pewlett_Hackard_Analysis/blob/main/Visuals/dept_totals.png)

 * For the sake of comparison, we compared the "retiring class" to the "new class" by counting the number of people PH will lose to retirement in the next 4 years (90,000) to the number of employees they hired in their most recent four years (21,000) with the query below. So, even with a mentorship program, Pewlett-Hackard needs to put some heavy recruitment practices in place if they plan to recover the amount of positions they are going to lose. 
 
![New Hire Query (1996-1999)](https://github.com/andeevosters/Pewlett_Hackard_Analysis/blob/main/Visuals/new_hire_query.png)
