## Evaluating the State of California’s Higher Education

### Problem Statement
Given the current per-pupil spending in California, this analysis will look at whether:
1. Students are achieving satisfactory educational outcomes, and
2. The current budget is related to improvements in educational outcomes.

<br>Analysis will be conducted at the county level, and limited to the year 2018-19. ACT and SAT results will be used as proxies to understand educational outcomes. 

### Contents
- [Background](#Background)
- [Data Dictionary](#Data-Dictionary)
- [Conclusions and Next Steps](#Conclusions-and-Next-Steps)

### Background
Total state budget for public TK-12 education in 2018-19 in California was USD97.2 billion. The state spent USD55.4 billion on institutions supporting high-school education (taken as a sum of spending by Unified and High School Agencies). 

This analysis looks at whether the allocated budget is enough to achieve the desired educational outcomes.

**Approach** 
* Evaluate educational outcomes achieved in 2018-19: Compare county-level educational outcomes (SAT and ACT results) to assess:
    * County-level performance relative to national benchmarks
    * County performance ranking with respect to educational outcomes
* Review per-pupil expenditures: Determine per-pupil county-level spending allocated for high-school students, in order to determine:
    * Whether higher spending has any bearing on better educational outcomes
    
### Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|county|object|ACT/SAT/Spending|The political subdivision which oversees reporting for educational and expenditure outcomes.|
|agency_type_unified|object|Spending|Indicates whether a Local Educational Agency serves Higher Education students (unified school districs cater to K-12 students).|
|total_spending_unified_sum|float|Spending|Total expenditure per student, reported by Unified Education districts, aggregated by county.|
|total_spending_unified_mean|float|Spending|Average expenditure per student, reported by Unified Education districts, aggregated by county.|
|agency_type|object|Spending|Spending|Indicates whether a Local Educational Agency serves Higher Education students.|
|total_spending_high_sum|float|Spending|Total expenditure per student, reported by High School Education districts, aggregated by county.|
|total_spending_high_mean|float|Spending|Average expenditure per student, reported by High School Education districts, aggregated by county.|
|sat_enroll_sum19|float|SAT|Total number of students enrolled in grade 12.|
|sat_enroll_mean19|float|SAT|Average number of students enrolled in grade 12.|
|sat_test_taken_sum19|float|SAT|Total number of grade 12 students who took the SAT.|
|sat_test_taken_mean19|float|SAT|Average number of grade 12 students who took the SAT.|
|sat_participation_rate_mean19|float|SAT|Grade 12 students who took the SAT as a % of students enrolled in grade 12 (calculated as an average across districts).|
|sat_ERW_success_mean19|float|SAT|Average of grade 12 students who met or exceeded the benchmark (480/800) for Evidence-Based Reading & Writing (ERW) test for grade 12 (as % of students enrolled in grade 12).|
|sat_Math_success_mean19|float|SAT|Average of grade 12 students who met or exceeded the benchmark (530/800) for New SAT Math test for grade 12 (as % of students enrolled in grade 12).|
|sat_Both_success_mean19|float|SAT|Average of grade 12 students who met or exceeded the benchmark for both the ERW and Math tests for grade 12 (as % of students enrolled in grade 12).|
|enroll12_sum_act|float|ACT|Total number of students enrolled in grade 12.|
|enroll12_mean_act|float|ACT|Average number of students enrolled in grade 12.|
|numtsttakr_act|float|ACT|Total number of grade 12 students who took the ACT.|
|numtsttakr_mean|float|ACT|Average number of grade 12 students who took the ACT.|
|act_participation_rate|float|ACT|Grade 12 students who took the ACT as a % of students enrolled in grade 12 (calculated as an average across districts).|
|avgscrmath_mean_act|float|ACT|Average ACT Score for Math.|
|avgscrsci_mean_act|float|ACT|Average ACT Score for Science.|
|avgscreng_mean_act|float|ACT|Average ACT Score for English.|
|avgscrread_mean_act|float|ACT|Average ACT Score for Reading.|
|pctge21_act|float|ACT|Average percent of test takers whose ACT composite scores were greater or equal to 21.|
|high_spend|float|Spending|Current cost of education per student (calculated as total expenditure of education per average daily attendance), including expenditures for salaries, employee benefits, books, supplies, equipment, services and indirect costs. Costs are reported by Local Educational Agency, which controls and administers state funding to individual school districts.|

Note: All values denoted with a * reflect cases with insufficient number of students to create an anonymous aggregate for reporting.

<br>ACT Dataset: [ACT Test Results, California Department of Education]("../data/act_2019_ca.csv")
<br>SAT Dataset: [SAT Test Results, California Department of Education]("../data/sat_2019_ca.csv")
<br>Spending Dataset: [Per Pupil Spending, California Department of Education.]("../data/Education_spending_total_spending_by_LEA_by_county.csv")

### Conclusions and Next Steps
1. Just 43.4% of California students met or exceeded the SAT benchmark.
    - While 56% of students met or exceeded the ACT benchmark, fewer students take the ACT
2. California students fare worse in Mathematics than English, Reading, or Writing
    - SAT and ACT outcomes in mathematics were closely related, implying that interventions and variables impacting performance in mathematics, impacts test-takers for both tests 
3. Higher spending per pupil did not result in better educational outcomes

**Next Steps in the Analysis**
1. Confirm that SAT and ACT results:
    - How well they reflect educational outcomes
    - How they relate to acceptance and success criteria in post-secondary education
    - How they compare to other factors that evaluate educational outcomes, especially with respect to accounting for geographic and economic dispersion, English proficiency, and diversity and representation
2. Review spending per student calculations to finalize outcomes
3. Consider conducting a cohort-based analysis, to see whether a continuous 4-year investment results in improved educational outcomes
4. Define and evaluate factors that impact resource allocation in education
5. Conduct time-series analysis to test factors identified as having a significant impact on resource allocation effectiveness for education outcomes