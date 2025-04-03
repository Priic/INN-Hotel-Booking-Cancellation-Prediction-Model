# INN-Hotel-Booking-Cancellation-Prediction-Model

## Context

A significant number of `hotel bookings` are called-off due to `cancellations or no-shows`. The typical reasons for cancellations include change of plans, scheduling conflicts, etc. This is often made easier by the option to do so free of charge or preferably at a low cost which is beneficial to hotel guests but it is a less desirable and possibly revenue-diminishing factor for hotels to deal with. Such losses are particularly high on last-minute cancellations.
  
**`INN Hotels Group`** has a chain of hotels in Portugal who are facing problems with the **`high number of booking cancellations`** due to various factors. 
These cancellations are impacting the hotel on various fronts -like `Loss of resources (revenue)` when it cannot resell the room, `Additional costs for advertisement/publicity/commisions` through different distribution channels to help sell these rooms, `lowering room prices at the last minute`, resulting in reducing the profit margin and `unnecessary works for hotel staff` for making arrangements for guests.

The `dataset` we have analyzed here consist of **`approx 38k hotel booking details of the customers`**. They contains informations about the **`booking details for the year(2017- 2018)`**. It include details on `guest counts (adult and children), guest arrival month and date, number of week and weekend nights` it's booked for, `how much in advance` it's booked. Do the guest have any `special meal plan` ,`car space or special request requirements?` what `kind of room is booked`. is the customer a `repeating or new customers`.

## Objective
The increasing number of cancellations calls for a Machine Learning based solution that can help in predicting which booking is likely to be canceled. The main idea here is to analyze the data provided to find which factors have a high influence on booking cancellations and then **`build a predictive model`** that can **`predict which booking is going to be canceled in advance`**, and help in formulating profitable policies for cancellations and refunds.

## Model Building Approach

As a Data Scientist,
1. I explored the dataset to understand its `shape, size, data types, missing values, duplicates, and statistical summary`.
2. Conducted **`Exploratory Data Analysis (EDA)`** to identify key factors affecting cancellations.
3. Data Preprocessing: Cleaned and processed data by `handling missing values, outliers, and feature scaling `to ensure high-quality input for model training.
4. `Model Building:` Built **`Logistic Regression and Decision Tree classification models`**, addressing multicollinearity and applying **`pruning techniques`** for improved performance.
5. Model Evaluation: Optimized the decision threshold `using AUC-ROC`, achieving an `F1 score of 0.80,` boosting revenue by 10% and enhancing customer retention.
6. Provided `actionable insights to reduce cancellations`, identifying key predictors like `lead time, market segment, and room price`.
   
## Data Description
The data contains the different attributes of customers' booking details. The detailed data dictionary is given below.

**Data Dictionary**

* `Booking_ID:` unique identifier of each booking
* `no_of_adults:` Number of adults
* `no_of_children:` Number of Children
* `no_of_weekend_nights:` Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel
* `no_of_week_nights:` Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel
* `type_of_meal_plan:` Type of meal plan booked by the customer:
    * Not Selected – No meal plan selected
    * Meal Plan 1 – Breakfast
    * Meal Plan 2 – Half board (breakfast and one other meal)
    * Meal Plan 3 – Full board (breakfast, lunch, and dinner)
* `required_car_parking_space:` Does the customer require a car parking space? (0 - No, 1- Yes)
* `room_type_reserved:` Type of room reserved by the customer. The values are ciphered (encoded) by INN Hotels.
* `lead_time:` Number of days between the date of booking and the arrival date
* `arrival_year:` Year of arrival date
* `arrival_month:` Month of arrival date
* `arrival_date:` Date of the month
* `market_segment_type:` Market segment designation.
* `repeated_guest:` Is the customer a repeated guest? (0 - No, 1- Yes)
* `no_of_previous_cancellations:` Number of previous bookings that were canceled by the customer prior to the current booking
* `no_of_previous_bookings_not_canceled:` Number of previous bookings not canceled by the customer prior to the current booking
  
* `avg_price_per_room:` Average price per day of the reservation; prices of the rooms are dynamic. (in euros)
* `no_of_special_requests:` Total number of special requests made by the customer (e.g. high floor, view from the room, etc)
* `booking_status:` Flag indicating if the booking was canceled or not.
  
