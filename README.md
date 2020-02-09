# DSI Project 4: West Nile Virus Prediction
By: Kelvyn, Willy, Jia Chi

## Problem Statement:
West Nile virus (WNV) is a single-stranded RNA virus which causes West Nile fever. While WNV is commonly spread to humans through mosquitoes, the primary hosts and source of WNV are actually in birds. Fortunately, most people who are infected with WNV exhibit no symptoms. However, approximately 1 in 5 people with WNV will develop a fever and other symptoms. Slightly less than 1% of infected patients will serious neurological illnesses that can result in death.

The city of Chicago and the Chicago Department of Public Health (CDPH) has been running a comprehensive surveillance and control program to combat the spread of WNV. Since 2004, Chicago health officials have been laying and testing mosquito traps so as to designate pesticide spraying efforts to control mosquito numbers. However, in spite of these steps, WNV continues to be present in Chicago.

To better formulate action strategies and to prevent a possible WNV outbreak, Chicago city officials have tasked us to develop a model to that will better help them predict the presence of WNV, and to let them effectively allocate resources towards preventing transmission of this potentially deadly virus. Using the provided NOAA weather data, CDPH trap location, testing, and spraying data, our model's efficacy will be assessed through a Kaggle submission, as well as a project report (Jupyter Notebook) and presentation to CDC and Chicago city officials about our key findings are recommendations.

## Executive Summary:
Contents:
1. Problem Statement
2. Executive Summary
3. Importing the Libraries
4. Importing in the Kaggle Data
5. Inspecting and cleaning the Training and Test dataset
6. Inspecting the Weather dataset
7. Inspecting the Spray dataset
8. Merging the Training/Test Datasets with Weather Datasets
9. Exploratory Data Analysis (EDA))
10. Feature Selection and Engineering
11. Data Modelling
12. Model Evaluation
13. Model Intepretation and Findings
14. Conclusions and Recommendations
15. References

## Data Dictionary
As this is a Kaggle competition, the data dictionary can be found at the following link:

https://www.kaggle.com/c/predict-west-nile-virus/rules

## Model Evaluation
The best model for predicting WNV is AdaBoost+SMOTE

|Model|Kaggle Private|Kaggle Public
|:-------|------------|------------|
|**DecisionTree + SMOTE**|0.645|0.658|
|**RandomForest + SMOTE**|0.639|0.651|
|**Gradient + SMOTE**|0.662|0.684|
|**AdaBoost + SMOTE**|0.687|0.698|

## Key Findings
- The presence of long daylight hours has a negative impact on the presence ov WNV.
- Only certain species of mosquitoes (Culex Restuans/Culex Pipiens) are able to transmit WNV.
- Certain geographical locations (longitudes/latitudes/trapIDs) have a higher or lower prevalence of WNV.
- Mosquito spraying efforts in 2011 and 2013 have largely failed to target the key WNV hotspot regions.

## Recommendations
**1) The study of seasonal weather patterns on mosquito behaviour**
As observed by how the amount of daylight-hours impact the presence of WNV, the relationship between the 2 is still unclear. To provide granular neighbourhood/block specific meteorological data, future projects should consider recruiting State and Local authorities to utilize their weather data collection resources.
 
**2) Understanding how WNV is transmitted by mosquitos**
As WNV is only transmitted by 2 species of mosquitoes (Culex Restauns/Pipiens), from a city management and health perspective, understanding the behaviors and habitats of these mosquitoe species will enable better modelling of effective mosquito eradication efforts.

**3) Consolidated mosquito spraying efforts**
To maximise city resources, all mosquito-borne disease statistics should be reported into a central repository. That way, possible mosquito-borne disease transmissions may be monitored and appropriate steps taken quickly. Regular mosquito pre-spraying efforts should also be undertaken in summer months at predicted mosquito hotspots regardless of whether WNV is present.

**4) Anti-mosquito education efforts**
The city of Chicago should also allocate resources to help educate its residents on how to prevent mosquito breeding in their households. These may include TV/Radio commercials, public transportation billboards and school exhibitions.
