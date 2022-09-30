# Phase 2 Project Description


## Project Overview

For this project, I used multiple linear regression modeling to analyze house sales in a northwestern county.

### Business Problem

So You’re Not Chip And Joanna Gaines? You don't have to be to get the most bang for your buck when buying and selling real estate. Whether you are just starting out in the flipping business, want to increase the value of your current home, or are long term planning for your financial future, you can analyze certain aspects of the real estate market to make the best decisions for your needs. 

### The Data

I used the King County House Sales dataset, which can be found in  `kc_house_data.csv` in the data folder in this project's GitHub repository. The description of the column names can be found in `column_names.md` in the same folder. We will be sorting through the data to decide what we want to keep and focus on to include in our models.

### Modeling

After reviewing the data, I checked which data points had the highest correlation to the price. I made dummies of categorical items, removed outliers, and created a test and train set to make a baseline model with a adjusted R^2 score to .602. 

![baseline.png](https://user-images.githubusercontent.com/102811933/193312198-1a59b297-7054-4524-a67f-2895e0c15b1e.png)
Then I took out more outliers, removed anything with p-values higher than .05, and ran it again, increasing the adjusted R^2 score to .607. 
![model_improved.png](https://user-images.githubusercontent.com/102811933/193312717-b3cf5ecf-52eb-41b2-9f44-c957a47f27a9.png)

I further experimented with scaling, and then repeating the whole process without dummies and only with a limited number of variables. Each path had it's positives and negatives that I would like to revisit, though I was suprised that the non-dummies model performed considerably lower than the non-dummies model in consideration to ad. R^2 values. 

The results of the models revealed coeffients that varied greatly, high multicollinearity, and very high MSE. This could be because in the real estate business, you can have one home be drastically priced one way in one area, and the opposite in another location. Because of this, and other factors not included on the dataset, we can presume that more information and a more detailed model will be needed to accurately product results.

## Conclusion

**When buying:**
Look for undervalued homes with the most sqft living space that you can afford, especially with neighbors with big homes. Carefully consider how many bathrooms the house has, and if there is room to install another bathroom or expand a small bathroom (think .25/.5/.75 to a full 1 bath). Consider searching to buy in the colder months when prices are lower, specifically late Autumn (November) and winter (December thru January) as home prices generally skew lower then.

**Before selling:¶**
If you do not intend on expanding the living area of a home and cannot add any more bathrooms, it is advisable to renovate what you do have by upgrading features, appliances, and fixtures.

**When selling:**
When you are looking to sell for the most, keep in mind that you would actually want to list in early Spring (March), or mid to late summer (July and August), as most homes sell for higher in the Spring/early Summer and very late Summer/early Autumn.
