# Thermal-Comfort-Prediction

## Probelm Statements:

Majority  of  energy  consumption  in buildings  is  due  to  air-conditioning,  because  of hot  and humid  weather.    Besides  attaining  a  healthy  indoor environment, a  prior  knowledge  about the occupant’s thermal comfort can be beneficial in reducing energy consumption, as it can save energy which is  otherwise spent in extra cooling. 
This project is a data-driven  approach  to  predict  individual thermal  comfort using  environmental  and  human factors as input. 

## Data Collections: 

Data Preprocessing ASHRAE  is  one  of  the  main  organizations  that  set thermal comfort standards and guidelines. For this project, we have  used  the  database  of  thermal  comfort  experiments performed,  which is  publicly available  as  part  of  the  ASHRAE  RP-884  project.

## feature set:
Feature Set and Output The following factors were included in the feature set: 
Fanger’s  parameters:  The  six  Fanger’s  parameters are well established as definite influencers of thermal comfort:  air  temperature  (Ta),  mean  radiant temperature  (MRT),  relative  humidity  (RH),  air speed  (Va),  clothing  rate  (Clo),  and  metabolic  rate (M). 

Outdoor effective  temperature (ETout): The  effective temperature  indicates  the  combined  effect  of  air temperature, relative  humidity and air  velocity. 
Thus it  better  represents overall outdoor  weather, as compared to using only outdoor air temperature.  

## Model Building:

Thermal comfort has been selected as the prediction target. Dataset will be divided into target variable (i.e. Thermal comfort) and feature variables. 3 different prediction models for thermal comfort will be explored using random forest classification algorithm.

Prediction Model 1 (using 5 features)
The following 5 common features in ASHRAE thermal comfort model will be used for the first prediction model:

1) Air temperature (C)

2) Air velocity (m/s)

3) Relative humidity (%)

4) Clo

5) Met

Prediction Model 2 (using 3 features)
Question: Does reducing the number of feature variables help to improve the prediction model?

The following 3 features related to indoor environment conditions will be used for the second prediction model:

1) Air temperature (C)

2) Air velocity (m/s)

3) Relative humidity (%)

Prediction Model 3 (using 10 features)
Including in all 10 feature variables into the third prediction model to see if accuracy score can be improved:

1) Air temperature (C)

2) Air velocity (m/s)

3) Relative humidity (%)

4) Clo

5) Met

6) Season

7) Koppen climate classification

8) Building type

9) Cooling startegy_building level

10) Outdoor monthly air temperature (C)

## Conclusion
Prediction model 3, comprising of all 10 feature variables, has the best results (i.e. highest accuracy) when using random forest classification algorithm.

However, there are limitations to using this prediction model:

Dataset used for training is more skewed towards hot semi-arid climate
Dataset used for training is more skewed towards summer season
Dataset used for trinaing is more skewed towards office building type
Approximately 55% accuracy result may not be good enough to predict thermal comfort with high confidence
Recommendations:

Using more diverse and evenly distributed dataset for training (e.g. include more climate types, more different building types)
Include radiant temperature as one of the feature variables since this is one of the more recognised factor affecting thermal comfort
