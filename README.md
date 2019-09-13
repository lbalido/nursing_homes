# Nursing Home Ratings




## Introduction


As our loved ones grow older, it becomes more and more difficult for them to remain in their home by themselves. Not only are they are more prone to injuries and risks of under/over medicating, but activities of daily living such as bathing and eating become increasingly more difficult. While family and friends are able to take care of them at the beginning, many reach a point where 24 hr care is needed and they can no longer stay in their home.

Nursing homes are a great alternative when loved ones reach this point. They are facilities for people who do not need to be in hospitals, but cannot be cared for at home and offer the most extensive care a person can get outside a hospital. Most facilities have both long term and short term residents, and include services such as:

    - Acitivies of Daily living such as bathing, dressing, and eating
    - Skilled care such monitoring medications, physical therapy, occupational therapy, etc.
    - 24 hour emergency care
    - Social activities

#### How do you choose the best nursing home for your loved one? 

The Center for Medicare and Medicaid Services have developed a rating system to help with this decision. Every year an inspection is done at each nursing home throughout the US and given an overall rating from one through five. This was designed to help consumers, families, and caregivers compare nursing homes.


## Data Overview


The overall rating is based on three aspects of the nursing home:

1. Health Inspections - This rating is based on the three most recent annual health inspection investigations as well as recent inspections due to complaints. These inspections are conducted by a state employee to determine whether the nursing home has met the state's minimum quality requirements. Any deficiencies are weighted by scope and severity, and also takes into account the number of revisits required to make sure the deficiency has been corrected. 

2. Staffing - This rating has information regarding the number of hours provided on average to each resident each day. This is based on two measures: RN hours per resident and total nurse hours per resident (the sum of RNs, LPN, and nurse aides). 

3. Quality Measures - This rating is based on how well nursing homes are caring for their residents' physical and clinical needs. It includes a total of 17 measures based on performance (10 measures for long-term stays and 7 measures for short-term stays). These measures include percentage of hospitalizations or falls, new or worsened bed sores, depression, etc.

This dataset was taken from data.medicare.gov and was last updated August 1, 2019. It covers 15,512 nursing homes throughout the US with 85 different features. We are going to focus on the three aspects that make up the overall rating.


## Exploratory Data Analysis

![Rating Distributions](images/rating_distributions.png?raw=true "Title")

I wanted to focus on the data in the nursing rating dataset that related to the overall rating.  Since the overall rating is made up of the three subcategories of Health Inspections, Quality Measures, and Staffing, I took a closer look at those three.  Even though the dataset has 85 features, many of the features were not independent, and so I took the features of each subcategory that were the most comprehensive and independent. 

The Quality Measures data were all categorical, so I did not want to use that data. The Staffing data had a very small spread, this wouldn't give us much insight.  So I chose to use the health inspection scores. 

With the Health Inspection scores, the lower the scores the better the rating. FOr every complaint or deficiency, depending on the severity the nursing home is given points.  Therefore, we are looking for nursing homes with lower Health Inspection scores.





I'm interested in seeing if wealthy areas affect the scores.  In order to do this, I took another dataset that includes the 2017 GDP per capita per state. I took the mean of this set, and any states above the mean I labelled as "wealthy" and any states below the mean I labelled as "poor". The map below shows the wealthy states colored.

![GDP Per Capita Per State](slides/gdp_per_capita_map.png?raw=true "Title")



## Hypothesis Testing


Ho = There is no difference in scores between wealthy states and poor states.

Ha = The scores from wealthy states are better than poorer states

𝛼 = .05

U-test

P-value = .778




## Conclusion

I fail to reject the null hypothesis. 

This is a good sign. It means that there should not be a difference in health scores dependent on how wealthy a state is. 

