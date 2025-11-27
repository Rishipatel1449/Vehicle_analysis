# Vehicle Price Analysis - Project Summary

## Overview

This project analyzes used car pricing data to identify key factors that drive vehicle prices. The analysis uses machine learning regression models to predict car prices and provides insights to used car dealerships.

## Key Findings

### Best Performing Model
- **Polynomial Regression (4 features, degree 2)**
  - R² = 0.4906 (explains ~49% of price variation)
  - MAE = $6,984.82 (average prediction error)
  - RMSE = $10,467.73

### Key Drivers of Used Car Prices

1. **Vehicle Age/Year (Strongest Predictor)**
   - Newer vehicles command significantly higher prices
   - Vehicle age alone explains 26% of price variation
   - Relationship is non-linear (polynomial degree 3 performs best for year alone)
   - **Recommendation**: Prioritize acquiring newer inventory (2015-2025 models)

2. **Mileage (Odometer)**
   - Lower mileage increases value, but effect is weaker than age
   - Odometer reading alone explains only 5% of price variation
   - **Recommendation**: While lower mileage is desirable, don't overpay for low-mileage older vehicles

3. **Engine Size (Cylinders)**
   - More cylinders associated with higher prices
   - Cylinders alone explain 7% of price variation
   - **Recommendation**: Consider engine size when pricing, especially for performance-oriented segments

4. **Feature Interactions**
   - Combining multiple features with polynomial transformations significantly improves prediction accuracy
   - R² improves from 0.37 (linear) to 0.49 (polynomial) - a 32% improvement
   - **Recommendation**: Use comprehensive pricing models that consider multiple factors simultaneously

### Strategic Recommendations

**For Inventory Management:**
- Focus on 2015-2025 models for best price-to-value ratio
- Balance age and mileage: newer vehicles with moderate mileage often outperform older low-mileage vehicles
- Consider feature combinations rather than individual factors

**For Pricing Strategy:**
- Implement pricing models that consider year, odometer, age, and cylinders together
- Account for non-linear relationships (vehicle age has exponential impact)
- Set realistic expectations: model explains ~49% of variation; market factors, brand, condition, and location also matter

## Project Files

- **[Model.ipynb](Model.ipynb)** - Main analysis notebook with data exploration, model building, and evaluation
- **[prompt_II.ipynb](prompt_II.ipynb)** - CRISP-DM framework responses and response to findings

## Dataset

- **Original Dataset**: 426,880 used car listings
- **Cleaned Dataset**: 370,156 records after data cleaning
- **Features Analyzed**: Year, Odometer, Cylinders, Age
- **Target Variable**: Price (filtered to $1 - $200,000 range)

## Models Built

1. Single Feature Linear Regression Models (Year, Odometer, Cylinders, Age)
2. Polynomial Feature Models (Year only, degrees 2 and 3)
3. Multiple Linear Regression (4 features)
4. Polynomial Regression (4 features, degree 2) - **BEST MODEL**



## Technical Details

- **Language**: Python 3.11.7
- **Key Libraries**: pandas, numpy, matplotlib, seaborn, scikit-learn
- **Data Split**: 70% training, 30% testing (random_state=42)
- **Validation**: Train-test split with performance metrics (R², MAE, RMSE)



