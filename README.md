# Insurance Data Analysis and Prediction

This project involves analyzing and building a predictive model for insurance charges based on a dataset containing demographic, health, and lifestyle attributes. The final model uses multiple linear regression to predict charges.

---

## Features of the Project

### 1. **Data Loading and Preprocessing**
- The dataset `new_insurance_data.csv` is loaded using Pandas.
- Missing values are handled:
  - Numerical columns are filled with their mean values.
  - Categorical columns are filled with their mode values.
- Outliers in specific numerical columns (`bmi`, `Hospital_expenditure`, `Anual_Salary`, `charges`) are removed using the Interquartile Range (IQR) method.

### 2. **Variance Inflation Factor (VIF) Analysis**
- VIF is calculated to detect multicollinearity among features.
- Columns with high VIF (>5) are iteratively removed to ensure a robust model.
  - Dropped columns include: `num_of_steps`, `bmi`, `age`, `NUmber_of_past_hospitalizations`.

### 3. **Feature Selection**
- Final features used for modeling:
  - `children`
  - `Claim_Amount`
  - `past_consultations`
  - `Hospital_expenditure`
  - `Anual_Salary`

### 4. **Model Pipeline**
- A pipeline is created for efficient preprocessing and modeling:
  - **Preprocessing:**
    - Numerical columns are scaled using `StandardScaler`.
    - Categorical columns are encoded using `OneHotEncoder`.
  - **Modeling:**
    - A `LinearRegression` model is used to predict insurance charges.

### 5. **Model Evaluation**
- Metrics used to evaluate the model:
  - **R2 Score:** Measures the proportion of variance in the dependent variable explained by the model.
  - **Mean Absolute Percentage Error (MAPE):** Measures the accuracy of predictions as a percentage.
- Results:
  - **R2 Score:** `0.8436`
  - **MAPE:** `0.2816`

---

## File Structure
- `new_insurance_data.csv`: The input dataset.
- `insurance_model.py`: The script containing data preprocessing, VIF calculation, and model pipeline.
- `README.md`: This file, explaining the workflow and results.

---

## Instructions to Run
1. Install the required libraries:
   ```bash
   pip install pandas numpy scikit-learn statsmodels
   ```
2. Place the `new_insurance_data.csv` file in the same directory as the script.
3. Run the script:
   ```bash
   python insurance_model.py
   ```
4. View the R2 Score and MAPE in the output.

---

## Future Improvements
- Explore additional models like Decision Trees or Random Forests to improve accuracy.
- Perform hyperparameter tuning to optimize the Linear Regression model.
- Investigate feature engineering techniques for better input representation.

---

## Dependencies
- Python 3.7 or above
- Libraries:
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `statsmodels`

---

## Contact
For questions or suggestions, please contact [abhishekanase07@gmail.com].


