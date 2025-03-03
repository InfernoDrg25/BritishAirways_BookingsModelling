# British Airways Customer Booking Prediction
This repository contains the code and analysis for predicting customer bookings for British Airways using a Random Forest Classifier. The goal is to understand the factors influencing bookings and improve marketing strategies.

## Project Overview
The objective of this project is to predict whether a customer will complete a booking based on various features such as flight day, route, sales channel, and more. Understanding these factors can help British Airways enhance their marketing efforts and improve customer experience.

## Dataset
The dataset used for this analysis is `customer_booking.csv`, which contains the following key features:
- `flight_day`: Day of the week the flight is scheduled
- `route`: Flight route
- `sales_channel`: Channel through which the booking was made
- `purchase_lead`: Number of days between booking and flight
- `flight_hour`: Hour of the day the flight is scheduled
- `num_passengers`: Number of passengers in the booking
- `booking_complete`: Target variable (0 = No, 1 = Yes)

## Jupyter Notebook
1. **Exploratory Data Analysis** (`exploratory_data_analysis.ipynb`):
   - Load and explore the dataset
   - Visualize the distribution of features
   - Analyze relationships between features and the target variable

2. **Data Preprocessing** (`data_preprocessing.ipynb`):
   - Handle missing values
   - Encode categorical variables using Label Encoding
   - Scale numerical features using StandardScaler
   - Split the data into training and testing sets

3. **Model Training** (`model_training.ipynb`):
   - Train a Random Forest Classifier on the preprocessed data
   - Evaluate the model using various metrics (accuracy, precision, recall, F1-score)
   - Perform cross-validation to ensure robustness
   - Analyze feature importance
   - Plot ROC curve and calculate AUC score

## Results
The Random Forest model achieved the following performance metrics on the test set:
- **Accuracy**: 85.39%
- **Precision**: 56.36%
- **Recall**: 10.36%
- **F1 Score**: 17.50%
- **ROC AUC Score**: 77.65%

## Key Findings
- The "Purchase Lead" is by far the most dominant feature, suggesting that the timing of the booking is crucial.
- “Route” importance suggests that certain routes may have different booking completion patterns.
- Features related to the flight itself (hour, day, duration) and booking details (length of stay, origin) are generally more important than the optional service features.

## Recommendations
Based on the analysis, the following recommendations are made to British Airways:
- Focus marketing efforts on high-demand routes and sales channels with higher booking completion rates.
- Offer incentives for early bookings to increase the completion rate.
- Monitor and analyze booking patterns regularly to adapt strategies accordingly.

Thank you for exploring this project!
