## Healthcare Financial & Operational Performance Dashboard
__________________________________________________________________________________________________________________________________________________________________________________________
## Intro page
<img width="901" height="502" alt="navigate" src="https://github.com/user-attachments/assets/22050f98-4174-43fe-a56a-11eef451318c" />
__________________________________________________________________________________________________________________________________________________________

## DATA MODEL

**1. Data Model / Schema Diagram**

<img width="1120" height="497" alt="d0 data modelling" src="https://github.com/user-attachments/assets/150ee11a-09b8-4ad8-b454-c8f2147a48e9" />

This visual represents the logical data architecture of the healthcare analytics solution. It follows a classic star-schema style design, optimized for reporting and BI workloads.

**Key Observations:**

•	Central Fact Table – visits

o	Acts as the transactional core.

o	Contains measurable events such as Admitted Date, Discharge Date, Emergency Visit, Follow-Up Visit, and financial metrics like Insurance Coverage.

o	Each record represents a patient encounter.

•	Dimension Tables

These provide descriptive context for slicing and filtering:

o	Date Table → Time intelligence (Month, Weekday, etc.)

o	Patients → Demographics (Age, Gender, City)

o	Providers → Doctor / provider attributes

o	Departments → Organizational grouping (Cardiology, Neurology, etc.)

o	Procedures → Clinical activities (X-Ray, MRI, etc.)

o	Diagnoses → Medical classification

o	Insurance → Payer information

o	Cities → Geographic hierarchy (City, State)

**•	Relationship Structure**

o	One-to-many relationships from dimensions into visits.

o	Ensures filtering propagates correctly for analytics.

o	Supports multidimensional analysis (time, geography, clinical, financial).

Why This Matters:

•	Clean separation of facts vs attributes improves performance.

•	Enables flexible reporting without redundancy.

•	Ideal for Power BI / OLAP-style querying.
_____________________________________________________________________________________________________________________________________________________________________________________________________________

## DASHBOARD 1
## 2. Healthcare Provider Dashboard (Summary & Distribution View)

<img width="900" height="500" alt="d1" src="https://github.com/user-attachments/assets/941d0e03-0200-45ad-bfb4-114527782f93" />

This is the executive KPI overview dashboard, focusing on financial performance and categorical distribution.

**Top KPI Band:**

The header metrics provide an immediate snapshot of operational health:

•	Total Billing Amount

•	Total Medication Cost

•	Total Treatment Cost

•	Total Insurance Cost

•	Total Room Charges

•	Out-of-Pocket Cost

These represent the core revenue and cost drivers of the healthcare provider.

**Secondary KPI Layer (Averages):**

•	Average Billing Amount

•	Average Medication Cost

•	Average Treatment Cost

•	Average Insurance Cost

•	Average Room Charges

•	Average Out-of-Pocket Cost

These normalize performance and help identify pricing or cost anomalies.

**Visual Breakdowns**

A. Billing by City (Map Visual)

•	Geographic distribution of revenue.

•	Identifies high-value regions or patient concentration.

•	Useful for expansion, marketing, or resource allocation decisions.

B. Billing by Procedure (Bar Chart)

•	Compares contribution of services (X-Ray, CT Scan, MRI, etc.).

•	Highlights revenue-generating procedures.

•	Helps assess service demand and equipment utilization.

C. Billing by Diagnosis (Stacked Bars)

•	Connects financial data with clinical patterns.

•	Shows which conditions drive costs/revenue.

•	Segmented by visit type (Emergency / Inpatient / Outpatient).

D. Billing by Department

•	Evaluates departmental financial impact.

•	Assists in budgeting, staffing, and performance tracking.

**Analytical Value**

This dashboard primarily answers:

•	Where is revenue coming from?

•	Which services generate the most value?

•	Which medical conditions drive billing patterns?

•	How do departments compare financially?

It is designed for high-level decision-makers.
____________________________________________________________________________________________________________________________________________________________________________________________________________________

## DASHBOARD 2
## 3. Financial & Trend Analysis Dashboard (Comparative View)

<img width="888" height="506" alt="d2" src="https://github.com/user-attachments/assets/0c2b9558-2e02-4249-82c9-88b8464feed5" />

This visual emphasizes time-based performance, variance analysis, and trend behavior.

**Top Section – Time Intelligence & Comparisons**

A. Total Billing Amount vs YTD Comparison

•	Compares yearly performance (e.g., 2024 vs 2025).

•	Indicates growth or contraction.

•	Supports strategic forecasting.

B. YTD Trend Indicator

•	Shows cumulative performance trajectory.

•	Helps detect seasonal patterns or slowdowns.

C. Weekly Billing Comparison

•	Highlights short-term fluctuations.

•	Useful for operational monitoring.

**Middle Section – Month-over-Month Analysis**

**Billing vs Previous Month**

•	Displays positive and negative variances.

•	Quickly surfaces months with abnormal changes.

•	Aids in root-cause analysis (policy changes, patient volume shifts, etc.).

**Bottom Section – Departmental Weekly Trends**

Line charts for departments such as:

•	Orthopedics

•	General Surgery

•	Pediatrics

•	Cardiology

•	Neurology

**Insights Provided:**

•	Departmental performance dynamics.

•	Day-level patterns (Sun → Sat).

•	Identifies peak demand days.

•	Useful for workforce planning and scheduling.
__________________________________________________________________________________________________________________________________________________________________________________
## DASHBOARD 3
## 3. Patient Volume, Visit Behavior & Department Utilization Analytics

<img width="899" height="505" alt="d3" src="https://github.com/user-attachments/assets/09869668-bcac-4298-bba5-79882d458d58" />

1. Overall Analytical Narrative

Your dashboard tells a healthcare operations story centered on:

Patient Flow → Visit Patterns → Department Load → Quality Signals

It allows stakeholders (hospital admin / operations / clinical management) to quickly understand:

•	How many patients are being handled

•	How they are distributed across admission vs outpatient

•	How visits split between emergency vs non-emergency

•	Which departments carry demand

•	Whether patient experience aligns with volume

2. Core KPI Layer (Top Summary Metrics)

These serve as executive snapshot indicators.

Total Admitted

Represents inpatient workload.

**Operational meaning:**

•	Bed utilization pressure

•	Admission trends

•	Resource & staffing implications

Total Outpatient

Reflects ambulatory care demand.

Operational meaning:

•	OPD efficiency

•	Doctor scheduling

•	Throughput capacity

Total Visit

Acts as the primary volume driver.

Conceptually:

```
Total Visit = Emergency Visits + Non-Emergency Visits
```
Business relevance:

•	Overall hospital traffic

•	Demand forecasting anchor

3. Visit Type Distribution

Emergency vs Non-Emergency %

This metric answers:

“What type of care demand dominates?”

Interpretation examples:

•	Higher Emergency %

o	Acute case pressure

o	Possible triage / ER bottlenecks

o	Unplanned utilization

•	Higher Non-Emergency %

o	Routine / scheduled care

o	Predictable operational flow

o	Preventive & elective services

This metric is strategically important because it influences:

•	Staffing models

•	Equipment readiness

•	Cost structures

4. Patient Length of Stay (LOS) & Admission

Patients by Length of Stay

This visual describes inpatient resource intensity.

Insights you can derive:

•	Short stays dominance

o	Efficient treatment cycles

o	High turnover

•	Long stays dominance

o	Complex cases

o	High bed blocking risk

o	Financial impact

Operational linkage:

•	Capacity management

•	Case severity mix

•	Discharge efficiency

5. Department-Level Utilization

Total Visit by Department & Visit Type

This answers:

“Where is demand concentrated and what type of cases drive it?”

Examples of insights:

•	High emergency load in a department

o	Critical care dependency

o	Urgent clinical readiness

•	High non-emergency load

o	Elective / routine specialization

o	Scheduling optimization opportunity

This metric supports:

•	Department staffing decisions

•	Equipment allocation

•	Budget planning

6. Temporal Pattern Analysis

Total Outpatient by Weekday

This visual uncovers cyclical behavior.

Typical interpretations:

•	Mid-week peaks

o	Standard appointment clustering

o	Doctor availability effects

•	Weekend dips / spikes

o	Reduced services vs emergency spillover

Operational impact:

•	Shift planning

•	Queue management

•	OPD slot balancing

7. Quality & Experience Signal

Patient Satisfaction Score

This is your performance quality indicator.

Key analytical value:

•	Compare volume vs satisfaction

•	Detect service stress effects

Example logic:

•	High visits + Low satisfaction → Service overload risk

•	Moderate visits + High satisfaction → Operational balance

This metric introduces a decision-making dimension, not just reporting.

8. Provider / Doctor Cards

These act as micro-performance units.

They allow evaluation of:

•	Individual provider ratings

•	Patient distribution per doctor

•	Potential workload imbalance

Strategic utility:

•	Performance benchmarking

•	Patient preference patterns

•	Workforce management

9. Implicit Business Story Your Dashboard Enables

Your dashboard supports questions like:

•	Is patient demand growing or shifting?

•	Are emergency cases driving hospital load?

•	Which departments need capacity reinforcement?

•	Are patient experience metrics aligned with workload?

•	Do visit patterns suggest scheduling inefficiencies?

10. Analytical Strength of Your Design

What works conceptually:

✔ Multi-layered analysis (Volume → Type → Department → Time → Quality)

✔ Good separation of operational vs quality metrics

✔ Supports both executive and operational decision contexts.
___________________________________________________________________________________________________________________________________________________________________________________________________________________
## TOOLTIP

<img width="201" height="448" alt="tooltip" src="https://github.com/user-attachments/assets/19db0459-4fd9-4ff0-8f15-24abeb517ad8" />

This tooltip functions as a provider-level performance snapshot, summarizing the operational and experience metrics associated with an individual doctor.

Interpretation of elements:

•	Provider Identification (Dr. Emma Jones)

Establishes the analytical context — all displayed metrics relate specifically to this physician’s patient interactions.

•	Age (34)

Demographic attribute. While not operationally decisive alone, it may support workforce profiling, segmentation, or HR analytics when compared across providers.

•	Nationality (European)

Informational descriptor. Typically relevant only in organizational diversity analysis or staffing composition studies, not performance evaluation.

•	Patients Attended (4,973)

Core workload / volume indicator.

Analytical significance:

o	Reflects clinical throughput

o	Indicates provider demand / utilization

o	Useful for capacity and workload balancing

o	Can be benchmarked against peers

•	Patient Satisfaction Score (4.21)

Quality-of-care / experience metric.

Analytical significance:

o	Captures perceived service quality

o	Can be correlated with patient volume

o	Helps detect performance vs workload dynamics

**Combined Analytical Insight:**

This tooltip enables micro-level performance assessment:

```Dr. Emma Jones manages a high patient volume (4,973) while maintaining a strong satisfaction score (4.21), suggesting effective service delivery under workload pressure.```

In dashboard design terms, this tooltip supports:

✔ Provider benchmarking

✔ Workload vs quality evaluation

✔ Drill-down analysis from aggregated visuals

<img width="888" height="503" alt="d3 with tooltips" src="https://github.com/user-attachments/assets/647e7ef2-eae4-4c52-98a4-f8425c457797" />
_____________________________________________________________________________________________________________________________________________________________________________________________
## Overall Interpretation Across All Visuals

Together, these visuals create a comprehensive healthcare analytics framework:

1.	Data Model → Ensures structured, scalable analytics.

2.	Executive Dashboard → Communicates financial and categorical performance.

3.	Trend Dashboard → Enables temporal, variance, and operational analysis.
   
4.	Hospital Performance & Care Utilization Dashboard → A consolidated view of patient volumes, admission patterns, emergency vs non-emergency demand, departmental workload, length of stay, temporal trends, and patient satisfaction to support operational and clinical decision-making.
____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

## DAX AND MEASURES: 
```
Out of Pocket = [Total Billing Amount]-[Total insurance cost]
```
```
Total Billing Amount = [Total room charges]+[Total medication cost]+[Total Treatment cost]
```
```
Total insurance cost = sum(visits[Insurance Coverage])
```
```
Total medication cost = sum(visits[Medication Cost])
```
```
Total room charges = SUMX(visits, visits[Room Charges(daily rate)]*visits[Length of stay])
```
```
Total Treatment cost = sum(visits[Treatment Cost])
```
```
_Previous month billing Amount = CALCULATE([Total Billing Amount], DATEADD(DateTable[Date],-1, MONTH))
```
``` 
% Department = 
  DIVIDE(
    [Total Billing Amount], 
  CALCULATE([Total Billing Amount],ALL(departments[Department]))
  )
```
```
% Procedure = 
  DIVIDE(
    [Total Billing Amount], 
  CALCULATE([Total Billing Amount],ALL(procedures[Procedure]))
  )
```
```
Active departments = SELECTEDVALUE(departments[Department])
```
```
Average Billing Amount per visit = DIVIDE([Total Billing Amount], [Total Patients])
```
```
Average Insurance Coverage = AVERAGE(visits[Insurance Coverage])
```
```
Average length of stay = AVERAGE(visits[Length of stay])
```
```
Average Medication Cost = AVERAGE(visits[Medication Cost])
```
```
Average Out of Pocket = DIVIDE([Out of Pocket], [Total Patients])
```
```
Average Patient satisfactiion score = AVERAGE(visits[Patient Satisfaction Score])
```
```
Average Room Charges = DIVIDE([Total Room charges], [Total Patients])
```
```
Average Treatment Cost = AVERAGE(visits[Treatment Cost])
```
```
Blankmeasure = 0
```
```
Previous weekday billing Amount = 
VAR _currentWeekday= SELECTEDVALUE(DateTable[WeekDay])
VAR _Previousweekday= 
switch(
    _currentWeekday,
    "Mon", "Sun",
    "Tue", "Mon",
    "Wed", "Tue",
    "Thr", "Wed",
    "Fri", "Thr",
    "Sat", "Fri",
    "Sun", "Sat",
    BLANK()
)
RETURN
CALCULATE (
    [Total Billing Amount],              -- your base measure
    DateTable[WeekDay] = _Previousweekday,
    ALL(DateTable)
)
```
```
Total Patients = DISTINCTCOUNT(visits[Patient ID]) 
```
```
% Emergency = 
VAR _TotalVisit =
    CALCULATE ( [Total visit], visits[Visit Type] = "Emergency" )

VAR _Admitted =
    CALCULATE ( [Total Admitted], visits[Visit Type] = "Emergency" )

VAR _Outpatient =
    CALCULATE ( [Total outpatient], visits[Visit Type] = "Emergency" )

VAR _Switchmeasures = 
    SWITCH (
        TRUE(),
        SELECTEDVALUE ( 'Change Measures'[Change Measures Order] ) = 0, [Total visit],
        SELECTEDVALUE ( 'Change Measures'[Change Measures Order] ) = 1, [Total Admitted],
        [Total outpatient]
    )

VAR _Switchvar =
    SWITCH (
        TRUE(),
        SELECTEDVALUE ( 'Change Measures'[Change Measures Order] ) = 0, _TotalVisit,
        SELECTEDVALUE ( 'Change Measures'[Change Measures Order] ) = 1, _Admitted,
        _Outpatient
    )

RETURN
IF (
    _Switchvar < _Switchmeasures,
    DIVIDE ( _Switchvar, _Switchmeasures, 0 ),
    DIVIDE ( _Switchmeasures, _Switchvar, 0 )
)
```
```
% Non Emergency = 
VAR _TotalVisit =
    CALCULATE ( [Total visit], visits[Visit Type] = "Non Emergency" )

VAR _Admitted =
    CALCULATE ( [Total Admitted], visits[Visit Type] = "Non Emergency" )

VAR _Outpatient =
    CALCULATE ( [Total outpatient], visits[Visit Type] = "Non Emergency" )

VAR _Switchmeasures = 
    SWITCH (
        TRUE(),
        SELECTEDVALUE ( 'Change Measures'[Change Measures Order] ) = 0, [Total visit],
        SELECTEDVALUE ( 'Change Measures'[Change Measures Order] ) = 1, [Total Admitted],
        [Total outpatient]
    )

VAR _Switchvar =
    SWITCH (
        TRUE(),
        SELECTEDVALUE ( 'Change Measures'[Change Measures Order] ) = 0, _TotalVisit,
        SELECTEDVALUE ( 'Change Measures'[Change Measures Order] ) = 1, _Admitted,
        _Outpatient
    )

RETURN
IF (
    _Switchvar < _Switchmeasures,
    DIVIDE ( _Switchvar, _Switchmeasures, 0 ),
    DIVIDE ( _Switchmeasures, _Switchvar, 0 )
)
```
```
% R Emergency = 1-[% Emergency] 
```
```
% R Non Emergency = 1-[% Non Emergency]
```
```
Average satisfaction score = 
VAR _score= AVERAGEX(values(visits[Provider ID]),CALCULATE(AVERAGE(visits[Patient Satisfaction Score])))
RETURN
"Avg Rating:" & " " & FORMAT(_score, "0.00")
```

```
Patient satisfaction  score = 
VAR _score= AVERAGEX(values(visits[Provider ID]),CALCULATE(AVERAGE(visits[Patient Satisfaction Score])))
RETURN
"Patient Satisfaction Score:" & " " & FORMAT(_score, "0.00")
```
```
Total Admitted = [Total visit]-[Total outpatient]
```
```
Total outpatient = COUNTBLANK(visits[Length of stay])
```
```
Total visit = COUNTROWS(visits)
```
```
Switch Date = {
    ("WeekDay", NAMEOF('DateTable'[WeekDay]), 0),
    ("WeekType", NAMEOF('DateTable'[WeekType]), 1),
    ("Quarter", NAMEOF('DateTable'[Qtr]), 2),
    ("Month", NAMEOF('DateTable'[Month]), 3),
    ("Year", NAMEOF('DateTable'[Year]), 4)
}
```
```
Change Measures = {
    ("Total visit", NAMEOF('DAX MEASURES'[Total visit]), 0),
    ("Total Admitted", NAMEOF('DAX MEASURES'[Total Admitted]), 1),
    ("Total outpatient", NAMEOF('DAX MEASURES'[Total outpatient]), 2)
}
```
```
DateTable = 
ADDCOLUMNS(
    CALENDARAUTO(),
"Year", YEAR([Date]),
"Month", FORMAT([Date],"mmm"),
"Monthnum", MONTH([Date]),
"WeekDay", FORMAT([Date],"ddd"),
"WeekNum", WEEKDAY([Date]),
"Qtr", "Q-"& QUARTER([Date]),
"WeekType", IF(WEEKDAY([Date])= 1 || WEEKDAY([Date])= 7 ,"Weekend","Weekday")
)
```
```
[Patient Location Switch ] = {
    ("City", NAMEOF('cities'[City]), 0),
    ("State", NAMEOF('cities'[State]), 1)
}
```


