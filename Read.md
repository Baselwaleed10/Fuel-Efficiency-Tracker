# Fuel Efficiency Tracker: A Machine Learning Approach

This repository presents a machine learning-based approach for predicting vehicle fuel efficiency (measured in MPG - miles per gallon). The models were trained on a cleaned car dataset and evaluated to determine the most accurate method for real-world fuel consumption prediction.

## Paper Authors
- AL Basel Waleed  
- Asem Eliwa  
- Mahmoud Mohamed  
Nile University

## Abstract
We developed and evaluated regression models including:
- Random Forest Regressor
- XGBoost Regressor
- Neural Networks

The goal was to create a Fuel Efficiency Tracker tool that can estimate MPG based on vehicle features such as make, model, engine size, and more.

## Dataset Description
The dataset includes:
- Model year
- Manufacturer
- Fuel type
- Engine size
- Transmission type
- Mileage
- MPG (target)

### Preprocessing Steps:
- Outlier removal (MPG values between 1–150)
- Label encoding for categorical features
- 80/20 train-test split

## Models Used

1. **Random Forest Regressor**  
   - 200 trees  
   - Max depth = 15

2. **XGBoost Regressor**  
   - 200 estimators  
   - Learning rate = 0.05  
   - Max depth = 6

3. **Neural Network**  
   - 2 hidden layers (128 and 64 units)  
   - ReLU activation, Batch Normalization, Dropout  
   - Optimizer: Adam

## Results

| Model           | MSE     | R² Score |
|----------------|---------|----------|
| Random Forest  | 12.33   | 0.9184   |
| XGBoost        | 16.22   | 0.8927   |
| Neural Network | 31.76   | 0.7899   |

Random Forest achieved the best performance in terms of both Mean Squared Error and R² score.

## Conclusion
Ensemble models like Random Forest and XGBoost outperform deep neural networks for this fuel efficiency task, particularly when working with structured tabular data. This project demonstrates the feasibility of building a reliable fuel consumption prediction tool based on vehicle characteristics.

## References
1. Chen & Guestrin, “XGBoost: A scalable tree boosting system”, ACM SIGKDD, 2016.  
2. Breiman, “Random Forests”, Machine Learning, 2001.  
3. Goodfellow et al., *Deep Learning*, MIT Press, 2016.
