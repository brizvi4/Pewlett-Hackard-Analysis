# Pewlett Hackard Analysis

## Overview

For this analysis, I was assigned to help Bobby in providing a list of employees who are retiring from Pewlett Hackard (PH). Bobby's manager needs this information since he needs to see how many and exactly which employees will be retiring. The manager also wants to figure out which of those employees will be eligible for a retirement package. After providing this information using PostreSQL, Bobby's manager assigned us with another task. He asked us to identify employees who are eligible to participate in a mentorship program. Again, Bobby and I used pgAdmin and PostreSQL to illustrate our findings. 

## Results

- From the unique_titles csv file, we can see that most people who are retiring have the titles of "Senior Engineer" and "Senior Staff". 
- There are around 1550 employees eligible for mentorship_eligibility which is a good thing for the company since these employees can train the new employees. 
- From the retirement_titles csv file, it can be seen that many employees had more than one title since they got promoted. 
- From the retring_titles csv file, we can see that there are a total of 7 types of positions which will need to be filled.

## Summary

PH will need to fill 25916 roles for the position of "Senior Engineer", 24926 roles for the position of "Senior Staff", 9285 roles for the position of "Engineer", 7636 roles for the position of "Staff, 3603 roles for the position of "Technique Leader", 1090 roles for the posotion of "Assistant Engineer" and 2 manager positions. 

![image](https://user-images.githubusercontent.com/95254809/155265354-b58a9e10-265b-4da6-b321-4d290b5db6b4.png)

The good thing is that PH has around 1550 employees available for the mentorship eligibility program. And the good thing is that many of them hold the positions of "Senior Engineer" and "Senior Staff" which is a good thing since these positions will have the most number of vacancies in the future. 

One more thing which we could have done was to group the titles and count them in the mentorship_eligibility table. This way, we would know the number of employess eigible for the mentorship program according to their titles. This could have been done by using the following query:

SELECT  COUNT(title), title
INTO unique_mentorship_eligibility
FROM mentorship_eligibility
GROUP BY title
ORDER BY COUNT(title) DESC
;

