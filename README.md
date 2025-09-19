INN Hotels Group: Booking Cancellation Prediction
Project Overview
This project provides a data-driven solution for the INN Hotels Group to address the high number of booking cancellations. The primary objective is to build a predictive machine learning model that can identify which bookings are likely to be canceled. By accurately predicting cancellations, the hotel can take proactive measures to minimize revenue loss and optimize resource management.

Business Problem
INN Hotels Group, a chain of hotels in Portugal, is experiencing a high rate of booking cancellations. This leads to significant revenue loss and operational inefficiencies. This project aims to analyze the factors influencing these cancellations and develop a predictive model to help the hotel group move from a reactive to a proactive cancellation management strategy.

Dataset
The dataset used for this project is INNHotelsGroup.csv. It contains detailed information about hotel bookings, including guest details, booking specifics, and historical data. Key features include:

booking_status: The target variable, indicating whether a booking was Canceled or Not_Canceled.

lead_time: The number of days between the booking date and the arrival date.

avg_price_per_room: The average price of the room per night.

market_segment_type: The channel through which the booking was made (e.g., Online, Offline).

no_of_special_requests: The number of special requests made by the guest.

repeated_guest: A flag indicating if the guest is a repeated visitor.

Methodology
The project followed a standard machine learning workflow, which included the following stages:

Exploratory Data Analysis (EDA): Initial analysis of the dataset to understand its structure, identify patterns, and uncover key relationships between variables. Visualizations were used to gain insights into factors influencing cancellations.

Data Preprocessing: The raw data was prepared for modeling. This involved:

Handling missing values and outliers.

Creating new, more informative features (total_nights, previous_booking_rate).

Encoding categorical variables.

Scaling numerical features.

Splitting the data into training and testing sets.

Model Building: Two baseline classification models were built:

Logistic Regression

Decision Tree Classifier

Model Performance Improvement: The baseline models were fine-tuned to enhance their performance.

Logistic Regression: Multicollinearity was addressed, and the optimal classification threshold was determined using the ROC curve.

Decision Tree Classifier: The model was pruned to prevent overfitting.

Model Comparison and Selection: All models were evaluated on key metrics (Precision, Recall, F1-score) to compare their performance. The best model was selected based on its ability to meet the business objective.

Key Findings & Recommendations
Key Factors: The EDA revealed that factors like lead_time, no_of_special_requests, and average_price_per_room are strong predictors of booking cancellations.

Final Model: The Tuned Decision Tree Classifier was selected as the final model due to its high recall score, which is crucial for identifying as many potential cancellations as possible.

Actionable Insights: Based on the model's predictions and insights, the following recommendations are made to the INN Hotels Group:

Targeted Communication: Engage with guests who have a high probability of canceling (e.g., those with long lead times) through personalized emails or special offers.

Dynamic Pricing: Adjust pricing for periods with a high risk of cancellation to maintain a healthy occupancy rate.

Proactive Interventions: Implement targeted interventions, such as early check-in offers or room upgrades, to incentivize high-risk guests to keep their bookings.

Feature Drift Detection: Continuously monitor the data to ensure the model remains relevant and effective over time.

By implementing these data-driven strategies, the hotel group can significantly reduce their cancellation rate and increase overall revenue.

How to Reproduce the Project
Clone the repository:

git clone [your_repository_url]

Install dependencies:

pip install pandas numpy scikit-learn statsmodels matplotlib seaborn

Run the analysis:

The complete analysis, including the code for data preprocessing, model building, and tuning, is available in the machine_learning_report.ipynb file (or main.py).
