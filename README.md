# Diabetes Prediction

## _Predicting Rental Prices in NYC - Evaluating Price Factors._

<a href="https://www.linkedin.com/in/mohit-matta-61b65b18"> Author: Mohit Matta </a>

<a href="https://mohitmatta.github.io/">Click here to go back to Portfolio Website </a>

![A remote image](https://mohitmatta.github.io/assets/img/work-analytics.jpg)

Abstract: 

Diabetes, often described as a “Disease of Civilization”, is a major public health problem that is approaching epidemic proportions globally. Undiagnosed diabetes can be predisposing factor to a fatal cardiac stroke. Its exponentially increasing cases has become a matter of concern world wide. Usually onset of type 2 diabetes happens in middle age and sometimes in old age. But nowadays incidences of this disease are reported in children as well. Risk factors leading to diabetes range from genetic susceptibility and body weight to food habits and lifestyle. Adult with diabetes have a two-to-three fold increased risk of heart attacks, neuropathy, foot ulcers, limb amputation and kidney failure. Early diagnosis is crucial and can be accomplished through relatively inexpensive testing of blood sugar. Diabetes can be controlled by promoting healthy diet and regular exercise, thereby reducing the growing global problem of overweight people and obesity.
Classification is one of the most important decision making techniques in many real world problem. In this work, the main objective is to classify the data as diabetic or non-diabetic and improve the classification accuracy. The main objective of our model is to achieve high accuracy.Classification accuracy can be increased if we use much of the data set for training and few data sets for testing.The aim of this project is to develop a system which can predict the diabetic risk level of a patient with a higher accuracy.

### Project Specific Questions
- What are the physical factors that are highly correlated?
- What are the physical factor directly leading to diabetes?
- Is diabetes gender neutral?
- Does agegroup play a role in diabetes?
- Do women with 2 pregnancies or more have a higher chance of diabetes than women with one or no pregnancy?
- what is the optimum value of k for kNN model that gives highest accuracy?
- Can Diabetes be predicted in an early stage using above analysis?
	

### Methods used in my project

1.	Obtain relevant data that I would review as both an apartment lease and a landlord. These include apartment data, highly rated and reviewed Yelp reviewed business locations, zip codes for each NYC borough area, top employers with high revenue and size in number of employees and NYC attraction locations.

2.	Generate new features as distances from each apartment to each location.

3.	Analyze the distribution of my values. Review how my variables relate to each other to understand which affect each other.

4.	Synthesize new features that allow for a sense of contributing factors toward price fluctuation using my other obtained variables.

5.	Revisit reviews of how my features correlate.

6.	Train my model using sklearn’s ensemble RandomForestRegressor algorithm to generate my model and test it multiple times using sklearn KFold while measuring accuracy and loss at each iteration.

7.	Perform hyperparameter tuning reviews using RandomizedSearchCV to identify best weights to use. Then retrain and re-evaluate.

8.	Generate visualizations of the decision tree for explain-ability.

9.	Export and review the important features from my model.

10.	Perform final test with predictions.

### Project Dataset:
- Type:		CSV
- Columns: 	184
- Rows:		33,986

## Included Project Variables / Factors 

 | Feature / Factors | Definition | 
 | --------- | --------- | 
 | bathrooms | RentHop - Number of bathrooms | 
 |  bedrooms | RentHop - Number of bedrooms | 
 |  latitude | RentHop - Latitude | 
 |  longitude | RentHop - Longitude | 
 |  elevator | RentHop - Elevator available 1 yes, 0 no | 
 |  cats_allowed | RentHop - Cats allowed 1 yes, 0 no | 
 |  hardwood_floors | RentHop - Hardwood floors 1 yes, 0 no | 
 |  dogs_allowed | RentHop - Cats allowed 1 yes 0 no | 
 |  doorman | RentHop - Doorman available 1 yes, 0 no | 
 |  dishwasher | RentHop - Dishwasher available 1 yes, 0 no | 
 |  no_fee | RentHop - No down payment available 1 yes, 0 no | 
 |  laundry_in_building | RentHop - Laundry in premise available 1 yes, 0 no | 
 |  fitness_center | RentHop - Fitness center on premise available 1 yes, 0 no | 
 |  laundry_in_unit | RentHop - Laundry in apartment available 1 yes, 0 no | 
 |  roof_deck | RentHop - Roof deck available 1 yes, 0 no | 
 |  outdoor_space | RentHop - Private outdoor space available 1 yes, 0 no | 
 |  dining_room | RentHop - Dining room available 1 yes, 0 no | 
 |  high_speed_internet | RentHop - High Speed Internet available 1 yes, 0 no | 
 |  balcony | RentHop - Balcony available 1 yes, 0 no | 
 |  swimming_pool | RentHop - Swimming pool available 1 yes, 0 no | 
 |  new_construction | RentHop - Is it new construction 1 year 1 yes, 0 no | 
 |  terrace | RentHop - Terrace available 1 yes, 0 no | 
 |  exclusive | RentHop - Exclusive Offer available 1 yes, 0 no | 
 |  loft | RentHop - Loft apartment 1 yes, 0 no | 
 |  garden_patio | RentHop - Garden Patio available 1 yes, 0 no | 
 |  wheelchair_access | RentHop - Wheel chair access available 1 yes, 0 no | 
 |  common_outdoor_space | RentHop - Common outdoor space available 1 yes, 0 no | 
 |  interest_level_val | RentHop - Renthop Apartment Level of Interest | 
 | geohash | Imputed Geohash based on Latitude and Longitude | 
 |  borough_id | Imputed identifier for the borough id | 
 |  borough_val | Imputed identifier for the area within the borough | 



### Distance to Highly Rated and Priced Businesses recorded by Yelp
| Yelp Rating | Latitudes | Longitudes | 
| ------ | ------ | ------ | 
 | <a href="https://maps.google.com/?q=40.71360594,-74.00834961">Yelp_Highest_Priced_1 -Cluster Center</a> | 40.71360594 | -74.00834961 |  
 | <a href="https://maps.google.com/?q=40.76068284,-73.97826484">Yelp_Highest_Priced_2 -Cluster Center</a> | 40.76068284 | -73.97826484 | 
 | <a href="https://maps.google.com/?q=40.73287131,-73.99541715">Yelp_Highest_Priced_3 -Cluster Center</a> | 40.73287131 | -73.99541715 | 
 | <a href="https://maps.google.com/?q=40.71570017,-74.00162143">Yelp_Highest_Rated_1 -Cluster Center</a> | 40.71570017 | -74.00162143 | 
 | <a href="https://maps.google.com/?q=40.80175434,-73.94419938">Yelp_Highest_Rated_2 -Cluster Center</a> | 40.80175434 | -73.94419938 | 
 | <a href="https://maps.google.com/?q=40.76213922,-73.98069774">Yelp_Highest_Rated_3 -Cluster Center</a> | 40.76213922 | -73.98069774 | 

## Additional combined dataset variables

### Apartment Description 
- Length of the apartment description

## Additional combined dataset variables

### Apartment Amenities
- bathrooms
- bedrooms
- latitude
- longitude
- price
- interest_level
- elevator
- cats_allowed
- hardwood_floors
- dogs_allowed
- doorman
- dishwasher
- no_fee
- laundry_in_building
- fitness_center
- laundry_in_unit
- roof_deck
- outdoor_space
- dining_room
- high_speed_internet
- balcony
- swimming_pool
- new_construction
- terrace
- exclusive
- loft
- garden_patio
- wheelchair_access
- common_outdoor_space


## Pythonic Libraries Used in this project
Package               Version
--------------------- ---------
- async-generator       1.10
- asyncio               3.4.3
- certifi               2020.12.5
- dask                  2021.3.1
- decorator             4.4.2
- defusedxml            0.7.1
- folium                0.12.1
- geojson               2.5.0
- geopy                 2.1.0
- gmaps                 0.9.0
- gmplot                1.4.1
- greenlet              1.0.0
- htmlmin               0.1.12
- html-parser           0.2
- ImageHash             4.2.0
- imgkit                1.1.0
- importlib-metadata    2.1.1
- joblib                1.0.1
- jsonschema            3.2.0
- MarkupSafe            1.1.1
- matplotlib            3.3.4
- mplleaflet            0.0.5
- networkx              2.5
- notebook              6.3.0
- numpy                 1.20.1
- packaging             20.9
- pandas                1.2.3
- pandas-profiling      2.11.0
- pandasql              0.7.3
- piianalyzer           0.1.0
- pygeohash             1.2.0
- pydot                 1.4.2
- pyodbc                4.0.30
- PyYAML                5.4.1
- requests              2.25.1
- scikit-learn          0.24.1
- scipy                 1.6.1
- seaborn               0.11.1
- Shapely               1.7.1
- simplejson            3.17.2
- sklearn               0.0
- SQLAlchemy            1.4.2
- threadpoolctl         2.1.0
- typing-extensions     3.7.4.3
- urllib3               1.26.4
- websockets            8.1

## Repo Folder Structure

└───Datasets

└───Scripts

└───Results

## Python Files 

| File Name  | Description |
| ------ | ------ |
| JsonYelpDatay.py | Yelp Data Extraction |
| LoopJson.py | Json Data Conversion to Central CSV |
| LoopJsonFiles.py | Loop through JSON files, transform and create consolidated CSV | 
| Pandas_Profiling_Generate_EDA_Reports.py | Quick Descriptive Statistics | 
| RentHop_EDA_Reviews.py | Preliminary Data Wrangling and EDA review | 
| TopNYCEmployerMap.py | Map Top NYC Employers | 
| DistancesToTopNYCEmployers.py | Updates Renthop Apartments with geohashes of the Latitudes and Longitudes | 
| CalculateDistancesToTopNYCEmployers.py | Updates Distances from the Renthop Apartments to the top employers | 
| ClusterNYCYelpRatedBusinesses.py | Creates clusters and gets the centers for these kmeans clusters. Using Yelp Highest Ratings and Yelp Most Expensive Restaurants | 
| NYC_RentHop_ApartmentLocations_Map | Create Map of the locations of the apartments in my master dataset |
| GetZipCode.py | Created to get zipcodes from lat and long so to remove non NYC apartments from the NYC RentHop dataset using a list of valid Zip Codes |
| GetZipCodeLow.py | Created to get zipcodes from lat and long so to remove non NYC apartments from the NYC RentHop dataset using a list of valid Zip Codes / partitioned by interest level due to larger base recordset causing session timeout with Nominatim |
| GetZipCodeMedium.py | Created to get zipcodes from lat and long so to remove non NYC apartments from the NYC RentHop dataset using a list of valid Zip Codes / partitioned by interest level due to larger base recordset causing session timeout with Nominatim |
| GetZipCodeHigh.py | Created to get zipcodes from lat and long so to remove non NYC apartments from the NYC RentHop dataset using a list of valid Zip Codes / partitioned by interest level due to larger base recordset causing session timeout with Nominatim |
| Combine_RentHop_InterestFiles.py | Combines the resulting csv files from GetZipCodeHigh/Medium/Low.py files |
| NYCAttractionsMap.py | Creates Maps of the NYC Attractions | 
| CalculateDistancesToNYCAttractions.py | Generates the geohash for these attractions using the Latitudes and Longitudes | 
| RemoveNonNYCRecords.py | Removes Non NYC apartments from master analytics dataset |
| BoroughZips.py | Updates the Borough along with Borough Area Name using ZipCode. Adds numeric code for each. | 
| FinalDataWranglingEDA.py | Final Data Wrangling, strips html, punctuation and cleans up non NYC Zipcode related apartments. | 
| VariableCorrelationReview.py | Variable Correlation Analysis using the master analytics dataset | 
| RandomForest.py | Model review and testing. Features Analysis and parameter tuning. | 
| HyperparameterTuning.py | Model review and testing. Features Analysis and parameter tuning. | 
| DecisionTree.py | Visualize the Decision Tree for explainability. | 
| FeatureImportance.py | Feature Reviews. | 
| Prediction.py | Prediction Reviews. | 

## Datasets
| File  | Description |
| ------ | ------ |
| NYCEmployers.csv | NYC Top Employers - https://fortune.com/best-workplaces-new-york/2020/search/ | 
| yelp_business_data.csv | NYC Yelp Businesses  | 
| renthopNYC.csv | Renthop DataSet |  
| FinalLeadAnalyticsRecord.csv | Final Analytics Data Set |  
| NYCAttractions.csv | NYC Attractions |  

## Results
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Top_15_Rental_Prediction_Features.png?raw=true)
The above displays the top 15 features / factors contributing to rental price predictions.
It indicates the following features / factors are important: location, amenities, the length of the apartment description, proximity to attractions and employers.

![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Decision_Tree.png?raw=true)
Above is the decision tree generated by model. In the future, I plan to find a way to make this easier to view.

### Prediction
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/PredictionValuesExample.png?raw=true)
After feeding in the values for latitude, longitude and amenity information, my prediction code imputes the rest of the distance variables and makes pricing prediction.
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/PredictionValuesExampleResults.png?raw=true)
However, since my Renthop apartment inventory data is from 2017, my predicted prices are what can be expected from 4 years ago. Given that the rental market usually raises apartment prices by $90-$150 each year, I believe my prediction power is working correctly. The current rental price for the apartment in my example is 3482. Which is a difference of $530. Thus, supporting an increase of $132 in lease rents.

### Accuracy and MAE
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Accuracy_MAE_Results.png?raw=true)
Model Accuracy and MAE results are looking pretty interesting!
To measure the accuracy and loss of my model, I am using a set of my predicted values minus the actual target values between my train and test data. Then taking the mean of the absolute value of each in the set of values to divide this number by my target test values and then multiply by 100 to generate a mean absolute percentage error.  I then subtract 100 minus the mean absolute percentage error to produce accuracy metrics.




## Maps .. Location .. Location  .. Location

### Location of Top NYC Employers - https://fortune.com/best-workplaces-new-york/2020/search
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_Top_Employers_Heatmap.png?raw=true)
Heatmap Location for Top Employers In NYC <a href="https://adanque.github.io/ProjectResults/PredictionApartmentRentalPrices/NYC_Top_Employers_Heatmap.html">Click Here for an interactive map</a>

### Locations of RentHop's Inventoried Apartments
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_ApartmentLocations_Map.png?raw=true)
Apartment locations contained in my NYC RentHop dataset. Note: the outliers outside of NYC - these will be removed from my final cleaned dataset.<a href="https://adanque.github.io/ProjectResults/PredictionApartmentRentalPrices/NYC_RentHop_ApartmentLocations_Map.html">Click Here for an interactive map</a>
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_ApartmentLocations_Heatmap.png?raw=true)
Above is a heatmap of the apartments located in NYC. This map helps to identify the focused areas of apartments.

### Location of NYC Attractions
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_Attractions.png?raw=true)
NYC Attraction locations.
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_Attractions_Heatmap.png?raw=true)
Above is a heatmap of the attractions located in NYC

### Location of Yelp's Top Pricing and Highest Rating
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_Highest_Priced_Yelp_Businesses_KMeans_Cluster.png?raw=true)
Plot of the KMeans clusters of Yelp Rated High Priced Businesses

![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_Top_Rated_Yelp_Businesses_KMeans_Cluster_Centers.png?raw=true)
Map of the centers of each of the KMeans clusters of Yelp Rated High Priced Businesses<a href="https://adanque.github.io/ProjectResults/PredictionApartmentRentalPrices/NYC_Highest_Rated_Yelp_Businesses_KMeans_Cluster_Centers.html">Click Here for an interactive map</a>

![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_Highest_Priced_Yelp_Businesses_KMeans_Cluster_Centers.png?raw=true)
Plot of the KMeans clusters of the Highest Yelp Priced Businesses. <a href="https://adanque.github.io/ProjectResults/PredictionApartmentRentalPrices/NYC_Highest_Priced_Yelp_Businesses_KMeans_Cluster_Centers.html">Click Here for an interactive map</a>

![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_Highest_Rated_Yelp_Businesses_KMeans_Cluster.png?raw=true)
Plot of the KMeans clusters of the Highest Yelp Rated Businesses 

![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_Map_Highest_Priced_Yelp_Businesses_KMeans_Cluster_Centers.png?raw=true)
Map of the centers of each of the KMeans clusters of the Yelp Rated Highest Priced Businesses <a href="https://adanque.github.io/ProjectResults/PredictionApartmentRentalPrices/NYC_Top_Cluster_Centers.html">Click Here for an interactive map</a>

![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_Map_Highest_Rated_Yelp_Businesses_KMeans_Cluster_Centers.png?raw=true)
Map of the centers of each of the KMeans clusters of the Highest Yelp Rated Businesses 

## Apartment Amenities Review
### Interest Levels
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_Interest_Level_Pie.png?raw=true)
RentHop Apartment Review Level Breakdown. This chart shares the story of the higher inventory of lesser desired apartments over the more desired.

![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_Interest_Level_Review.png?raw=true)
RentHop Apartment Review Level Distribution. This chart displays the inventory of by bedroom counts and their related interest level. It shows that the low interest group has the most apartments in each category of bedroom count.

### Bedrooms
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_Bedrooms_Breakdown_by_Interest.png?raw=true)
RentHop Apartment Bedroom Distribution Breakdown

![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_Bedrooms_Breakdown_by_Interest_Frequency.png?raw=true)
RentHop Apartment Bedroom Distribution Frequency

![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_Bedrooms_Occurences_Histogram.png?raw=true)
RentHop Apartment Bedroom Distribution by Interest Level

### Bathrooms
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_Bathrooms_Occurences_Histogram.png?raw=true)
RentHop Apartment Bathroom Distribution 

![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_Bathrooms_Occurences_Violin_Chart.png?raw=true)
RentHop Apartment Violin plot of bathroom by Interest Level

### Pricing Reviews
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_Price_Outlier_Detection_Review.png?raw=true)
Pricing Outlier Detection
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/NYC_RentHop_Price_w90_pct_Max_Price_Excluded.png?raw=true)
Apartment Pricing Distribution

### Variable Correlation Reviews
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Variable_Relationship_Review_1.png?raw=true)
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Variable_Relationship_Review_2.png?raw=true)
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Variable_Relationship_Review_3.png?raw=true)
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Variable_Relationship_Review_4.png?raw=true)
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Variable_Relationship_Review_5.png?raw=true)
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Variable_Relationship_Review_6.png?raw=true)
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Variable_Relationship_Review_7.png?raw=true)
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Variable_Relationship_Review_8.png?raw=true)
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Variable_Relationship_Review_9.png?raw=true)
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Final_Variable_Relationship_Review.png?raw=true)
After analyzing the 184 variables, I was able to synthesize a set of variables that has created a nice relationship with my price variable that is returning a predictive accuracy between 83-87%. 
However, I believe I can synthesize more features / factors to reduce my Mean Absolute Error as it is currently between 563-1346.

## Data Sources
| Source  | Description | URL |
| ------ | ------ | ------ |
| RentHop | NYC Apartments Inventory | https://www.kaggle.com/c/two-sigma-connect-rental-listing-inquiries/data | 
| Yelp | Collection of NYC Business Ratings and Prices | https://www.yelp.com/dataset | 
| Fortune | NYC List of top 40 Employers | https://fortune.com/best-workplaces-new-york/2020/search/ | 
| Pluto | NYC Borough Location Area Information | https://www1.nyc.gov/ | 
| Mygeodata | NYC Location of Attractions | https://mygeodata.cloud/ | 
| Zip Codes | NYC Zip Codes | https://worldpostalcode.com/united-states/new-york/new-york-city | 
| Boroughs Area Names | Borough by Zip Code | https://www.nycbynatives.com/nyc_info/new_york_city_zip_codes.php & https://storage.googleapis.com/plos-corpus-prod/10.1371/journal.pone.0194799/1/pone.0194799.s001.pdf?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=wombat-sa%40plos-prod.iam.gserviceaccount.com%2F20210328%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20210328T203603Z&X-Goog-Expires=3600&X-Goog-SignedHeaders=host&X-Goog-Signature=91b1ec1a775a9e750bc63a5cd5d7bc1e36ebba6f7271f16239ef3bf4fb44a025c106d9737e6bc6b88a4e1402ece330e70790ec33e25622be67c35e409e637a4b763cb2461a5b037bf23bc3ab415791fd625225cffbeac605de27991074666cf5a8acb1a0b428e2e7f71d383dfdfc3aaabada40e2aadd923a3ae48fc4da6e4e42fec97bc62ac32a84e05b9cfb9f269c10e600859b0f0a6ce5ac4cf04c7eef0e57d47ba99eac61b04a70ccdeff079a33ee0156343794d022edad687477934124d775295d416026a1bd31d0fd44da85820a2758b6034cd284f1bbbcc6e565918cb2cbbf35441ba1d0221691732c2047bb7d11d53f0ac5309ea2616c5adab80dff96 |

## References: 

Kopp, C. (November 2019). How Expensive is it to Live in New York City? Retrieved from: https://www.investopedia.com/articles/personal-finance/012315/how-expensive-new-york-city-really.asp

Riley, E. (July 2019). Cost of Living in Chicago vs. NYC: Which Big City Is Cheaper? Retrieved from: https://streeteasy.com/blog/cost-of-living-in-chicago-vs-nyc/#:~:text=Median%20rent%20for%20a%201,That's%20nothing%20to%20scoff%20at.

TIMOTHY102, (October 2020). Predicting NYC AirBnB Rental Prices with TensorFlow. Retrieved from  https://www.analyticsvidhya.com/blog/2020/10/predicting-nyc-airbnb-rental-prices-tensorflow/

Carmody, B. (February 2021). Best Rental Listing Sites. Retrieved from  https://www.investopedia.com/best-rental-listing-sites-5075293

RentCafe. (n.d.). RentCafe is a listing site that can be used for comparable pricing with my predicted values. Retrieved from https://www.rentcafe.com/

Mastroeni, T. (October 2020). How is Artificial Intelligence Used in Real Estate? Retrieved from https://www.fool.com/millionacres/real-estate-market/real-estate-innovation/how-is-artificial-intelligence-used-in-real-estate/

Barzilay, O. (March 2017). Property Management May Be The Next Frontier For AI. Retrieved from https://www.forbes.com/sites/omribarzilay/2017/03/14/property-management-may-be-the-next-frontier-for-ai/?sh=3ba8d5f66fb3

McLaughlin, K. (November 2019). Robots Are Taking Over (the Rental Screening Process). Retrieved from https://www.wsj.com/articles/robots-are-taking-over-the-rental-screening-process-11574332200

Devanesan, J. (October 2019). What happens when AI enters the rental market? Retrieved from https://techhq.com/2019/10/what-happens-when-ai-enters-the-rental-market/

Antony, V. (May 2020) Predicting Apartment Rental Prices in Germany. Retrieved from https://towardsdatascience.com/predicting-apartment-rental-prices-in-germany-d5635197ab00

Villar, B. (April 2020). Machine Learning and RealState: Predicting Rental Prices in Amsterdam. Retrieved from https://towardsdatascience.com/ai-and-real-state-renting-in-amsterdam-part-1-5fce18238dbc

Najera, C. Hunter, T. Zhan, D. Bialer, J. (March 2017). Predicting Interest for NYC Apartment Rental Listings - A Guideline For Landlors and Agents. Retrieved from https://nycdatascience.com/blog/student-works/predicting-interest-nyc-apartments-rent-guideline-landlords/



:bowtie:
