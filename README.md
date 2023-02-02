
#  Hotel Bookings Analysis

## Objective
We are provided with a hotel bookings dataset. 

Out main objective is perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.

## Business Problem Overview
Have you ever pondered the ideal season of the year to reserve a hotel room? Or the ideal duration of stay to obtain the most affordable daily rate? What to do if you wanted to forecast whether a hotel will unreasonably receive a lot of unique requests? his lodging You can better investigate those questions by using a dataset! This data collection comprises booking information for a resort hotel and a city hotel, as well as information about the date the reservation was made. duration of stay. among other variables, the number of adults, kids, and/or babies, and the quantity of parking places. The deta no longer contains any information that might be used to individually identify you. Investigate and evaluate the data to find crucial elements.

## Business Objective
To find best time of year to book a hotel room

## Dataset
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

```
- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.
```
- Total number of rows in data: 119390
- Total number of columns: 32

## Data Cleaning and Feature Engineering
### (1) Removing Duplicate rows
All duplicate rows were dropped.
### (2) Handling null values
- Null values in columns `company` and `agent` were replaced by 0.
- Null values in column `country` were replaced by 'others'.
- Null values in column `children` were replaced by the mean of the column.
  
### (3) Converting columns to appropriate data types
- Changed data type of `children`, `company`, `agent` to int type.
- Changed data type of `reservation_status_date` to date type.
### (4) Removing outliers
- One outlier was found in the `adr` column. Simply dropped it.

## Exploratory Data Analysis

Performed EDA and tried answering the following questions:

Q1) Which countries have the most passengers.

Q2) Find hotel who have the maximum ADR (Average Daily Rate)

Q3) Find the Average of total ADRs

Q4) Define the average of number of nights stayed.

Q5) Define the hotel and country of people who had 5 special requests

Q6) Define the people country whom reserved a hotel with most number of babies and children

```

Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:

  - Bar Plot.
  - Histogram.
  - Scatter Plot.
  - Pie Chart.
  - Line Plot.
  - Heatmap.

```
## Conclusion
```
(1) There are 66.4% city Hotels and 33.6% Resort Hotels.
(2) In month of january and february lead time is low.
(3) Contract ' of Customer Types has the most stay duration.
(4) City Hotel has the most visitors.
(5) The people from PRT country reserved a hotel with most number of babies and children.
(6) PRT Country has most Passengers.
(7) City Hotel has the maximum ADR (Average Daily Rate) which is 5400.0
(8) Agent no. 9 has made most no. of bookings.
(9) Most demanded room type is A, but better adr rooms are of type H, G and C also. Hotels should increase the no. of room types A and H to maximise revenue.
```
## Challenges
```
(1) There was a lot of duplicate data.
(2) Choosing appropriate visualization techniques to use was difficult.
(3) A lot of null values were there in the dataset.

https://kumarmhaske.github.io/EDA_Hotel_Bookings_Data_Analysis/  Tap here for a quick preview.
