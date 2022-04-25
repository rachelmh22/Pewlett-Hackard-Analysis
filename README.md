# Pewlett Hackard Analysis

## Overview of Project

The purpose of this project is use SQL to analyze the data and find answers to the questions regarding employees at Pewlett Harkard close to retirement. The data collected from this analysis will inform the company how many employees are retiring soon, and related information, such as their positions and which departments they work in. This will allow the company to make preparations for the turnover in employees so that the company is not left with empty positions when employees leave, as this could result in operational losses. 

## Results

- Based on the retiring_titles.csv file, we can see that a large majority of employees close to retirement hold senior positions in the company. It will be important for the company to ensure these senior positions are filled. 

<img width="175" alt="Retiring Titles" src="https://user-images.githubusercontent.com/100614930/165017900-6576ad54-dfa6-4652-9bdc-c6acf8996fa0.png">

- In the retirement_titles.csv file, many employees held multiple titles at their time at Pewlett Harkard. If we look at each title a single employee holds, it can be concluded that the company promotes their employees every few years. For example, Kwee Schusler (employee no. 10066) started at the company in 1986  and is promoted from assistant engineer to engineer in 1992 and then another promotion in 6 years in 1998 to senior engineer. Therefore, many of those retiring can have their positions replaced internally and promotions will be available to existing employees that will not be retiring as an incentive. 

<img width="429" alt="Kwee" src="https://user-images.githubusercontent.com/100614930/165017958-dd5d8f83-ffc0-404c-9abb-ce56399c74d5.png">

- The retirement_titles.csv file also informs the company when employees joined the company. This will tell us how long an employee has worked for the company.

- The mentorship eligibility.csv file gives a list of employees that are eligible to participate in a mentorship program. This list has when existing employees began to work at the company and their titles. The mentorship program can then be organized and prioritized based on experience and seniority at the company and the positions of those in the program.

## Summary

### How many roles will need to be filled as the "silver tsunami" begins to make an impact?

Counting all the employees in the unique_titles.csv file, 72,458 employees are in their retirement period and based on the retiring_titiles.csv file, 25,916 are senior engineer positions. It will be crucial for the company to begin preparing to find replacements for these positions or promote current engineers in the company to ensure these positions are not empty as this can impact company operations. 

#### Query
SELECT COUNT (emp_no)
FROM unique_titles;

### Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?

Counting the number of employees eligible for the mentorship program from the mentorship_eligibilty.csv file, only 1,549 employees will be able to participate. Depending on the mentorship program is set up, each eligible employee will need to mentor 40-50 employees if all positions are filled. However, some positions can be replaced through promotions and those eligible can create teams to assist them in the mentorship programs. Therefore, if organized well, the mentorship program can be successful. 

#### Query
SELECT COUNT (emp_no)
FROM mentorship_eligibilty;
