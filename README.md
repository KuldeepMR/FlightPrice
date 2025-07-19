1. 🎯 Problem Statement
Airfare prices fluctuate due to a variety of dynamic factors like travel dates, airline carriers, stops, duration, and source/destination cities. The aim of this project is to build a machine learning model that accurately predicts the price of flight tickets based on these variables, allowing users to plan their journeys efficiently and affordably.

2. 📊 Dataset Overview
Source: Kaggle – Flight Fare Prediction Dataset

Size: ~10,000 rows

Target Variable: Price

Key Features:
Feature	Description
Airline	Name of the airline
Date_of_Journey	Date of the journey
Source	City from where the flight departs
Destination	City where the flight lands
Route	Flight route
Dep_Time	Departure time
Arrival_Time	Arrival time
Duration	Total travel time
Total_Stops	Number of stops in the journey
Additional_Info	Misc info about flight (e.g., no info)
Price	Flight ticket price (Target variable)

3. 📈 Exploratory Data Analysis (EDA)
Key insights from the data:

Airlines like Jet Airways have higher average prices.

Non-stop flights are more expensive than flights with stops.

Flight prices are influenced by duration and departure time.

No strong correlation with Additional_Info.

Data Cleaning Done:

Removed missing values

Parsed and split date/time fields

Cleaned inconsistent duration formats

4. 🛠 Feature Engineering
Extracted:

Journey_Day, Journey_Month from Date_of_Journey

Dep_Hour, Dep_Min from Dep_Time

Arrival_Hour, Arrival_Min from Arrival_Time

Converted Duration into numeric hours and minutes

Used Label Encoding and One-Hot Encoding for categorical columns:

Airline, Source, Destination, Total_Stops

Final feature set included ~30 columns after transformation.

5. 🧠 Model Building & Evaluation
Algorithms Tested:
Linear Regression

Decision Tree Regressor

Random Forest Regressor

XGBoost Regressor

Evaluation Metrics:
MAE (Mean Absolute Error)

RMSE (Root Mean Squared Error)

R² Score

🔥 Best Model: Random Forest Regressor
Model	R² Score	RMSE
Linear Regression	0.61	~4200
Decision Tree	0.85	~2500
Random Forest	0.91	1900
XGBoost	0.89	~2000

6. 🖥 Deployment
Developed a simple Flask web app

Inputs: User fills in flight details

Output: Predicted flight fare shown in real-time
