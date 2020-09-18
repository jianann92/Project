# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Ames Housing Data - Linear Regression - README.md

### John Lim Jian Ann, DSI-17-Singapore

---

## Problem Statement

**How can you increase your real estate value in Ame, Iowa?**

## Executive Summary

I work in a real estate title company in Ame, Iowa and I help clients with their real estate closing. Clients have asked me how to get the most out of their real estate.
By using data analysis and modelling techniques, I find out what brings most value to a real estate and how to get the most out of the property you already have.

---

## Data dictionary:

|Feature|Type|Description|Values|
|---|---|---|---|
|**SalePrice**|*int*|Price of the property **(Target Value)**|USD|
|**Id**|*int*|ID of the property|integer|
|**PID**|*int*|Parcel Number for the lot|integer|
|**MS SubClass**|*object*|Dwelling Type|20 - 1-STORY 1946 & NEWER ALL STYLES<br>30 - 1-STORY 1945 & OLDER<br>40 - 1-STORY W/FINISHED ATTIC ALL AGES<br>45 - 1-1/2 STORY - UNFINISHED ALL AGES<br>50 - 1-1/2 STORY FINISHED ALL AGES<br>60 - 2-STORY 1946 & NEWER<br>70 - 2-STORY 1945 & OLDER<br>75 - 2-1/2 STORY ALL AGES<br>80 - SPLIT OR MULTI-LEVEL<br>85 - SPLIT FOYER<br>90 - DUPLEX - ALL STYLES AND AGES<br>120 - 1-STORY PUD (Planned Unit Development) - 1946 & NEWER<br>150 - 1-1/2 STORY PUD - ALL AGES<br>160 - 2-STORY PUD - 1946 & NEWER<br>180 - PUD - MULTILEVEL - INCL SPLIT LEV/FOYER<br>190 - 2 FAMILY CONVERSION - ALL STYLES AND AGES|
|**MS Zoning**|*object*|Zoning classification of the lot|A - Agriculture<br>C - Commercial<br>FV - Floating Village Residential<br>I - Industrial<br>RH - Residential High Density<br>RL - Residential Low Density<br>RP - Residential Low Density Park<br>RM - Residential Medium Density|
|**Lot Frontage**|*float*|Linear feet of street connected to property|ft|
|**Lot Area**|*int*|Lot size in square feet|sq ft|
|**Street**|*object*|Type of road access to property|Grvl - Gravel<br>Pave - Paved<br>|
|**Lot Shape**|*object*|General shape of property|Reg - Regular<br>IR1 - Slightly irregular<br>IR2 - Moderately Irregular<br>IR3 - Irregular|
|**Land Contour**|*object*|Flatness of the property|Lvl - Near Flat/Level<br>Bnk - Banked - Quick and significant rise from street grade to building<br>HLS - Hillside - Significant slope from side to side<br>Low - Depression|
|**Lot Config**|*object*|Lot configuration|Inside - Inside lot<br>Corner - Corner lot<br>CulDSac - Cul-de-sac<br>FR2 - Frontage on 2 sides of property<br>FR3 - Frontage on 3 sides of property|
|**Land Slope**|*object*|Slope of property|Gtl - Gentle slope<br>Mod - Moderate Slope<br>Sev - Severe Slope|
|**Neighborhood**|*object*|Physical locations within Ames city limits|Blmngtn - Bloomington Heights<br>Blueste - Bluestem<br>BrDale - Briardale<br>BrkSide - Brookside<br>ClearCr - Clear Creek<br>CollgCr - College Creek<br>Crawfor - Crawford<br>Edwards - Edwards<br>Gilbert - Gilbert<br>IDOTRR - Iowa DOT and Rail Road<br>MeadowV - Meadow Village<br>Mitchel - Mitchell<br>Names - North Ames<br>NoRidge - Northridge<br>NPkVill - Northpark Villa<br>NridgHt - Northridge Heights<br>NWAmes - Northwest Ames<br>OldTown - Old Town<br>SWISU - South & West of Iowa State University<br>Sawyer - Sawyer<br>SawyerW - Sawyer West<br>Somerst - Somerset<br>StoneBr - Stone Brook<br>Timber - Timberland<br>Veenker - Veenker|
|**Condition 1**|*object*|Proximity to main road or railroad|Artery - Adjacent to arterial street<br>Feedr - Adjacent to feeder street<br>Norm - Normal<br>RRNn - Within 200' of North-South Railroad<br>RRAn - Adjacent to North-South Railroad<br>PosN - Near positive off-site feature--park, greenbelt, etc.<br>PosA - Adjacent to postive off-site feature<br>RRNe - Within 200' of East-West Railroad<br>RRAe - Adjacent to East-West Railroad|
|**Condition 2**|*object*|Proximity to main road or railroad (if a second is present)|Proximity to main road or railroad|Artery - Adjacent to arterial street<br>Feedr - Adjacent to feeder street<br>Norm - Normal<br>RRNn - Within 200' of North-South Railroad<br>RRAn - Adjacent to North-South Railroad<br>PosN - Near positive off-site feature--park, greenbelt, etc.<br>PosA - Adjacent to postive off-site feature<br>RRNe - Within 200' of East-West Railroad<br>RRAe - Adjacent to East-West Railroad|
|**Bldg Type**|*object*|Type of dwelling|1Fam - Single-family Detached<br>2FmCon - Two-family Conversion; originally built as one-family dwelling<br>Duplx - Duplex<br>TwnhsE - Townhouse End Unit<br>TwnhsI - Townhouse Inside Unit|
|**House Style**|*object*|Style of dwelling|1Story - One story<br>1.5Fin - One and one-half story: 2nd level finished<br>1.5Unf - One and one-half story: 2nd level unfinished<br>2Story - Two story<br>2.5Fin - Two and one-half story: 2nd level finished<br>2.5Unf - Two and one-half story: 2nd level unfinished<br>SFoyer - Split Foyer<br>SLvl - Split Level|
|**Overall Qual**|*int*|Overall material and finish quality|1 - Very Poor <-> 10 - Very Excellent|
|**Overall Cond**|*int*|Overall condition rating|1 - Very Poor <-> 10 - Very Excellent|
|**Year Built**|*int*|Original construction date|year|
|**Year Remod/Add**|*int*|Remodel date (same as construction date if no remodeling or additions)|year|
|**Roof Style**|*object*|Type of roof|Flat - Flat<br>Gable - Gable<br>Gambrel - Gabrel (Barn)<br>Hip - Hip<br>Mansard - Mansard<br>Shed - Shed|
|**Roof Matl**|*object*|Roof material|ClyTile - Clay or Tile<br>CompShg - Standard (Composite) Shingle<br>Membran - Membrane<br>Metal - Metal<br>Roll - Roll<br>Tar&Grv - Gravel & Tar<br>WdShake - Wood Shakes<br>WdShngl - Wood Shingles|
|**Exterior 1st**|*object*|Exterior covering on house|AsbShng - Asbestos Shingles<br>AsphShn - Asphalt Shingles<br>BrkComm - Brick Common<br>BrkFace - Brick Face<br>CBlock - Cinder Block<br>CemntBd - Cement Board<br>HdBoard - Hard Board<br>ImStucc - Imitation Stucco<br>MetalSd - Metal Siding<br>Other - Other<br>Plywood - Plywood<br>PreCast - PreCast<br>Stone - Stone<br>Stucco - Stucco<br>VinylSd - Vinyl Siding<br>WdSdng - Wood Siding<br>WdShing - Wood Shingles|
|**Exterior 2nd**|*object*|Exterior covering on house (if more than one material)|AsbShng - Asbestos Shingles<br>AsphShn - Asphalt Shingles<br>BrkComm - Brick Common<br>BrkFace - Brick Face<br>CBlock - Cinder Block<br>CemntBd - Cement Board<br>HdBoard - Hard Board<br>ImStucc - Imitation Stucco<br>MetalSd - Metal Siding<br>Other - Other<br>Plywood - Plywood<br>PreCast - PreCast<br>Stone - Stone<br>Stucco - Stucco<br>VinylSd - Vinyl Siding<br>WdSdng - Wood Siding<br>WdShing - Wood Shingles|
|**Mas Vnr Type**|*object*|Masonry veneer type|BrkCmn - Brick Common<br>BrkFace - Brick Face<br>CBlock - Cinder Block<br>None - None<br>Stone - Stone|
|**Mas Vnr Area**|*float*|Masonry veneer area in square feet|sq ft|
|**Exter Qual**|*object*|Exterior material quality|Ex - Excellent<br>Gd - Good<br>TA - Average/Typical<br>Fa - Fair<br>Po - Poor|
|**Exter Cond**|*object*|Present condition of the material on the exterior|Ex - Excellent<br>Gd - Good<br>TA - Average/Typical<br>Fa - Fair<br>Po - Poor|
|**Foundation**|*object*|Type of foundation|BrkTil - Brick & Tile<br>CBlock - Cinder Block<br>PConc - Poured Contrete<br>Slab - Slab<br>Stone - Stone<br>Wood - Wood|
|**Bsmt Qual**|*object*|Height of the basement|Ex - Excellent (100+ inches)<br>Gd - Good (90-99 inches)<br>TA - Typical (80-89 inches)<br>Fa - Fair (70-79 inches)<br>Po - Poor (<70 inches)<br>NA - No Basement|
|**Bsmt Cond**|*object*|General condition of the basement|Ex - Excellent<br>Gd - Good<br>TA - Typical - slight dampness allowed<br>Fa - Fair - dampness or some cracking or settling<br>Po - Poor - Severe cracking, settling, or wetness<br>NA - No Basement|
|**Bsmt Exposure**|*object*|Walkout or garden level basement walls|Gd - Good Exposure<br>Av - Average Exposure (split levels or foyers typically score average or above)<br>Mn - Mimimum Exposure<br>No - No Exposure<br>NA - No Basement|
|**BsmtFin Type 1**|*object*|Quality of basement finished area|GLQ - Good Living Quarters<br>ALQ - Average Living Quarters<br>BLQ - Below Average Living Quarters<br>Rec - Average Rec Room<br>LwQ - Low Quality<br>Unf - Unfinshed<br>NA - No Basement|
|**BsmtFin SF 1**|*float*|Type 1 finished square feet|sq ft|
|**BsmtFin Type 2**|*object*|Quality of second finished area (if present)|GLQ - Good Living Quarters<br>ALQ - Average Living Quarters<br>BLQ - Below Average Living Quarters<br>Rec - Average Rec Room<br>LwQ - Low Quality<br>Unf - Unfinshed<br>NA - No Basement|
|**BsmtFin SF 2**|*float*|Type 2 finished square feet|sq ft|
|**Bsmt Unf SF**|*float*|Unfinished square feet of basement area|sq ft|
|**Total Bsmt SF**|*float*|Total square feet of basement area|sq ft|
|**Heating**|*object*|Type of heating|Floor - Floor Furnace<br>GasA - Gas forced warm air furnace<br>GasW - Gas hot water or steam heat<br>Grav - Gravity furnace<br>OthW - Hot water or steam heat other than gas<br>Wall - Wall furnace|
|**Heating QC**|*object*|Heating quality and condition|Ex - Excellent<br>Gd - Good<br>TA - Average/Typical<br>Fa - Fair<br>Po - Poor|
|**Central Air**|*int*|Central air conditioning|Y/N|
|**Electrical**|*object*|Electrical system|SBrkr - Standard Circuit Breakers & Romex<br>FuseA - Fuse Box over 60 AMP and all Romex wiring (Average)<br>FuseF - 60 AMP Fuse Box and mostly Romex wiring (Fair)<br>FuseP - 60 AMP Fuse Box and mostly knob & tube wiring (poor)<br>Mix - Mixed|
|**1st Flr SF**|*int*|First Floor square feet|sq ft|
|**2nd Flr SF**|*int*|Second floor square feet|sq ft|
|**Low Qual Fin SF**|*int*|Low quality finished square feet (all floors)|sq ft|
|**Gr Liv Area**|*int*|Above grade (ground) living area square feet|sq ft|
|**Bsmt_full_bath**|*float*|Basement full bathrooms|number|
|**Bsmt_Half Bath**|*float*|Basement half bathrooms|number|
|**Full Bath**|*int*|Full bathrooms above grade|integer|
|**Half Bath**|*int*|Half baths above grade|integer|
|**Bedroom AbvGr**|*int*|Number of bedrooms above basement level|integer|
|**Kitchen AbvGr**|*int*|Number of kitchens|integer|
|**Kitchen Qual**|*int*|Kitchen quality|Ex - Excellent<br>Gd - Good<br>TA - Typical/Average<br>Fa - Fair<br>Po - Poor|
|**Totrms AbvGrd**|*object*|Total rooms above grade (does not include bathrooms)|integer|
|**Functional**|*object*|Home functionality rating|Typ - Typical Functionality<br>Min1 - Minor Deductions 1<br>Min2 - Minor Deductions 2<br>Mod - Moderate Deductions<br>Maj1 - Major Deductions 1<br>Maj2 - Major Deductions 2<br>Sev - Severely Damaged<br>Sal - Salvage only|
|**Fireplaces**|*int*|Number of fireplaces|integer|
|**Garage Type**|*object*|Garage location|2Types - More than one type of garage<br>Attchd - Attached to home<br>Basment - Basement Garage<br>BuiltIn - Built-In (Garage part of house - typically has room above garage)<br>CarPort - Car Port<br>Detchd - Detached from home<br>NA - No Garage|
|**Garage Yr Blt**|*float*|Year garage was built|year|
|**Garage Finish**|*object*|Interior finish of the garage|Fin - Finished<br>RFn - Rough Finished<br>Unf - Unfinished<br>NA - No Garage|
|**Garage Cars**|*float*|Size of garage in car capacity|number|
|**Garage Area**|*float*|Size of garage in square feet|sq ft|
|**Garage Qual**|*object*|Garage quality|Ex - Excellent<br>Gd - Good<br>TA - Typical/Average<br>Fa - Fair<br>Po - Poor<br>NA - No Garage|
|**Garage Cond**|*object*|Garage condition|Ex - Excellent<br>Gd - Good<br>TA - Typical/Average<br>Fa - Fair<br>Po - Poor<br>NA - No Garage|
|**Paved Drive**|*object*|Paved driveway|Y - Paved<br>P - Partial Pavement<br>N - Dirt/Gravel|
|**Wood Deck SF**|*int*|Wood deck area in square feet|sq ft|
|**Open Porch SF**|*int*|Open porch area in square feet|sq ft|
|**Enclosed Porch**|*int*|Enclosed porch area in square feet|sq ft|
|**3Ssn Porch**|*int*|Three season porch area in square feet|sq ft|
|**Screen Porch**|*int*|Screen porch area in square feet|sq ft|
|**Pool Area**|*int*|Pool area in square feet|sq ft|
|**Misc Val**|*int*|Value of miscellaneous feature|USD|
|**Mo Sold**|*int*|Month sold|1 - January <-> 12 - December|
|**Yr Sold**|*int*|Year sold|year|
|**Sale Type**|*object*|Type of sale|WD - Warranty Deed - Conventional<br>CWD - Warranty Deed - Cash<br>VWD - Warranty Deed - VA Loan<br>New - Home just constructed and sold<br>COD - Court Officer Deed/Estate<br>Con - Contract 15% Down payment regular terms<br>ConLw - Contract Low Down payment and low interest<br>ConLI - Contract Low Interest<br>ConLD - Contract Low Down<br>Oth - Other|

---

**Exploratory Data Analysis**

Remove features with more than 40% missing values or features that does not help in our prediction:

|Feature|Type|Description|Reason for dropping|
|---|---|---|---|
|**Pool Qc**|*object*|Pool quality|>40% missing values|
|**Misc Feature**|*object*|Miscellaneous feature not covered in other categories|>40% missing values|
|**Alley**|*object*|Type of alley access to property|>40% missing values|
|**Fence**|*object*|Fence quality|>40% missing values|
|**Fireplace Qu**|*object*|Fireplace quality|>40% missing values|
|**Utilities**|*object*|Type of utilities available|Most samples belonging to one class|

Reclass features with Y/N variables
 - 1 for Y and 0 for N

**Feature Exploration**

Reg plotting with seaborn - scatter plots between variables to visualize relationships
 - Visualize the nature of correlations between variables, identify non-normal distributions across variables
 - Establish relationship between features to work on feature engineering as well as remaining nan values

**Feature Engineering**

Get dummies for Nominal data:
 - Visualized the data and determine the majority and minority classes
 - Group or drop minority classes
 - Get dummies and add it into dataframe

Get ranking for Ordinal data:
 - Visualized the data and determine the ranks
 - Rank data in ordinal manner

Different methods for remaining Nan values:
 - Visualize distribution within feature and relationship with other feature
 - Establish a reason for using a method to deal with nan values in that feature
 - Interpolation method
 - Using the mean of the feature
 - Dropping the sample with nan value

Polynomial Features to amplify the increase in SalePrice per unit change in feature :
 - Visualize the relationship between SalePrice and variables
 - Target which variable to do polynomial features

|Polynomial Feature|Type|Description|Details|
|---|---|---|---|
|**Liv Area_bsmt sf**|*float*|Gr Liv Area X Total Bsmt SF|Above grade (ground) living area square feet X Total square feet of basement area|
|**qual_neighbor**|*int*|Overall Qual X Neighborhood_rank|Rates the overall material and finish of the house X Physical locations within Ames city limits|
|**Liv Area_qual**|*int*|Gr Liv Area X Overall Qual|Above grade (ground) living area square feet X Rates the overall material and finish of the house|
|**bsmt sf_neighbor**|*float*|Total Bsmt SF X Neighborhood_rank|Total square feet of basement area X Physical locations within Ames city limits|
|**Liv Area_neighbor**|*int*|Gr Liv Area X Neighborhood_rank|Above grade (ground) living area square feet X Physical locations within Ames city limits|
|**bsmt sf_qual**|*float*|Total Bsmt SF X Overall Qual|Total square feet of basement area X Rates the overall material and finish of the house|


**Model Execution**

Train / Test Split
 - Splitted the Supervised data set to 75% - 25% where 75% is used for training the model and 25% is used for supervised testing

Scaling
 - Using standard scaler to center and scale all features into a common scale as we will be using regularization

Benchmark model
 - Linear model as benchmark for model selection

Regularization
 - Ridge, Lasso and ElasticNet models
 - Identified features that has 0 coefficient in Lasso model

Model selection
 - Removed features that has 0 coefficient in Lasso model
 - Refitted and predict with Linear, Ridge, Lasso and ElasticNet models

Assessment
 - Test models with MAE, MSE, RMSE, Cross-Validation Scores for R^2
 - Comparing scores of test set and selected Lasso model for production and implementation


### Top features with correlation to sales price in absolute value
|**Feature**|**Correlation**|
|---|---|
|Liv Area_qual|0.872916|
|Liv Area_neighbor|0.855079|
|bsmt sf_qual|0.830457|
|Liv Area_bsmt sf|0.821892|
|bsmt sf_neighbor|0.821573|
|Overall Qual|0.804410|
|Exter Qual|0.715866|
|Kitchen Qual|0.694008|
|Total Bsmt SF|0.667955|
|Garage Area|0.655399|

---

### What values did the model find most important?

Final Lasso model was fitted with 80 features
The features with the largest coefficients:

|**Feature**|**Coefficients**|
|---|---|	
|bsmt sf_qual|31831.071643|
|Liv Area_qual|29291.207631|
|Total Bsmt SF|15481.259340|
|Overall Qual|9026.601533|
|Bsmt Unf SF|8040.275624|
|Liv Area_bsmt sf|7999.014900|
|Lot Area|6804.573712|
|sale_type_New|6767.370142|
|Liv Area_neighbor|6132.203478|
|bsmt sf_neighbor|5977.583515|

---

## Final Model Details
 * Lasso Model
 * Mean Absolute error     : 15346.96879
 * Mean Squared error      : 414513931.46842
 * Root Mean Squared error : 20359.61521
 * Optimal Alpha is        : 71.08159356753374
 * R^2 score is            : 0.91342

---

## Insights, Findings & Recommendations
 
 - Tested per unit change in selected feature to see effect on SalePrice
 - Tested with Overall Quality, External Quality, Kitchen Quality, Total Basement Square Feet, Ground Floor Living Area
 
Results are as follows:
  - 1 unit change in Overall Qual leads to approximately 10820.978792853928 change in SalePrice
  - 1 unit change in Exter Qual leads to approximately 4685.020657317706 change in SalePrice
  - 1 unit change in Kitchen Qual leads to approximately 6698.188331313283 change in SalePrice
  - 1 unit change in Total Bsmt SF leads to approximately 28.325894480552776 change in SalePrice
  - 1 unit change in Gr Liv Area leads to approximately 49.308528164149735 change in SalePrice
  - 1 unit change in Garage Area leads to approximately 12.805701398084716 change in SalePrice

## Overall quality
Findings : 
* Improving the overall quality of the property by 1 grade leads to a change in average sale price by approximately $10,000
* Home buyers consider the Overall quality and condition of the property. Renovations takes time and money
* Home buyers are likely to pay more for a property that is move in ready

Recommendations :
* Basic maintenance of homes in Iowa cost around $2500
* Ensure no leaks in pipes or roofs within property, electrical wiring is not exposed. Plumbing and electricity in working condition
* No cracks on walls, ceilings, floors, window etc
* Property can be properly secured property
* Property is move in ready

## Exterior quality
Findings :
* Improving the exterior of the property by 1 grade can potentially increase the value of your house by approximately $4685.
* The exterior of your home is the first thing people see on your sale listing. A better quality exterior means a higher chance in getting buyers to click on your listing or attract buyers to view your property.
* As your property attracts more interest, naturally there will be more bids and the seller has a higher bargaining power to push up their property sale price.

Recommendations :
* Repaint the exterior of your home, mow the lawn and be sure grass is not overgrown (especially during summer)
* Change the exterior of your property to a better quality

## Kitchen Quality
Findings:
* Improving the exterior of the property by 1 grade can potentially increase the value of your house by approximately $6698
* More than 54% of consumers reported cooking more and baking more in America
* After a complete kitchen remodel, 90% of homeowners reported they wanted to be in their homes more

Recommendations :
* Look at quotes from contractors to remodel kitchen
* Adopt open concept kitchen so you make kitchen look bigger and living area look bigger

## Total Basement Square Feet
Findings : 
* From our model, increasing the basement square feet of the property leads to change in your sale price by approximately $28.33 per SF
* Average cost of finishing a basement is lower than addition of an above ground room
* Emergency shelter during hurrican season

Recommendations :
* Finish up your basement if it is unfinish
* If no basement, evaluate the all in cost required and reconsider if it will be too expensive

## Ground living area 

Findings : 
* From our model, increasing the ground living area potentially increases your real estate value by approximately $49 per SF
* This is the main area homebuyers look at when viewing the property. It is where you, as the seller  are the host to your customer
* What homebuyers are after is living space. For the same neighborhood, the higher the living space, the more valuable the price of the property.

Recommendations :
* Look at your unutilized lot area and consider extension projects to increase your living space
* Consider enclosing your balcony and extend your living space. Open balcony is not considered part of living area
* Adopt open concept design to give homebuyers comfortable space when viewing your property

## Garage Area

Findings :
* Increasing the garage area SF will potentially increase the value of your real estate by approximately $12.81 per SF
* Des Moines is the city located beside Ame. Cars in Des Moines are at risk of theft. Having a garage protects one's car from getting stolen
* Families in Iowa owns  2 cars on average having more garage space means you will have enough space to secure all your automobile
* Extra storage space and work space

Recommendations :
* Look at your unutilized lot area and consider adding garage or expanding your garage space
* Attached garage is recommended as one does not need to get outdoors to access their car during the winter
---

## Limitations :
This model is just a guide line for one to follow and it does not guarantee success at driving up the value of your real estate.
There are million of factors that come into play.
To name a few, Macro economic factors like COVID 19, resulting in halt in home evictions that results in more than 40 million landlords (home owners) seeking to evict their tenant. This will cause a huge decline in property prices like the case in 2008 when more and more properties are being foreclosed.
There may also be future development in your neighborhoods that result in an exponential increase in home value. You probably dont have to do anything and to increase the value of your property.
Also, this model is just a reference to predict home prices in Ame, Iowa. If you consider the same property features but from San Francisco, the prediction will be way off.
If unsure about your home value, it is still safer to go through an evaluator or multiple evaluators to get accurate estimates.

---
## Data Sources

Provided
 - train.csv
 - test.csv

- Property search with parcel ID: https://beacon.schneidercorp.com/Application.aspx?AppID=165&LayerID=2145&PageTypeID=2&PageID=1104
- Home inspection checklist for home quality check : http://donerighthomeinspection.com/what-we-inspect/index.asp
- Basement construction on property prices : https://www.homelight.com/blog/how-much-value-does-a-finished-basement-add/
- Kitchen quality article : https://www.foodnavigator-usa.com/Article/2020/04/15/Survey-Cooking-at-home-will-become-the-new-normal-post-pandemic
- Research on kitchen remodelling : https://www.homelight.com/blog/how-much-does-a-kitchen-remodel-increase-home-value/
- Car theft article Iowa : https://www.allproservicenter.com/protecting-your-sedan-from-theft-in-des-moines-iowa/
- Number of cars per household in Iowa : https://datausa.io/profile/geo/iowa#:~:text=The%20average%20car%20ownership%20in%20Iowa%20is%202%20cars%20per%20household.
