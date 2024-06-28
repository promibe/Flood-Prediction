# Flood-Prediction
Predicting The probability of a particular location having flood

## Understanding the Problem
* <b>Overview</b> <br>
    Welcome to the 2024 Kaggle Playground Series! We plan to continue in the spirit of previous playgrounds, providing interesting an approachable datasets for our community to practice their machine learning skills, and anticipate a competition each month.

* <b>Your Goal:</b> <br>
The goal of this competition is to predict the probability of a region flooding based on various factors.

### Dataset
* The given dataset for flood prediction problem is divided into
  - <b>train set:</b> This is the dataset that will be used for building the model
  - <b>test set:</b> this is the test dataset that will be used for the final prediction after the model has been built
  - <b>sample submission set</b> This is an example of how the submission will look like 

## Understanding the Dataset
* MonsoonIntensity: This feature refers to the strength or vigor of the monsoon season, which is characterized by heavy rainfall and often associated with a shift in wind patterns.
<br>

* TopographyDrainage: This feature refers to the topography of the area as regards to its drainage system, which affect the flow of water
<br>

* RiverManagement:This feature refers to the effective river management system in the area, such as dam construction and waterways 
<br>

* Deforestation: This feature refers to the measure or rate of deforestation, it can disrupt water cycles, leading to changes in precipitation, runoff, and soil erosion, which can impact water quality and availability hence cause the region to be prone to flood
<br>

* Urbanization: This feature refers to the degree of urbanization of the region. Well developed regions often leads to improved runoff and reduced flood because of the presence of impervious surfaces like pavements and building.
<br>

* ClimateChange: This feature represent the influence Climate change has on flood risk. Climatic change has significant implications for flood risk, as it can alter precipitation patterns, increase the frequency and intensity of extreme weather events, and contribute to sea-level rise. 
<br>

* DamsQuality: The features represents the quality of dams which plays a significant role in managing flood risk. Dams are important infrastructure for water storage, flood control, hydropower generation, and water supply. However, the effectiveness of dams in reducing flood risk depends on various factors related to their design, construction, operation, and maintenance:
<br>

* Siltation: This features also known as sedimentation, refers to the accumulation of sediment, such as sand, silt, and clay, in rivers, reservoirs, and other water bodies over time. Siltation can have significant implications for flood risk, Excessive siltation can reduce water storage capacity and increase flood risk. 
<br>

* AgriculturalPractices: This features represent the Agricultural practices in a region which can have significant implications for flood risk, both in terms of exacerbating or mitigating flooding, Clearing forests or natural vegetation for agricultural expansion increases the risk of flooding, and other agricultural practices
<br>

* Encroachments: This feature likely indicates the extent of encroachment or unauthorized occupation of floodplains and other natural waterways, which can exacerbate flood impacts.
<br>

* Disaster Preparedness: This feature could represent the level of preparedness and response capabilities of local authorities and communities in dealing with flood disasters.
<br>

* Drainage Systems: This feature may describe the condition and effectiveness of drainage infrastructure, including stormwater drains, culverts, and canals.
<br>

* Coastal Vulnerability: This feature likely assesses the susceptibility of coastal areas to flooding and storm surges, considering factors such as sea level rise, coastal erosion, and tidal patterns.
<br>

* Landslides: This feature may indicate the risk of landslides in the region, which can be triggered by heavy rainfall and contribute to downstream flooding.
<br>

* Watersheds: Watersheds are areas of land where all the water drains into a common outlet, such as a river or lake. This feature may represent the characteristics of watersheds in the region and their influence on flooding.
<br>

* Deteriorating Infrastructure: This feature likely describes the condition of critical infrastructure systems (e.g., roads, bridges, levees) that play a role in flood mitigation and response.
<br>

* Population Score: This feature may indicate population density or other demographic factors that can influence flood vulnerability and the potential impact on human lives and property.
<br>

* Wetland Loss: This feature likely measures the extent of wetland loss in the region, which can reduce natural flood storage capacity and increase flood risk.
<br>

* Inadequate Planning: This feature could represent deficiencies in land use planning, zoning regulations, and development policies that contribute to increased flood vulnerability.
<br>

* Political Factors: This feature may encompass political considerations and governance issues that affect flood risk management, such as corruption, regulatory enforcement, and allocation of resources.
<br>

* Flood Probability: This is likely the target variable you're trying to predict, representing the likelihood or probability of flooding occurring in a given area based on the combination of all the aforementioned factors.

## Data Exploration
The dataset was explored, the following inference was derived
* We have a total number of 22 featuers including the ID column
* The minimum value for the features are zero excluding the id column
* The maximum value for all the features lies betweeh 16 and 19
* All the features are Numeric features
* Non of the features has Null values out of the total number of 1,117,957 enteries 
* The target variable is between <b>0.285</b> and <b>0.725</b>
* we could also understand that an average of 50.935233 has FloodProbability value of 0.5, a total of 569434
* From statistical probability, we understood that the probability value from <b>0</b> t0 <b>0.49</b> is lesser than that of <b>0.5</b> t0 <b>1</b>

## Data Cleaning
* Pandas, numpy were used
The data was inspected and it was clean, no duplicates, no NaN values and the datatypes are okay

## Data Visualization
* matplotlib.pyplot and seaborn was used
The following chart were used to understand the distribution of the dataset:
* countplot
* histogram
* Distribution plot
* Boxplot - used to determined if there are outliers
* Density plot
* HeatMap - use to check the correlation between the various features

## Data Preprocessing 
The dataset was scaled, with the following Salars:
* MinMaxScaler
* Normalizer
* StandardScaler
* RoburstScaler

## Modelling 
The dataset was splitted into train and test set.
The following Machine Learning algorithms were used to predict the Probability of flood
Note: The Problem is a Regression problem, so a regression algorithm was used:
* Linear Regression Model
* Logistic Regression
* Decision Tree Regressor
* Support Vector Regressor
* Gradient Boosting Regressor
* Cat Boost Regressor
* Xg Boost Regressor

## Feature Engineering 
More features were created to improve the performance of the model

# Result 
* It was observed after various experiment, that the CatBoostRegressor model has the highest accuracy value of <b>0.8657 R2 Score value</b>
