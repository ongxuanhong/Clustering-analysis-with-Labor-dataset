# Introduction
Through experiment clustering, we can self-evaluate as a good or bad employee. Based on information from labor dataset, i used partition (Kmean) and hierarchical (AGNES) methods for analyzing an input employee.

Blog: https://ongxuanhong.wordpress.com/2015/08/27/gom-nhom-clustering-analysis-tap-du-lieu-labor/

# Download links
* Link: https://archive.ics.uci.edu/ml/machine-learning-databases/labor-negotiations/labor-negotiations.data
* Description: https://archive.ics.uci.edu/ml/machine-learning-databases/labor-negotiations/labor-negotiations.names

# Exploratory analysis

![Exploratory analysis](https://ongxuanhong.files.wordpress.com/2015/08/load-labor-dataset.png)

* Number of instances: 57
* Number of attributes: 17

|Name|Type|Missing value|
|---|---|---|
|duration|numeric|1 (2%)|
|wage increase in first year|numeric|1 (2%)|
|wage increase in second year|numeric|11 (19%)|
|wage increase in third year|numeric|42 (74%)|
|cost of living allowance|nomial|20 (35%)|
|working hours|numeric|6 (11%)|
|pension|nomial|30 (53%)|
|standby pay|numeric|48 (84%)|
|shift differencial|numeric|26 (46%)|
|education allowance|nomial|35 (61%)|
|statutory holidays|numeric|4 (7%)|
|vacation|nomial|6 (11%)|
|longterm disabil|nomial|29 (51%)|
|contribution towards the dental plan|nomial|20 (35%)|
|bereavement|nomial|27 (47%)|
|contribution towards the health plan|nomial|20 (35%)|

# Algorithm run with missing and replaced missing value
* Number of group: 2
* Evaluating with Classes To Clusters method
* Using Euclide distance
* A: has missing value, B: replaced missing value

|Algorithm|Incorrectly clustered instances (A)|Incorrectly clustered instances (B)|
|---|---|---|
|SimpleKMeans|13.0 (22.807%)|13.0 (22.807%)|
|AGNES với Single Link|20.0 (35.0877%)|19.0 (33.333%)|
|AGNES với Complete Link|21.0 (36.8421%)|17.0 (29.824%)|
|AGNES với Adjusted Complete Link|21.0 (36.8421%)|19.0 (33.333%)|
|AGNES với Average Link|20.0 (35.0877 %)|15.0 (26.315%)|
|AGNES với Mean Link|15.0 (26.3158%)|16.0 (28.070%)|
|AGNES với Centroid Link|25.0 (43.8596%)|19.0 (33.333%)|
