# ![] Project 1: Standardized Test Analysis

### Overview

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.

### Problem Statement

This project aims to identify trends indicating a performance advantage on the SATs & ACTs related to the so-called “equitable ranking” of public school districts throughout the state of California, primarily for the consideration of resource allocation by state legislation.

---

### Datasets

#### Provided Data

* [`act_2019_ca.csv`](../data/act_2019_ca.csv): 2019 ACT Scores in California by School ([source](https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary](https://www.cde.ca.gov/ds/sp/ai/reclayoutact19.asp))
* [`sat_2019_ca.csv`](../data/sat_2019_ca.csv): 2019 SAT Scores in California by School ([source](https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary](https://www.cde.ca.gov/ds/sp/ai/reclayoutsat19.asp))

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**district_name**|*object*|2018-19 CA Dept. of Edu.|The name of the California Public School District.| 
|**enrolled_seniors_x**|*integer*|2018-19 CA Dept. of Edu.|The number of 12th grade students enrolled in the School District in the 2018-19 School Year from SAT records.|
|**tested_seniors_x**|*integer*|2018-19 CA Dept. of Edu.|The number of 12th grade students that took the SAT in the 2018-2019 school year.| 
|**num_over_benchmark_sat**|*integer*|2018-19 CA Dept. of Edu.|The number of 12th grade students, per School District, that took the SAT and scored above the mean combined score threshold set by the College Board.|
|**pct_over_benchmark_sat**|*float*|2018-19 CA Dept. of Edu.|The percent of 12th grade students, per School District, that took the SAT and scored above the mean combined score threshold set by the College Board.| 
|**enrolled_seniors_y**|*integer*|2018-19 CA Dept. of Edu.|The number of 12th grade students enrolled in the School District in 2018-19 from ACT records.|
|**tested_seniors_y**|*integer*|2018-19 CA Dept. of Edu.|The number of 12th grade students, in each School District, that took the ACT in the 2018-19 school year.| 
|**num_over_benchmark_act**|*integer*|2018-19 CA Dept. of Edu.|The number of 12th grade students, per School District, that took the ACT in 2018-19 AND scored a composite score greater than or equal to 21.|
|**pct_over_benchmark_act**|*float*|2018-19 CA Dept. of Edu.|The percent of 12th grade students, per School District, that took the ACT and scored a composite score of at least 21.| 
|**rank**|*integer*|2018 census|The order of CA Public School District's "equity", where rank-1 indicates the so-called "most equitable school district".|
|**score**|*float*|2018 census|The equity grade of each School District as determined by an absolute difference in School District Expenditures per Pupil and Mean Household Income in each School District (i.e. the highest "score" corresponds to the so-called least equitable district).| 
|**expenditures_per_pupil**|*integer*|2018 Census|The amount a school district spends per pupil based on data from the U.S. Census: Annual Survey of School System Finances.This is used to score public school districts by comparison to the CA State average. A given score is based on 50 and, for each % above(below) the average expenditure per pupil across the sate, one point is subtracted(added).|
|**income**|*integer*|2018 census|The average household income by school district. This is used to score public school districts by comparison to the CA State average. A given score is based on 50 and, for each % above(below) the state average income, one point is added(subtracted). | 

#### Additional Data

* [`equitable_county_rank.csv`](../data/equitable_county_rank.csv): 2019 California School District Equitablility Ranking ([source](https://wallethub.com/edu/e/most-least-equitable-school-districts-in-california/77056/))

---

### Deliverables
- A Jupyter notebook that describes your data with visualizations & statistical analysis.
- A README markdown file the provides an introduction to and overview of your project.
- Your presentation slideshow rendered as a .pdf file.
**NOTE**: Your entire Github repository will be evaluated as your technical report.
---

### Submission

Your technical report will be hosted on Github Enterprise. Make sure it includes:

- A README.md (that isn't this file)
- Jupyter notebook(s) with your analysis (renamed to describe your project)
- Data files
- Presentation slides
- Any other necessary files (images, etc.)

---

### Rubric

**Clarity of Message**
- Is the problem statement clearly presented?
- Does a strong narrative run through the project?
- Does the student provide appropriate context to connect individual steps back to the overall project?
- Is it clear how the final recommendations were reached?
- Are the conclusions/recommendations clearly stated?

**Data Cleaning and EDA**
- Does the student fix data entry issues?
- Are data appropriately labeled?
- Are data appropriately typed?
- Are datasets combined correctly?
- Are appropriate summary statistics provided?
- Are steps taken during data cleaning and EDA framed appropriately?

**Visualizations**
- Are the requested visualizations provided?
- Do plots accurately demonstrate valid relationships?
- Are plots labeled properly?
- Plots interpreted appropriately?
- Are plots formatted and scaled appropriately for inclusion in a notebook-based technical report?

**Research and Conceptual Understanding**
- Were useful insights gathered from outside sources?
- Are sources clearly identified?
- Does the student provide appropriate interpretation with regards to descriptive and inferential statistics?

###