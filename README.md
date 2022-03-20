# School_District_Analysis_2
## Overview:
Use Python and Pandas to efficiently examine a large amount of data obtained from an entire school district. With close to 40,000 students attending 15 schools normal analyses techniques prove to be ill suited for the job. The objective of this project is to use the power of Python and Panda programs to quickly examine this huge data set. It also uses Jupyter Notebooks to visualize the data in tabular format. A comprehensive analysis like this assists school boards and a variety of stakeholders to come to the right conclusions and make the right decisions.

## Overall Approach:
-	Import resources like the Panda library to assist in the analysis
-	Read the main data file
-	Examine the dataset for inconsistencies, e.g. spurious titles and/or suffixes, etc.
-	Merge datasets to create new data frames that provide more insight into the data
-	Perform key calculations on student performance data, e.g. reading and math scores
-	Try to gain additional insights by correlating student performance with school size, type and total spend per student 
-	Visualize the data to examine these trends and help tell the story

## Challenge
Challenge:
-	Evaluate math and reading scores for all grades and students in all the schools
-	Focus on one school in particular: Thomas High School, where the results appear suspicious for potential tampering
-	Identify whether replacing math and reading scores for Thomas High School ninth grade students with NaNs (‘not a number’) will affect the overall analysis.
## Resources Utilized to Complete Analysis
•	CSV Files: schools_complete.csv, students_complete.csv, clean_students_complete.csv
•	Jupyter Notebook Files:  PyCitySchools_Challenge_starter_code.ipynb

# Results
How was the overall district affected by the change in Thomas High School’s reading and math scores?
Impact at the District Level: 
Original data
	<img width="706" alt="Screen Shot 2022-03-20 at 10 02 11 AM" src="https://user-images.githubusercontent.com/99691015/159148299-9d76300c-fb27-47b0-9bed-596819244379.png">

With modified data:
	<img width="706" alt="Screen Shot 2022-03-20 at 10 02 11 AM" src="https://user-images.githubusercontent.com/99691015/159148375-ccd9a33a-e89f-448d-ada2-56d8f7a80da9.png">

This shows that the potential data inaccuracies with Thomas High School had little influence at the district level – in general <0.1% of a change. 

## Impact at the School Level
At the school level though there was a significant change. The average math and reading passing percentages, which were initially reported as 93.2% and 97.3% respectively, dropped down to 66.9% and 69.7% respectively. 
<img width="787" alt="Screen Shot 2022-03-20 at 10 09 25 AM" src="https://user-images.githubusercontent.com/99691015/159148498-2e674dc3-3ff5-4673-91db-7769614f8900.png">

### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
By replacing the ninth graders' math and reading scores, Thomas High School's performance ranking dropped from near the top of all schools (90.9% passing) to near the bottom (65.1% passing) in the district.

### How does replacing the ninth-grade scores affect the following:
o	Math and Reading Scores by Grade: Ninth grade math and reading scores dropped, when the scores were replaced to reflect NaN in the dataset.
o	Scores by School Spending: The spending range of $630 - $644 per student, at Thomas High School, remained the same. However, the percentage of overall students passing dropped from 79% to 63%, within that spending range

## Initial By Spend analysis:

<img width="787" alt="Screen Shot 2022-03-20 at 10 09 25 AM" src="https://user-images.githubusercontent.com/99691015/159148539-4e83d256-13fa-40e0-a786-bd16150d4e3f.png">

## Modified Spen d Analysis
<img width="787" alt="Screen Shot 2022-03-20 at 10 09 25 AM" src="https://user-images.githubusercontent.com/99691015/159151935-c599b1a8-ae76-491e-a710-cc07943f3b6c.png">

## Scores by School Size:
Thomas High School is a medium sized 1000 – 2000 student category of school size. Average math and reading scores within this bracket remained the same, however the percentage of students passing math and reading, both dropped by 6%. Schools in this medium school size bracket experienced a drop in percentage of overall students passing by 6%.

### Initial and Modified Size Analysis:
<img width="716" alt="Screen Shot 2022-03-20 at 12 33 20 PM" src="https://user-images.githubusercontent.com/99691015/159151969-68a43c52-c23c-47c6-8ea1-68e1e9d1f382.png">

## •	Scores by School Type: 
Charter schools demonstrated improved scores and overall passing % compared to district schools as shown below. E.g. Charter schools were consistently 36% points better than district schools in terms of overall passing percentage. Replacing the ninth-grade scores decreased passing math, reading and overall passing % scores by about 3%.

### Original Analysis by School Type:

<img width="733" alt="Screen Shot 2022-03-20 at 12 35 39 PM" src="https://user-images.githubusercontent.com/99691015/159152025-688d48d8-4b93-402b-b75d-73d1a33b7167.png">

### Modified Analysis by School Type:
<img width="708" alt="Screen Shot 2022-03-20 at 12 36 22 PM" src="https://user-images.githubusercontent.com/99691015/159152040-ca5f8455-bb36-4369-9901-45cab9bbf4d1.png">

## Summary
By conducting the comparative analysis, four major changes are evident in the updated school district analysis after reading and math scores for ninth grade Thomas High School students were replaced with NaNs.

### Results:
•	Scores at THS dropped significantly. As this was only one school and a medium sized one at that, the impact on overall district scores was quite muted.
•	Larger schools generally exhibited lower scores. One reason may be the presumed increased number of students per class and per teacher.
•	Per capita spend did not seem to have a noticeable impact on student academic performance.
•	Academic performance of students in charter schools was generally much better than that of district schools. 
### Approach:
•	Utilizing NaN provides an efficient way to capture discrepancies in the dataset. Replacing these with 0’s would have led to inaccurate data analyses. 
