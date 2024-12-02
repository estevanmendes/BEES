


## Summary of Workflow

### Data Preparation
1. **Data Loading and Preprocessing**:
    - Loaded training and testing datasets.
    - Applied filters to segregate data based on the number of orders in the last 12 months.
    - Scaled the features using `StandardScaler`.

### Model Training and Evaluation
2. **Elastic Net Model**:
    - Trained on training data with less than 3 orders.
    - Evaluated and plotted the coefficients.

3. **Random Forest Model**:
    - Trained on the same training data.
    - Evaluated and plotted feature importance.

4. **K-Nearest Neighbors (KNN) Model**:
    - Trained on the same training data.
    - Evaluated and plotted the results.

5. **Support Vector Machine (SVM)**:
    - Trained on the same training data.
    - Evaluated and plotted the results.

6. **Recurrent Neural Network (RNN)**:
    - Trained on the same training data.
    - Evaluated and plotted the results.

7. **Genetic Programming**:
    - Applied to evolve models.
    - Evaluated and selected the best model.

### Prediction
8. **Prediction for August**:
    - Prepared the testing dataset for August.
    - Trained Elastic Net models on the entire training data.
    - Predicted the number of orders for August and combined the results.

9. **Handling Clients with No Previous Orders**:
    - Used the median number of orders from clients in their first month to predict for clients with no previous orders.

### Analysis
10. **Customer Segmentation**:
    - Split customers into deciles based on their total order count.
    - Focused on decile 9 for further analysis.

11. **Maximum Likelihood Estimation (MLE)**:
    - Applied MLE to fit Poisson, Chi-squared, and Normal distributions to the data.
    - Evaluated the fit using visual inspection and statistical criteria.

12. **Minimization of Error**:
    - Used minimization of error to fit the distribution to a combination of functions.
    - Evaluated the fit using visual inspection and statistical criteria.

13. **Time Between Orders Analysis**:
    - Analyzed the time between orders for customers in decile 9.
    - Fitted a Poisson distribution to the data considering the weekly cycle.

### Conclusion
- The best model for predicting the number of orders uses the Poisson distribution for weekly orders, based on R-squared and residuals.