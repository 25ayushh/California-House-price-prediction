# California House Price Prediction

This project aims to predict house prices in California using two machine learning models: **Linear Regression** and **Random Forest Regression**. The dataset includes various features that describe the properties and demographics of the area.

## Dataset Features
- **longitude**: The geographical longitude coordinate of the house.
- **latitude**: The geographical latitude coordinate of the house.
- **housing_median_age**: The median age of the house.
- **total_rooms**: The total number of rooms in the house.
- **total_bedrooms**: The total number of bedrooms.
- **population**: The total population of the area.
- **households**: The number of households in the area.
- **median_income**: The median income of the household occupants.
- **median_house_value**: The median value of the house (target variable).
- **ocean_proximity**: The proximity of the house to the ocean.

## Project Workflow

### 1. Data Preprocessing
- The dataset is cleaned, handling missing values and removing null data points.
- The data is split into features (`X`) and the target variable (`y`), which is the median house price.

### 2. Data Splitting
- The data is split into training and testing sets using an 80/20 ratio to allow for model training and evaluation.
  ```python
  from sklearn.model_selection import train_test_split
  X = data.drop('median_house_value', axis=1)
  y = data['median_house_value']
  X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
  ```

### 3. Model Training and Evaluation
- **Linear Regression**: A simple model to establish a baseline for house price prediction.
- **Random Forest Regression**: A more complex, ensemble-based model that often provides better performance by reducing variance.
  
  Both models are evaluated using:
  - **Mean Squared Error (MSE)**
  - **R² score**

### 4. Results Visualization
- A comparison between the predicted and actual house prices is plotted to visually assess the model’s performance.

## Requirements
- Python 3.x
- Jupyter Notebook or Google Colab
- Libraries:
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `matplotlib` (for visualization)

