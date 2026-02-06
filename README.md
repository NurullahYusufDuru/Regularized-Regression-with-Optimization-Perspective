# DS538 Homework 1 – Regression, Optimization, and Regularization

This notebook contains the solution to **DS538 Homework 1**, focusing on linear regression modeling, optimization-based estimation, and regularization techniques. The assignment explores how different modeling and optimization approaches affect regression performance and coefficient behavior.

## Dataset and Preprocessing
The analysis starts with loading the dataset and augmenting it with two randomly generated features (`Rand1` and `Rand2`) to examine their impact on model performance. These features are later used to demonstrate feature relevance and overfitting behavior.

## Regression Models
Multiple regression models are implemented and compared:
- **Model 1:** Baseline linear regression  
- **Model 2 & 3:** Variants including additional features  
- **Model 4:** A small-sample regression case demonstrating overfitting  

Model comparison shows that random features do not meaningfully affect performance, while certain original features (e.g., `Length1`) are strongly related to the target variable. The perfect R² score observed in Model 4 highlights high variance due to insufficient training data.

## Optimization-Based Regression
The notebook formulates the linear regression problem as an explicit optimization task and solves it using **SciPy optimization**.  
The results confirm that the optimized coefficients and intercept exactly match those obtained from standard linear regression, leading to identical predictions.

## Regularization Analysis
Several Lasso-based regularization approaches are examined:
- Lasso with coefficient upper bounds  
- Lasso with penalty (λ-based formulation)  
- Lasso using scikit-learn  

The analysis demonstrates how decreasing the coefficient bounds or increasing the regularization parameter shrinks coefficients toward zero. Differences between custom Lasso formulations and scikit-learn’s implementation are explained through their loss function scaling.

## Technologies
- Python  
- pandas, numpy  
- scikit-learn  
- SciPy  
- matplotlib  

## Key Takeaways
This homework illustrates the equivalence between least squares regression and optimization-based solutions, highlights the dangers of overfitting in small samples, and provides a clear comparison of different Lasso regularization formulations.

