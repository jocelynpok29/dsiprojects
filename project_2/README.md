# dsiprojects
### Overview

This project seeks to identify the best regression model to predict the price of the housing in Ames, Iowa and the best predictors of housing prices. This can be done by looking into the house characteristics and locations.

### Datasets

#### Provided Data

The provided datasets are as follows:

- [Train dataset](./datasets/train.csv)
- [Test dataset](./datasets/test.csv)
- [Lasso submission](./datasets/submission_lasso.csv)
- [Ridge submission](./data/submission_ridge.csv)


These are the training and testing data for housing prices as well as the predicted prices submitted using the lasso and ridge model.

### Data Dictionary

|Feature|Type|Dataset|Description|
|:---|:---:|:---:|:---|
|Id|int|train_df|The Id of the record|
|PID|int|train_df|Parcel Id|
|MS SubClass|int|train_df|The building class|
|MS Zoning|object|train_df|Identifies the general zoning classification of the sale.|
|Lot Frontage|float|train_df|Linear feet of street connected to property|
|Lot Area|int|train_df|Lot size in square feet|
|Street|object|train_df|Type of road access to property|
|Alley|object|train_df|Type of alley access to property|
|Lot Shape|object|train_df|General shape of property|
|Land Contour|object|train_df|Flatness of the property|
|Utilities|object|train_df|Type of utilities available|
|Lot Config|object|train_df|Lot configuration|
|Land Slope|object|train_df|Slope of property|
|Neighborhood|object|train_df|Physical locations within Ames city limits|
|Condition 1|object|train_df|Proximity to main road or railroad|
|Condition 2|object|train_df|Proximity to main road or railroad (if a second is present)|
|Bldg Type|object|train_df|Type of dwelling|
|House Style|object|train_df|Style of dwelling|
|Overall Qual|int|train_df|Overall material and finish quality|
|Overall Cond|int|train_df|Overall condition rating|
|Year Built|int|train_df|Original construction date|
|Year Remod/Add|int|train_df|Remodel date (same as construction date if no remodeling or additions)|
|Roof Style|object|train_df|Type of roof|
|Roof Matl|object|train_df|Roof material|
|Exterior 1st|object|train_df|Exterior covering on house|
|Exterior 2nd|object|train_df|Exterior covering on house (if more than one material)|
|Mas Vnr Type|object|train_df|Masonry veneer type|
|Mas Vnr Area|float|train_df|Masonry veneer area in square feet|
|Exter Qual|object|train_df|Exterior material quality|
|Exter Cond|object|train_df|Present condition of the material on the exterior|
|Foundation|object|train_df|Type of foundation|
|Bsmt Qual|object|train_df|Height of the basement|
|Bsmt Cond|object|train_df|General condition of the basement|
|Bsmt Exposure|object|train_df|Walkout or garden level basement walls|
|BsmtFin Type 1|object|train_df|Quality of basement finished area|
|BsmtFin SF 1|float|train_df|Type 1 finished square feet|
|BsmtFin Type 2|object|train_df|Quality of second finished area (if present)|
|BsmtFin SF 2|float|train_df|Type 2 finished square feet|
|Bsmt Unf SF|float|train_df|Unfinished square feet of basement area|
|Total Bsmt SF|float|train_df|Total square feet of basement area|
|Heating|object|train_df|Type of heating|
|Heating QC|object|train_df|Heating quality and condition|
|Central Air|object|train_df|Central air conditioning|
|Electrical|object|train_df|Electrical system|
|1st Flr SF|int|train_df|First Floor square feet|
|2nd Flr SF|int|train_df|Second floor square feet|
|Low Qual Fin SF|int|train_df|Low quality finished square feet (all floors)|
|Gr Liv Area|int|train_df|Above grade (ground) living area square feet|
|Bsmt Full Bath|float|train_df|Basement full bathrooms|
|Bsmt Half Bath|float|train_df|Basement half bathrooms|
|Full Bath|int|train_df|Full bathrooms above grade|
|Half Bath|int|train_df|Half baths above grade|
|Bedroom AbvGr|int|train_df|Number of bedrooms above basement level|
|Kitchen AbvGr|int|train_df|Number of kitchens|
|Kitchen Qual|object|train_df|Kitchen quality|
|TotRms AbvGrd|int|train_df|Total rooms above grade (does not include bathrooms)|
|Functional|object|train_df|Home functionality rating|
|Fireplaces|int|train_df|Number of fireplaces|
|Fireplace Qu|object|train_df|Fireplace quality|
|Garage Type|object|train_df|Garage location|
|Garage Yr Blt|float|train_df|Year garage was built|
|Garage Finish|object|train_df|Interior finish of the garage|
|Garage Cars|float|train_df|Size of garage in car capacity|
|Garage Area|float|train_df|Size of garage in square feet|
|Garage Qual|object|train_df|Garage quality|
|Garage Cond|object|train_df|Garage condition|
|Paved Drive|object|train_df|Paved driveway|
|Wood Deck SF|int|train_df|Wood deck area in square feet|
|Open Porch SF|int|train_df| Open porch area in square feet|
|Enclosed Porch|int|train_df|Enclosed porch area in square feet|
|3Ssn Porch|int|train_df|Three season porch area in square feet|
|Screen Porch|int|train_df|Screen porch area in square feet|
|Pool Area|int|train_df|Pool area in square feet|
|Pool QC|object|train_df|Pool quality|
|Fence|object|train_df|Fence quality|
|Misc Feature|object|train_df|Miscellaneous feature not covered in other categories|
|Misc Val|int|train_df|$Value of miscellaneous feature|
|Mo Sold|int|train_df|Month Sold)|
|Yr Sold|int|train_df| Year Sold|
|Sale Type|object|train_df|Type of sale|
|Sale Price|int|train_df|the property's sale price in dollars|
