# SC1015 Mini Project
![Marketing Proposal Business Presentation in Yellow Orange 3D Style](https://github.com/aryaman-agarwal/SC1015-Mini-Project/assets/109872386/0cc6846f-6588-4168-b2ca-729e9f4a32c3)
SC1015: Data Science and Artfifcal Intelligence\
Mini Project: Singapore HDB Resale Price Prediction\
Lab: FCSA\
Group : 2\

Members:

1. Agarwal Aryaman ([@aryaman-agarwal](https://github.com/aryaman-agarwal))
2. Batra Sia ([@siabatra](https://github.com/siabatra))
3. Agarwala Grisha ([@grishaag18](https://github.com/grishaag18))

### Project Overview
This project aims to predict HDB flat resale prices in Singapore. It leverages machine learning to enhance transparency and efficiency in the public housing marketplace.

### Problem Statement
The primary challenge is to provide a predictive model for HDB flat resale prices, empowering both buyers and sellers with better decision-making tools.

### Dataset Description
The dataset covers HDB resale data from 2012 to 2021, including 78 features for each unit, sourced from the Singapore Public Housing Dataset on Kaggle.

### Data Preparation and Preprocessing
- **Standardization:** Conversion of all column names to lowercase, formatted to snake case.
- **Cleaning:** Removal of non-essential columns and application of `SimpleImputer` for missing data.
- **Feature Engineering:** Addition of new fields like `mall_nearest_distance` for enhanced spatial analysis.

### Exploratory Data Analysis
- **Price Trends:** Analysis shows a concentration of transactions within the SGD 200,000 to SGD 400,000 range.
- **Geospatial Analysis:** Heatmaps highlight areas with higher resale prices.
- **Correlation Matrix:** Strong positive correlation between `floor_area_sqm` and `resale_price`.

### Machine Learning Models
1. **Linear Regression**
   - Trained with scikit-learn’s LinearRegression; R² score of 0.988 on training data.
2. **Decision Trees**
   - Configured with a depth of 5; R² score shows strong fit to data.
3. **Random Forest**
   - Utilizes 100 trees with optimized hyperparameters; robust against overfitting.
4. **XGBoost**
   - Employs DMatrix for faster computation; finely tuned for optimal performance.

### Model Evaluation
- **Performance:** XGBoost achieved the highest R² score of 0.999, indicating excellent predictive accuracy.
- **Comparison:** All models were compared, showcasing XGBoost as the superior choice for this dataset.

### Conclusion
The models developed offer a robust framework for predicting HDB resale prices, providing valuable insights for market participants and policymakers.


---

### Data Dictionary:

<br>This dataset contains data of resale flats that have been sold from 2012 to 2021. 

| **Column names** | **Descriptions** |
|---|---|
| resale_price | the property's sale price in Singapore dollars. This is the target variable that you're trying to predict for this challenge. |
| Tranc_YearMonth | year and month of the resale transaction e.g. 2015-02 |
| town | HDB township where the flat is located e.g. BUKIT MERAH |
| flat_type | type of the resale flat unit e.g. 3 ROOM |
| block | block number of the resale flat e.g. 454 |
| street_name | street name where the resale flat resides e.g. TAMPINES ST 42 |
| storey_range | floor level (range) of the resale flat unit e.g. 07 TO 09 |
| floor_area_sqm | floor area of the resale flat unit in square metres |
| price_per_sqft | Price per Square Foot of the unit |
| flat_model | HDB model of the resale flat e.g. Multi Generation |
| lease_commence_date | commencement year of the flat units 99-year lease |
| Tranc_Year | year of resale transaction |
| Tranc_Month | month of resale transaction |
| mid_storey | median value of storey_range |
| lower | lower value of storey_range |
| 2room_rental | 2 room rental flat |
| 3room_rental | 3 room rental flat |
| 4room_rental | 4 room rental flat |
| postal | postal code |
| other_room_rental | other room rental flat |
| upper | upper value of storey_range |
| mid | middle value of storey_range |
| full_flat_type | combination of flat_type and flat_model |
| address | combination of block and street_name |
| floor_area_sqft | floor area of the resale flat unit in square feet |
| hdb_age | number of years from lease_commence_date to present year |
| max_floor_lvl | highest floor of the resale flat |
| year_completed | year which construction was completed for resale flat |
| residential | boolean value if resale flat has residential units in the same block |
| commercial | boolean value if resale flat has commercial units in the same block |
| market_hawker | boolean value if resale flat has a market or hawker centre in the same block |
| multistorey_carpark | boolean value if resale flat has a multistorey carpark in the same block |
| precinct_pavilion | boolean value if resale flat has a pavilion in the same block |
| total_dwelling_units | total number of residential dwelling units in the resale flat |
| Latitude | Latitude of the unit |
| Longitude | Longitude of the unit |
| planning_area | planning area of the unit |
| pri_sch_nearest_distance | distance of unit to the nearest primary school |
| 1room_sold | number of 1-room residential units in the resale flat |
| 2room_sold | number of 2-room residential units in the resale flat |
| 3room_sold | number of 3-room residential units in the resale flat |
| 4room_sold | number of 4-room residential units in the resale flat |
| 5room_sold | number of 5-room residential units in the resale flat |
| exec_sold | number of executive type residential units in the resale flat block |
| pri_sch_name | name of the nearest primary school |
| vacancy | vacancy of the unit |
| pri_sch_affiliation | affiliation of primary school |
| pri_sch_latitude | latitude of primary school |
| pri_sch_longitude | longitude of primary school |
| sec_sch_nearest_dist | distance to nearest secondary school |
| sec_sch_name | name of nearest secondary school |
| cutoff_point | PSLE cutoff point of nearest secondary school |
| affiliation | if there is affiliation for the nearest secondary school |
| sec_sch_latitude | latitude of secondary school |
| sec_sch_longitude | longitude of secondary school |
| multigen_sold | number of multi-generational type residential units in the resale flat block |
| mrt_nearest_distance | distance to nearest mrt |
| mrt_name | name of nearest mrt |
| bus_interchange | if there is a bus interchange |
| mrt_interchange | if there is an mrt interchange |
| mrt_latitude | latitude of mrt |
| mrt_longitude | longitude of mrt |
| bus_stop_nearest_distance | distance to nearest bus stop |
| bus_stop_name | name of bus stop |
| bus_stop_latitude | latitude of bus stop |
| bus_stop_longitude | longitude of bus stop |
| Mall_Nearest_Distance | Distance to the nearest mall |
| Mall_Within_500m | How many malls within 500m of the unit |
| Mall_Within_1km | How many malls within 1km of the unit |
| Mall_Within_2km | How many malls within 2km of the unit |
| Hawker_Nearest_Distance | Distance to nearest Hawker Center |
| Hawker_Within_500m | How many Hawker Centers within 500m of the unit |
| Hawker_Within_1km | How many Hawker Centers within 1km of the unit |
| Hawker_Within_2km | How many Hawker Centers within 2km of the unit |
| studio_apartment_sold | number of studio apartment type residential units in the resale flat block |
| 1room_rental | number of 1-room rental residential units in the resale flat block |
| hawker_food_stalls | number of stalls at nearest hawker centre |
| hawker_market_stalls | number of market stalls at nearest hawker centre |

---
