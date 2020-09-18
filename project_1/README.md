# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: SAT & ACT Analysis

### John Lim Jian Ann, DSI-17-Singapore

### Problem Statement

College Board (the organization that administers the SATs) are looking to increase participation rates among high schools in the United States as they are worried about the increasing popularity of ACT test.

College Board want to increase the SAT participation rate and would like to have data driven recommendations in doing so.


### Executive Summary

This project requires the examination of data of the 2017 and 2018 ACT and SAT participation rates and test scores for each state. The aim is to give deeper insights and analysis into these data sets and provide data driven recommendations to College Board on ways to improve SAT participation rate. We found a strong negative correlation between a change in average scores and participation rate in ACT test. There is also a negative correlation between the change in total scores and participation rate in SAT test.

This means a higher overall score might lead to a lower participation rate or vice versa. There is a relatively high positive correlation between change in change in SAT participation and change in ACT average score, and a positive correlation between change in ACT participation and change in change in SAT total score.

This finding suggests that a reduction in test difficulty might lead to a positive change in participation. However, as each state has different college enrollment population size,

we need to analyse deeper. A high negative correlation between the change in SAT participation and change in ACT participation is observed and this strongly implies falling participation rate from ACT/SAT could lead to increasing participation rate in SAT/ACT.



### Conclusions and Recommendations

Base on the findings we believe that instead of looking at the participation rate for each individual state, we should look into the total college enrollment size for each state as a high participation rate with a low population may have a lower absolute enrollment than a lower participation rate with a high participation rate.

We analyse the data and concluded that we want to focus on 2 groups. For both groups, we will only have states above 500,000 expected college enrollment. For the first group, we focus on states where the participation rates are above 40% and below 60%. These states are California, Florida, South Carolina, North Carolina and Oregon. California is a state that we want to place more emphasis in as there is a very high college enrollment size over 6 million. These states have apprximately 50% participation rate which implies these states are not exactly leaning towards taking SAT or ACT. Although we see that political standing of a particular state does not necessarily lead to a state leaning towards SAT or ACT, even if it does, looking at this set of data gives you a more neutral outlook and we can focus on these states without political intervention.

We recommend SAT to ramp up marketing campaigns in these area to improve the branding of SAT and improve over all participation rate over the years.

The other group we want to focus on are those that have above 60% participation rate. We have states like Texas, New York, Illinois, Geogria, Pennsylvania, Michigan, New Jersey, Virginia, Washington, Indiana, Massachusetts, Colorado, Maryland and Connecticut. In this group, SAT participation rate is higher and there is probably a substantial SAT reputation for high school students.

We further classify them into immature markets and mature markets. Immature markets are states with SAT participation rates that are above 60% and 90%. For this class, we recommend to improve marketing efforts to improve the branding that SAT already have and at the same time not fall below the 60% participation region. We might want to focus on Texas where participation is relatively high at 66% and college enrollment size above 5 million.

For the mature markets, we have states with SAT participation rates of above 90%. For this class, SAT already has a strong presence and branding. We recommend the college board leverage on its brand that it already has and maintain marketing efforts to ensure it competitiveness and presence.

We also found out that Colorado, Illinois and Rhode Island made it mandatory for all high school juniors to take SAT exam. This led to a substantial increase in SAT participation in 2018. We recommend that college board continue efforts to work with states to make SAT mandatory for high school students.


### Data

Data sources:
- ACT/SAT 2017 and 2018 were provided. Compared results to these sites:
	* https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/
	* https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows


- Population data was obtained from this site:
	* https://nces.ed.gov/programs/digest/d19/tables/dt19_203.20.asp

- Election data was obtained from this site:
	* https://www.kaggle.com/benhamner/2016-us-election


Updated data dictionary of final :

|Feature|Type|Dataset|Description|
|---|---|---|---
|State|object|final|States in the US|
|sat2017_participation|float|final|SAT 2017 Participation rate per state|
|sat2017_reading|int|final|Average score for Evidence-Based Reading and Writing in SAT 2017 for each state|
|sat2017_math|int|final|Average score for Math in SAT 2017 for each state|
|sat2017_total|int|final|Average total score in SAT 2017 for each state|
|act2017_participation|float|final|ACT 2017 Participation rate per state|
|act2017_english|float|final|Average score for English in ACT 2017 for each state|
|act2017_math|float|final|Average score for Math in ACT 2017 for each state|
|act2017_reading|float|final|Average score for Reading in ACT 2017 for each state|
|act2017_science|float|final|Average score for Science in ACT 2017 for each state|
|act2017_composite|float|final|Average score for ACT 2017 for each state|
|sat2018_participation|float|final|SAT 2018 Participation rate per state|
|sat2018_reading|int|final|Average score for Evidence-Based Reading and Writing in SAT 2018 for each state|
|sat2018_math|int|final|Average score for Math in SAT 2018 for each state|
|sat2018_total|int|final|Average total score in SAT 2018 for each state|
|act2018_participation|float|final|ACT 2018 Participation rate per state|
|act2018_english|float|final|Average score for English in ACT 2018 for each state|
|act2018_math|float|final|Average score for Math in ACT 2018 for each state|
|act2018_reading|float|final|Average score for Reading in ACT 2018 for each state|
|act2018_science|float|final|Average score for Science in ACT 2018 for each state|
|act2018_composite|float|final|Average score for ACT 2018 for each state|
|act_change_participation|float|final|Change in ACT Participation rate per state from 2017 to 2018|
|sat_change_participation|float|final|Change in SAT Participation rate per state from 2017 to 2018|
|act_change_composite|float|final|Change in ACT average score per state from 2017 to 2018|
|sat_change_composite|float|final|Change in SAT total score per state from 2017 to 2018|
|abbrev|object|final|Abbreviation of US states|
|party|object|final|Democrat or Republician state|
|enrollment_size_2018|int|final|Expected number of college enrollment per state|