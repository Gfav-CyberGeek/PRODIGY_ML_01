# PRODIGY_ML_01

# House Price Prediction using Linear Regression

This repository contains the implementation of a linear regression model to predict the prices of houses based on their square footage, number of bedrooms, and bathrooms. The dataset is sourced from the [Kaggle House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data) competition, and additional features are used to improve model performance.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Details](#model-details)
- [Results](#results)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project implements a linear regression model to predict house prices using features such as:

- Square Footage (`1stFlrSF`)
- Number of Bedrooms (`BedroomAbvGr`)
- Number of Bathrooms (`FullBath`)

We extended the model by adding more features, including the neighborhood, house style, garage capacity, and living area, and applied data preprocessing techniques such as scaling and one-hot encoding to handle categorical variables.

## Dataset

The dataset is sourced from the Kaggle competition ["House Prices: Advanced Regression Techniques"](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data).

- **Features used**: 
  - `1stFlrSF` (First floor square footage)
  - `GrLivArea` (Above-ground living area square footage)
  - `BedroomAbvGr` (Number of bedrooms above ground)
  - `FullBath` (Number of full bathrooms)
  - `TotalBsmtSF` (Total basement square footage)
  - `OverallQual` (Overall material and finish quality)
  - Categorical features like `Neighborhood`, `HouseStyle`, etc.

- **Target variable**: `SalePrice` (House price in dollars)

## Installation

To get started with this project, clone the repository and install the necessary dependencies:

1. Clone the repository:
   ```bash
   git clone https://github.com/Gfav-CyberGeek/PRODIGY_ML_01.git
   cd PRODIGY_ML_01
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Download the dataset from the Kaggle competition [here](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data), and place the `train.csv` file in the project directory.

2. Run the Python script:
   ```bash
   python house_price_prediction.py
   ```

3. The script will output the model's performance, including metrics such as Mean Squared Error (MSE) and R-squared (R²). Additionally, a scatter plot of actual vs predicted house prices will be displayed.

### Example Output

```
Mean Squared Error: 123456789.0
R-squared: 0.85
Cross-validated R-squared scores: [0.80, 0.84, 0.81, 0.83, 0.82]
Average cross-validated R-squared: 0.82
```

## Model Details

- **Preprocessing**: The dataset contains both numeric and categorical features. We used `StandardScaler` to scale numeric features and `OneHotEncoder` for categorical features.
  
- **Pipeline**: A scikit-learn pipeline was created to handle preprocessing and model training in a single step.

- **Model**: A simple linear regression model was trained on the selected features. We experimented with both basic and extended features to improve the model's performance.

### Features Used

- `1stFlrSF`: First floor square footage
- `GrLivArea`: Above-ground living area square footage
- `BedroomAbvGr`: Number of bedrooms above ground
- `FullBath`: Number of full bathrooms
- `TotalBsmtSF`: Total basement square footage
- `OverallQual`: Overall material and finish quality (ordinal)
- `Neighborhood`: Categorical, represents house neighborhood
- `HouseStyle`: Categorical, represents house architectural style
- `GarageCars`: Number of cars that can fit in the garage

## Results

The linear regression model performs reasonably well, with an R-squared score of around 0.82 after cross-validation. The model is able to capture the relationship between house prices and key features such as square footage, number of bedrooms, and quality indicators.

A scatter plot of actual vs predicted prices is generated to visualize the model's performance.

## Future Improvements

1. **Feature Engineering**: Further engineering of features such as creating interaction terms between key variables (e.g., `OverallQual` and `GrLivArea`).
2. **Advanced Models**: Explore more advanced models such as Ridge, Lasso, or Decision Trees to improve accuracy.
3. **Hyperparameter Tuning**: Use `GridSearchCV` or `RandomizedSearchCV` to fine-tune hyperparameters for better performance.
4. **Handling Missing Data**: Explore more sophisticated imputation techniques or drop features with a significant amount of missing data.

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue if you have any suggestions or find any bugs.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature-branch`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Open a pull request

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
