# Exploratory Data Analysis of Bicycle Accidents In Great Britain (1979 - 2018)
Bicycles for rent are now a popular means of transport in London especially when there are train cancellations or strikes.
There are several providers of this service with Lime and Forest as the most popular e-bike options.
Santander also offers pedal bicycles across the city.

-----------------------------------------------------------------------------------------
Cycling combines exercise and convenient city transport. It improves the cardiovascular and peripheral muscle tone[Reference]
However, this healthy and active transportation has its downsides. Cycling accidents can increase cost burden to NHS, productivity loss and long term disability. This is therefore an attempt to highlight trends in the public health impact of cycling in London using data from
https://www.kaggle.com/datasets/johnharshith/bicycle-accidents-in-great-britain-1979-to-2018/data

-----------------------------------------------------------------------------------------
## Summary of Hypothesis:
- H0: There are no differences/relationships between environmental/personal factors and the severity/casualties of bicycle accidents
- H1: There are differences/relationships between environmental/personal factors and the severity/casualties of bicycle accidents

- Population: UK cyclists involved in accidents(1979 - 2018)
- Independent Variable(s): Environmental factors(road conditions, road type, lighting condition, weather condition, time of the day) and Individual factors(gender, age group)
- Dependent Variable(s): Severity and Number of casualties

-----------------------------------------------------------------------------------------
## Methods
This data analysis involved the following steps using the Python data ecosystem:
- Load libraries and datasets
- Summarise and clean datasets
- Univariate and Bivariate Descriptive data analysis
- Hypothesis tests
- Results and Findings
- Comments
- Limitations

-----------------------------------------------------------------------------------------
## Results and Findings
- Number of vehicles: 
The mean and median of the number of vehicles involved in bicylce accidents was 1.98 and 2.0 respectively. The mode of this feature was 2 vehicles with a count of 758784 incidents. The variance and standard deviation of this feature was 0.097 and 0.311 respectively. The range of the number of vehicles was 12 and the inter-quartile range (IQR) was 0.0. Hence majority of bicycle accidents involve two vehicles.

- Number of casualties: 
The mean (1.047), median (1.0) and mode (1, count = 792685) were close for the number of casualties in bicycle accidents. The standard deviation was 0.253. The range and IQR were 59 and 0.0 respectively. Therefore there is mostly a single casualty in accidents. 

- Speed Limit: 
The average speed limit of roads that accident occured on was 33.340. The middle speed value after arranging the data in order was 30.0. The most common occuring speed limit was 30.0 with 686784 incidents. The variance was calculated to be 85.610.The average difference between values and the mean was 9.252. The difference between the largest and smallest speed limit was 70.0. The IQR was 0.0. Therefore a majority of accidents happen on low speed limit roads (30)

- Accident Severity: 
The distribution of accident severity was slight(n=681578, 82.32%), serious(n=139563, 16.85%) and fatal(n=6730, 0.81%)

- Test of normality:   
Number of vehicles(Statistic: 0.4672, p-value: 0.0000), Number of casualties(Statistic: 0.5314, p-value: 0.0000)
and speed limit (Statistic: 0.4839,  p-value: 0.0000) were statistically (Kolmogorov-Smirnov Test) and
visually(q-q plot, box-plot) determined to have a non-normal distribution.

-----------------------------------------------------------------------------------------
### Environmental Factors  
#### Road conditions on Number of casualties / Severity
- Dry roads (n=633936, 76.57%) had the highest total casualties. Subsequently was wet roads(n=184279, 22.25%). The Kruskal-Wallis test showed there was a significant difference between the distribution of casualties observed on different road conditions(H = 161.78, p < 0.001). The effect size was(epsilon-square) was 0.000195. Although the differences are significant the practical magnitude is small. The average number of casualties was still ONE(1) in any road conditions. The difference was most statistically strongest on dry and wet roads.

- Wet(residuals: fatal= +3.046,  serious= +2.63) and Flood(residuals: fatal= +1.91,  serious= +2.65) had the highest proportion of fatal and serious accidents. The association between road conditions with reference to severity was staistically significant (chi_statistic = 78.14, p < 0.001, cramers-v = 0.00687). Based on the cramers-v, the overall practical impact of road conditions on severity is negligible. Wet and frost show statistically significant associations with more severe outcomes.

#### Weather conditions on Number of casualties / Severity
- Clear weather (n=683162, 82.52%) and rain(n=82007, 9.90%) had the highest proportion of casualties. The difference between accident casualties during various weather conditions was statistically significant(H = 333.94, p < 0.001) with an effect size of 0.000403. The practical magnitude of weather conditions on the casualties per record is small. Evidence showed slightly higher mean casualties per record in clear conditions and does not show adverse weather conditions(snow, fog, rain) have more casualties per accident.

- Clear and windy(residuals: fatal= +6.33, serious= +7.08), rain and windy(residuals: fatal= +5.36, serious= +2.46), fog(residuals: fatal= +2.79, serious= +2.22) had the highest rates for severe injuries. Weather conditions and accident severity was statistically related (chi_statistic = 480.79, p < 0.001, cramers-v = 0.0170) but the practical implications are negligible based on the Cramer's V. Windy conditions and fog were statistically had more severe injuries.

#### Road type on Number of casualties / Severity
- Single carriageway(n=656703, 79.32%), Roundabout(n=75066, 9.06%) and Dual carriageway(n=59037, 7.13%) had the highest total casualty numbers. The distribution of casualties per accident statistically differed between road types (H = 1339.483, p < 0.001) with an effect size of 0.00161. This suggests that the association of road types with the number of casualties per accident was minor.

- Dual carriageway(residual: fatal= +35.01,  serious= +13.26), Slip road(residual: fatal= +0.046, serious= +0.86)	and Single carriageway(residual: fatal= -3.730, serious= +7.71) had the highest rate of fatal accidents. The association between road types and accident severity was statistically significant (chi_statistic = 2884.07, p = 0.0, cramers_v = 0.0417). Despite strong statistical significance, road type has negligible impact on variance in severity. Dual carriageways had the most severe injuries statistically.

- The severity of accidents when comparing road types and light conditions was assessed. Darkness no light had the most severe accidents on all road types with the exception of roundabouts. Slip road with Darkness no lights	(fatal=3.85%, serious=30.77%) and Dual carriageway with Darkness no lights(fatal=10.56%, serious=30.02%) had the worst injury severity.

- Dual carriageway had the most severe accident injuries in any weather condition. 


#### Light conditions on Number of casualties / Severity 
- The highest number of records occured during Daylight(n=660657, 79.80%) and Darkness lights lit (n=142039,	17.15%). The difference between light conditions was statistically significant (H = 272.41, p <0.001) with an effect size of 0.000329; the practical magnitude of light was therefore found to be negligible.

- Light conditions and the severity of accidents have a statistically significant but weak association (chi_statistic = 2923.25, p = 0.0, cramers-v = 0.0420). Darkness lights lit (residuals: fatal= +44.56, serious= +22.97) and Darkness no lights (residuals: fatal= -2.46, serious= +6.63%) had more severe accident injuries.
-----------------------------------------------------------------------------------------
### Time  

#### Traffic status on Number of casualties / Severity: 
- The highest number of accident records was observed during Morning Rush Hour(n=166617, 20.12%), Day Off-Peak(n=197129, 23.81%), Evening Rush Hour(n=214741, 25.93%). The difference was statistiaclly significant (H = 300.66, p < 0.001) with an effect size of 0.000363. The Morning Rush Hour period was statistically different from all other periods while all other periods had insignificant differences from one another. The effect size shows the that traffic status has negligible practical magnitude on casualties per accident.

- The association between the traffic status and accident severity was statistically significant but weak (chi_statistic = 1474.4563765293549, p = 0.0, cramers-v = 0.029). Night time and dawn is when the most severe injuries occured.

#### Day on Number of casualties / Severity: 
- Accidents were more common on week days than weekends. Wednesday(16.52%), Tuesday(16.49%), Thursday(16.46%), Friday(15.95%), Monday(15.19%), Saturday(10.59%), Sunday(8.80%). The difference between the number of casualties per accident was statistically significant (H = 628.1438, p < 0.001) with an effect size of 0.000758. Saturday and Sunday were statistically different from weekdays and each other. There was no statistical difference between the weekdays. The practical magnitude of the day of the week on the number of casualties per accident was negligible.

- The weekends had the highest severe accidents with Sunday(1%) and Saturday(0.81%) having the highest fatal rate
- Chi-sqaure for severity x day
- Number of casualties are higher during warmer periods(May to October)

-----------------------------------------------------------------------------------------
### Individual Factors
- The most common accident severity category was Slight(n=681578, 82.32%) whiles Fatal(n=6730, 0.81%%) was the least common.
- This distribution of severity across gender and age groups was similar to the distribution observed in the entire dataset.
- For females the most common age group was 21 to 25(25.67%), 56 to 65(24.16%) and 46 to 55(23.54%). The most common age group among males was 11 to 15(84.79%), 6 to 10 (82.68%) and 16 to 20(81.50%)

#### Age Group on Number of casualties / Severity 
- By age group, 11 to 15 (n= 169945, 20.05%), 26 to 35 (n=145081, 17.52%) and 16 to 20(n=122604, 14.80%) were the most frequently involved in accidents. 56 to 65(n=41913, 5.06%) and 66 to 75(n=15663, 1.89%) were the least frequently involved in bicycle accidents. The Kruskal-Wallis test indicated the differences were significant (H: 1287.28, p < 0.001). The effect size was observed as 0.00155.  This indicates minimal practical magnitude on the number of casualties per accident.
  
- The association between severity between the age group (chi_statistic = 7371.50, p = 0.0, cramers-v = 0.066) was statistically significant with a weak magnitude. The residuals of severity(fatal and serious) among age groups were the following 66 to 75(residuals: fatal= +42.06, serious= +28.40), 46 to 55(residuals: fatal= +12.71, serious= +23.95), 56 to 65(residuals: fatal= +28.40, serious= +32.90). Fatal and serious injuries increase with age.

#### Gender on Number of casualties / Severity
- A majority of accidents involved Males(n= 660031, 79.72%). Females(n=167721) were involved in 20.25% of accidents. Other(119) were involved in 0.014% of accidents. By gender, The difference between the various genders was observed to be statistically signigicant (H = 24.72, p < 0.001). The effect size was 0.0000298. This implies the practical magnitude of gender on casualties by accident is negligible. No statistically significant difference was observed between Other and male and female gender groups.
  
- Males experienced more serious, fatal injuries than females and others based on the mean ranking. However, females experience more slight injuries than males. An assumption for the chi-square test were not met. This was because the percentage of expected values less than 5 (33.33%) exceeded 20%. The Kruskal-Wallis test was run instead. The Kruskal-Wallis test indicated the differences were significant (H: 152.717, p < 0.001). The effect size was observed as 0.000184.  This indicates minimal practical magnitude on the number of casualties per accident.

-----------------------------------------------------------------------------------------
#### Comments
- The null hypothesis was rejected for all factors versus number of casualties. All parent environmental factors showed statistically detectable differences but with negligible practical magnitude on the number of casualties per accident. The large size of the dataset contributed to the strong statistical significance yet minor effective size.
- Bad weather does not result in increased casualties per accident. Windy conditions and fog may increase injury severity.
- Dual carriageways are extremely dangerous for fatal and serious bicycle accidents. Roundabouts and oneway streets had the least severe injuries.
- Darkness without lights are extremely dangerous. Street lights reduce accident severity. Nightime lit park bicycle paths?? High visibility clothing/stickers.
- Rush hours shows the safest outcomes despite high traffic volume. Most fatal and serious bicycle accidents occur at night and dawn. Possible reasons: Tiredness, Intoxication, Lighting.
- Majority of cycle accidents are slight which may indicate effectiveness of current interventions. Severe and fatal injuries are more common in males hence targetting this group in interventions may be helpful.Further investigation to explain the rationale for the gender differences is necessary [Injury severity over time??]
- Fatal and serious injuries are more common in the elderly. Preventing accidents in older cyclists should be a priority. Targetted campaigns, special cycle features such as collision warning and specialised medical response in areas with elderly cylists may help reduce accidents and manage trauma in elderly cyclists.
- Most fatal and serious accidents happen on weekends. Emergency Response teams?? may
- For typical road conditions wet, dry and snow had the worst accident severity in descending order.  
- High accidents on dry and clear roads
- Severe accidents on dual carriage way(irrespective of light)


-----------------------------------------------------------------------------------------
#### Limitations
- The other gender catergory was not investigated due to small numbers. The Chi-square test was not feasible for gender and severity. A Fisher–Freeman–Halton exact test was a considered option but not directly available in python. The 'Other' group was therefore excluded and the test was rerun
- The speed limit and number of vehicles were not investigated as factors in this analysis.
- Extensive multivariate analysis was not conducted. - Environmental and human factors were investigated individually. 
- Missing(road conditions = 0.19% vs flood = 0.03%) and unknown data(weather conditions = 2.9%; third in frequency, road type = 3.70% vs one-way street(0.67%) and slip roads(0.10%)) values were not deleted but appropriately labelled and ignored during analysis. This is because they represented a relevant portion of data relative to other levels under the same variable and removal risked possible distortion.
- There were outliers in the number of casualties column but there were not removed.
  
-----------------------------------------------------------------------------------------
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
- https://www.kaggle.com/code/prashant111/complete-guide-on-time-series-analysis-in-python
- https://claude.ai/
- https://chatgpt.com/