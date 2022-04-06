# Time Series Prediction for Food Sustainability
A machine learning system using a statistical regression model that can predict the top-k food products that would endure a shortage in each country in a specific period in the future. The prediction performance in terms of absolute error, root mean square error show promising results due to its low errors. This solution could help organizations and manufacturers understand the productivity and sustainability needed to satisfy the global demand.

## Python libraries
- pandas
- numpy
- matplotlib
- plotly
- seaborn
- statsmodels
- scikit-learn
- jupyter-notebook

## Dataset
The dataset for the solution is provided by Food and Agriculture Organization Corporate Statistical Database (FAOSTAT). The database provides free access to food and agriculture data for over 245 countries and territories and covers all FAO regional groupings from 1961 to the most recent year available (2019). The three datasets chosen from this database are as follows,
- Climate Change: Emissions Totals
- Forestry: Forestry Production and Trade
- Production: Crops and livestock products

## Steps involved in Training and Inference
1. Reading datasets from Amazon S3 buckets
2. Preprocessing the dataset - Removing NaN, Dropping redundant values, pivot tables etc
3. Perform Granger causality test
4. Check for stationary series - ADF test
5. Perform 1st and 2nd differencing to modify non-stationary series to stationary one
6. Train dataset with VAR model (each item is trained against different emissions as a separate model)
7. Run inference with trained model
8. With the forecast output - perform invert transformation to get back values in original scale
9. Find the top-k items that endure shortage by particular year
10. Visualize the production graphs for top-k items

## Visualizations
The visualizations on the datasets:
- Emission trend graphs for each emission element
- Production trend graphs for each production item/forest product
- Distribution of forestry products
- Distribution of production crops
- Distribution of emissions and emission types

## More information
Exploratory data analysis, data preprocessing, training and results - [Food sustainability](https://github.com/fionavictoria/MLFoodSustainability/blob/main/Time%20Series%20Prediction%20for%20Food%20sustainability.pdf)
   
> The future work of this project would focus on adding more datasets on Temperature change, Rainfall, Population, Trade flows that would add intricate factors to decide the production of crops in the future. 
> The solution can also be extended to cover social and economic sustainability to make the system a robust model for sustainability prediction. Technology companies like Microsoft and AWS are investing more in building sustainability solutions to reduce the carbon footprint. This research gives insights into what factors an organization should care about while designingsustainablesolutions. Giventherightdataset,thisresearchcanbefurtherextendedto be an in-built library to make sustainable factor predictions on social, environmental, and economic aspects.
-----------------------------
