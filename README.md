**1. Problem Statement**<br/>
Airfare prices fluctuate due to a variety of dynamic factors like travel dates, airline carriers, stops, duration, and source/destination cities. The aim of this project is to build a machine learning model that accurately predicts the price of flight tickets based on these variables, allowing users to plan their journeys efficiently and affordably.

**2.  Dataset Overview**<br/>
Source: Kaggle – Flight Fare Prediction Dataset

Size: ~10,000 rows

_Target Variable: Price_
_Key Features:_<br/>
Feature	Description <br/>
Airline	Name of the airline<br/>
Date_of_Journey	Date of the journey <br/>
Source	City from where the flight departs<br/>
Destination	City where the flight lands<br/>
Route	Flight route<br/>
Dep_Time	Departure time<br/>
Arrival_Time	Arrival time<br/>
Duration	Total travel time<br/>
Total_Stops	Number of stops in the journey<br/>
Additional_Info	Misc info about flight (e.g., no info)<br/>
Price	Flight ticket price (Target variable)<br/>

**3.  Exploratory Data Analysis (EDA)**<br/>
Key insights from the data:<br/>

Airlines like Jet Airways have higher average prices.<br/>

Non-stop flights are more expensive than flights with stops.<br/>

Flight prices are influenced by duration and departure time.<br/>

No strong correlation with Additional_Info.<br/>

Data Cleaning Done:<br/>

Removed missing values<br/>

Parsed and split date/time fields<br/>

Cleaned inconsistent duration formats<br/>

**4.  Feature Engineering**<br/>
Extracted:<br/>

Journey_Day, Journey_Month from Date_of_Journey<br/>

Dep_Hour, Dep_Min from Dep_Time<br/>

Arrival_Hour, Arrival_Min from Arrival_Time<br/>

Converted Duration into numeric hours and minutes<br/>

Used Label Encoding and One-Hot Encoding for categorical columns:<br/>

Airline, Source, Destination, Total_Stops<br/>

Final feature set included ~30 columns after transformation.<br/>

**5.  Model Building & Evaluation**<br/>
Algorithms Tested:<br/>
a. Linear Regression<br/>
b. Decision Tree Regressor<br/>
c. Random Forest Regressor<br/>
d. Redge Regression<br/>
e. Lasso Regression<br/>
f. GradientBoosting Regressor<br/>
g. ExtremeGradientBoosting Regressor<br/>
h. AdaBoosting Regressor	<br/>

_Evaluation Metrics:_<br/>
MAE (Mean Absolute Error)<br/>

RMSE (Root Mean Squared Error)<br/>

R² Score<br/>

_Best Model: ExtremeGradientBoosting Regressor_<br/>


**6.  Deployment**<br/>
Developed a simple Flask web app<br/>

Inputs: User fills in flight details<br/>

Output: Predicted flight fare shown in real-time<br/>

**7. Business Impact**<br/>
Enables budget-friendly travel planning<br/>

Can be used by OTAs like MakeMyTrip, Cleartrip for pricing strategies<br/>

Helps airlines optimize dynamic pricing models<br/>
