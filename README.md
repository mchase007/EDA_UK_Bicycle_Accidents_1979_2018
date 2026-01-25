# Exploratory Data Analysis of Bicycle Accidents In Great Britain (1979 - 2018)

Bicycles for rent are now a popular means of transport in London especially when there are train cancellations or strikes.
There are several providers of this service with Lime and Forest as the most popular e-bike options.
Santander also offers pedal bicycles across the city.

-----------------------------------------------------------------------------------------
Cycling combines exercise and convenient city transport. It improves the cardiovascular and peripheral muscle tone[Reference]
However, this healthy and active transportation has its downsides. Cycling accidents can increase cost burden to NHS, productivity loss and long term disability. This is therefore an attempt to highlight trends in the public health impact of cycling in London using data from
https://www.kaggle.com/datasets/johnharshith/bicycle-accidents-in-great-britain-1979-to-2018/data

-----------------------------------------------------------------------------------------
#### Summary of Hypothesis:
- H0: There are no differences/relationships between environmental/personal factors and the severity/casualties of bicycle accidents
- H1: There are differences/relationships between environmental/personal factors and the severity/casualties of bicycle accidents

- Population: UK cyclists involved in accidents(1979 - 2018)
- Independent Variable(s): Environmental factors(road conditions, road type, lighting condition, weather condition, time of the day)
                         Individual Factors(gender, age group)
- Dependent Variable(s): Severity and Number of casualties

#### Methods
This data analysis involved the following steps:
- Load libraries and datasets
- Summarise and clean datasets
- Univariate and Bivariate Descriptive data analysis
- Hypothesis tests
- Results and Findings

#### Results

- Number of vehicles
The mean and median of the number of vehicles involved in bicylce accidents was 1.98 and 2.0 respectively. The mode of this feature was 2 vehicles with a count of 758784 incidents. The variance and standard deviation of this feature was 0.097 and 0.311 respectively. The range of the number of vehicles was 12 and the inter-quartile range (IQR) was 0.0.

- Number of casualties
The mean (1.047), median (1.0) and mode (1, count = 792685) were close for the number of casualties in bicycle accidents. The standard deviation was 0.253. The range and IQR were 59 and 0.0 respectively.

- Speed Limit
The average speed limit of roads that accident occured on was 33.340. The middle speed value after arranging the data in order was 30.0. The most common occuring speed limit was 30.0 with 686784 incidents. The variance was calculated to be 85.610.The average difference between values and the mean was 9.252. The difference between the largest and smallest speed limit was 70.0. The IQR was 0.0.

- Accident Severity
The distribution of accident severity was slight(n=681578, 82.32%), severe(n=139563, 16.85%) and fatal(n=6730, 0.81%)

- Test of normality  
Number of vehicles(Statistic: 0.4672, p-value: 0.0000), Number of casualties(Statistic: 0.5314, p-value: 0.0000)
and speed limit (Statistic: 0.4839,  p-value: 0.0000) were statistically (Kolmogorov-Smirnov Test) and
visually(q-q plot, box-plot) determined to have a non-normal distribution.

##### Environmental Factors
- Accidents happened the most frequently on dry(n=633936, 76.58%) and wet(n=184279, 22.26%) road conditions.
- Accidents occured overwhelmingly on days with clear(n=683162, 82.5%) weather.
- Single carriageways(79.33%) were the road type where accidents occured the most.
- 30647(3.70%) accidents occured on roads where the road type was not know.
- Accidents occured the most during day light (n=660657, 79.80%)
  
- Road conditions on Number of casualties / Severity
Dry roads (n=633936, 76.57%) had the highest number of casualties. Subsequently was wet roads(n=184279, 22.25%). The Kruskal-Wallis test showed the was a significant difference between the number of casualties observed on different road conditions(H = 161.78, p < 0.001). The effect size was(epsilon-square) was 0.000195. The difference between road conditions with reference to severity was staistically significant (chi_statistic = 78.14, p < 0.001, cramers-v = 0.00687)

- Weather conditions on Number of casualties / Severity
Clear weather (n=683162, 82.52%) and rain(n=82007, 9.90%) had the highest casualty numbers. The difference between accident casualties during various weather conditions was statistically significant(H = 333.94, p < 0.001) with an effect size of 0.000403. The difference between weather conditions and accident severity was statistically significant (chi_statistic = 480.79, p < 0.001, cramers-v = 0.0170)

- Road type on Number of casualties / Severity
Single carriageway(n=656703, 79.32%), Roundabout(n=75066, 9.06%) and Dual carriageway(n=59037, 7.13%) had the highest casualty numbers. The difference between road types was statistically significant (H = 1339.483, p < 0.001) with an effect size of 0.00161. The difference between road types and accident severity was statistically significant (chi_statistic = 2884.07, p = 0.0, cramers_v = 0.0417).

- Light conditions on Number of casualties / Severity
The highest number of casualties occured during Daylight(n=660657, 79.80%) and Darkness lights lit (n=142039,	17.15%). The difference between light conditions was statistically significant (H = 272.41, p <0.001) with an effect size of 0.000329. The difference between light conditions and the severity of accidents was statistically significant (chi_statistic = 2923.25, p = 0.0, cramers-v = 0.0420).

##### Time  
- Traffic status on Number of casualties / Severity
The highest number of casualties was observed during Day Off-Peak(n=197129,	23.81%), Day Off-Peak(n=197129,	23.81%),Evening Rush Hour(n=214741,	25.93%)
and the Morning Rush Hour(n=166617,	20.12%). The difference was statistiaclly significant (H = 300.66, p < 0.001) with an effect size of 0.000363. The difference between the traffic status and accident severity was statistically significant (chi_statistic = 1474.4563765293549, p = 0.0, cramers-v = 0.029).

- Day on Number of casualties / Severity
- Accidents were also common on week days than weekends. Wednesday(16.52%), Tuesday(16.49%), Thursday(16.46%), Friday(15.95%), Monday(15.19%), Saturday(10.59%), Sunday(8.80%). The difference was statistiaclly significant (H = 628.1438, p < 0.001) with an effect size of 0.000758. 


##### Individual Factors
- The most common accident severity category was Slight(n=681578, 82%) whiles Fatal(n=6730, 1%) was the least common.
- This distribution of severity was also observed when severity was compared to gender and age group.
- A majority of accidents involved Males(n= 660031, 79%). Females(n=167721) were involved in 20% of accidents.
- By age group, 11 to 15 (n= 169945, 21%), 26 to 35 (n=145081, 18%) and 16 to 20(n=122604, 15%) were the most frequently involved in accidents.
- 56 to 65(n=41913, 5%) and 66 to 75(n=15663, 2%) were the least frequently involved in bicycle accidents.
- The most males were in the 11-15(21.83%) age group and the 26-35(19.50%) age group was the most common among females.
  
- Age Group on Number of casualties / Severity
The highest number of casualties was observed in the 16 to 20 (n=122602, 14.80%), 26 to 35 (n=145078, 17.52%) and 11 to 15 (n=169943, 20.52%) age groups. The Kruskal-Wallis test indicated the differences were significant (H: 1287.28, p < 0.001). The effect size was observed as 0.00155.

The distribution of severity(fatal and serious) among age groups were the following 66 to 75(fatal(%)=3.84, serious(%)=26.18), 36 to 45(fatal(%)=0.78, serious(%)=17.26), 46 to 55(fatal(%)=1.24, serious(%)=20.48), 56 to 65(fatal(%)=2.06, serious(%)=23.46). The difference of severity between the age group (chi_statistic = 7371.50, p = 0.0, cramers-v = 0.066) was statistically significant 


- Gender on Number of casualties / Severity
By gender, The difference between the various genders was observed to be statistically signigicant (H = 24.72, p < 0.001). The effect size was 0.0000298 These were the distribution of casualties by gender: Other(n=119, 0.014%), Female(n=167717, 20.25%) and Male(n=660025, 79.72%). 

The proportion of fatal and serious injuries were reported as Female(fatal(%)=0.71, serious(%)=16.01) and Male(fatal(%)=0.84, serious(%)=17.08). An assumption for the chi-square test were not met. This was because the percentage of expected values less than 5 (33.33%) exceeded 20%. The hypothesis was therefore not tested on these features.


Speed limit x Number of casualties
Little to no correlation (0.071)

Number of vehicles x Number of casualties
Very weak positive correlation (0.14)

#### Findings


#### Limitations
- The Chi-square test was not feasible for gender and severity. A Fisher–Freeman–Halton exact test was a considered option but not directly available in python.
- The speed limit and number of vehicles were not investigated as factors in this analysis.
- Missing and unknown data values were not deleted but appropriately labelled and ignored during analysis.
- There were outliers in the number of casualties column but there were not removed

#### References
- Mishra, P., Pandey, C. M., Singh, U., Gupta, A., Sahu, C., & Keshri, A. (2019). Descriptive statistics and normality tests for statistical data. Annals of cardiac anaesthesia, 22(1), 67–72. https://doi.org/10.4103/aca.ACA_157_18.
- Oluleye, A. (2023). Exploratory data analysis with Python cookbook: Over 50 recipes to analyze, visualize, and extract insights from structured and unstructured data. Packt Publishing
- Bettany-Saltikov, J., & Whittaker, V. J. (2014). Selecting the most appropriate inferential statistical test for your quantitative research study. Journal of clinical nursing, 23(11-12), 1520–1531. https://doi.org/10.1111/jocn.12343
- Peacock, Janet, and Philip Peacock, Oxford Handbook of Medical Statistics, 1 edn, Oxford Medical Handbooks (Oxford, 2010; online edn, Oxford Academic, 1 June 2011), https://doi.org/10.1093/med/9780199551286.001.0001
- Dinno, A. (2015). Nonparametric Pairwise Multiple Comparisons in Independent Groups using Dunn’s Test. The Stata Journal: Promoting Communications on Statistics and Stata, 15(1), 292-300. https://doi-org.ezproxy.tees.ac.uk/10.1177/1536867X1501500117 (Original work published 2015)
- Fiel Peres F. Effect sizes for nonparametric tests. Biochem Med (Zagreb). 2026 Feb 15;36(1):010101. doi: 10.11613/BM.2026.010101. Epub 2025 Dec 15. PMID: 41399660; PMCID: PMC12701665.
- Cramer, D., & Howitt, D. L. (2004). The SAGE Dictionary of Statistics: A Practical Resource for Students in the Social Sciences. SAGE Publications Ltd.
- King, B. M., Rosopa, P. J., & Minium, E. W. (2018). Statistical reasoning in the behavioral sciences (7th ed.). John Wiley & Sons. 
- https://peterstatistics.com

#### To-do list
- Adjusted standardised residual tests??
- Dunn's test??
- Time series analysis??