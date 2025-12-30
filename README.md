# California Housing Prices Model

## Project Overview and Purpose
This project aims to predict the median house value in various California districts based on 1990 census data. It explores a complete data science pipeline, from advanced data cleaning (handling missing values and outliers) to implementing and comparing multiple regression models.

## Key Technologies and Libraries
- **Language**: Python
- **Data Manipulation**: `pandas`, `numpy`
- **Visualization**: `matplotlib`, `seaborn`
- **Machine Learning**: `scikit-learn`, `xgboost`

## Data and Methodology
### Preprocessing Workflow
1. **Feature Mapping**: Categorical data like `ocean_proximity` was mapped to numerical values and later encoded using one-hot encoding.
2. **Missing Data**: Used `KNNImputer` (k=3) to intelligently fill missing values in the dataset.
3. **Outlier Removal**: 
   - Implemented `IsolationForest` to remove general anomalies.
   - Applied Interquartile Range (IQR) filtering specifically for categorical distribution.
4. **Feature Scaling**: Utilized `MinMaxScaler` to normalize features for better model performance.
5. **Feature Engineering**: Created interaction terms such as `income_x_latitude` to capture geographical economic trends.

### Model Architectures
The project evaluates three different approaches:
- **Linear Regression**: Used as a baseline model.
- **Random Forest Regressor**: An ensemble method to capture non-linear relationships.
- **XGBoost Regressor**: Optimized gradient boosting for high-performance prediction.

## Results and Insights
- **Performance**: The models were evaluated using the R² Score, with ensemble methods (Random Forest and XGBoost) typically outperforming simple Linear Regression.
- **Key Drivers**: Median income remains the most significant predictor of housing prices.
- **Visual Analysis**: The project includes residual plots to verify the assumptions of the regression models.


## How to Run
1. Ensure you have the `housing.csv` dataset in the same directory as the notebook.
2. Install dependencies: `pip install -r requirements.txt`.
3. Open `California Housing Prices Model.ipynb` and run all cells to see the full analysis and model comparisons.
