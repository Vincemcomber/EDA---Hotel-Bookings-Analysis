# EDA---Hotel-Bookings-Analysis
 We are provided with a hotel bookings dataset.  Out main objective is perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.

Dataset
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

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

Total number of rows in data: 119390
Total number of columns: 32

Data Cleaning and Feature Engineering
(1) Removing Duplicate rows
All duplicate rows were dropped.

(2) Handling null values
Null values in columns company and agent were replaced by 0.
Null values in column country were replaced by 'others'.
Null values in column children were replaced by the mean of the column.

(3) Converting columns to appropriate data types
Changed data type of children, company, agent to int type.
Changed data type of reservation_status_date to date type.

(4) Removing outliers
One outlier was found in the adr column. Simply dropped it.

(5) Creating new columns
Created new column total_stay by adding stays_in_weekend_nights+stays_in_week_nights.
Created new column total_people by adding adults+children+babies.

Exploratory Data Analysis
Performed EDA and tried answering the following questions:

1. Univariate Analysis
While doing univariate analysis of given hotel booking dataset, we answered following questions:
(1) Which agent made most of bookings?
(2) Which room type is in most demand and which room type generates highest adr?
(3) From which country most of the customers are coming?
(4) What is the most preferred meal by customers?
(5) How long do people stay at the hotels?

2. Hotel wise Analysis
While doing hotel wise analysis of given hotel booking dataset, we answered following questions:
(1) What is the percentage of bookings in each hotels?
(2) Which hotel makes more revenue?
(3) Which hotel has higher lead-time?
(4) What is most preferred stay length in each hotel?
(5) For which hotel, does people have to wait longer to get a booking confirmed?
(6) Which hotel has higher booking cancellations rate?
(7) Which hotel have higher and how much customer-returning rate?

3. Distribution channel wise Analysis
While doing Distribution channel wise analysis of given hotel booking dataset, we answered following questions:
(1) Which is the most common channel for booking hotels?
(2) Which channel is mostly used for early booking of hotels?
(3) Which channel has longer average waiting time?
(4) Which distribution channel brings better revenue generating deals for hotels?

4. Booking cancellation Analysis
We analyze the following possible reasons for booking cancellations:
(1) Which significant distribution channel has highest cancellation percentage?
(2) Does a longer waiting period or longer lead-time causes the cancellation of bookings?
(3) Whether not getting allotted the same room type as demand is the main cause of cancellation for bookings?
(4) Does not alloting the same room as demanded affect adr?
(5) Which deposit_type have a majotity of bookings?

5. Time wise Analysis
While doing time wise analysis of given hotel booking dataset, we answered following questions:
(1) What are the busiest months for hotels?
(2) In which months hotels charges higher adr? / Which month results in high revenue?
(3) What is the trend of bookings within a month? / How does booking numbers and adr changes within a month?
(4) Which types of customers mostly make bookings?

6. Some important questions
Some other analysis are also done, which are as follows:
(1) What are the different reason for special requests?
(2) What is the optimal stay length for better deal for customers?
(3) How adr is affected by total staying period in hotels?


Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:
Bar Plot.
Histogram.
Scatter Plot.
Pie Chart.
Line Plot.
Heatmap.
Box Plot.

Conclusion
● Around 62% bookings are for City hotel and 38% bookings are for Resort hotel, therefore City Hotel is busier than Resort hotel. In addition, the overall adr of City hotel is slightly higher than Resort hotel.
● Mostly guests stay for less than 5 days in hotel and for longer stays, Resort hotel is preferred.
● Both hotels have significantly higher booking cancellation rates and very few guests less than 3 % return for another booking in City hotel. 5% guests return for stay in Resort hotel.
● Most of the guests came from European countries, with most number of guests coming from Portugal.
● Guests use different channels for making bookings out of which most preferred way is TA/TO.
● For hotels higher adr deals come via GDS channel, so hotels should increase their popularity on this channel.
● Almost 30% of bookings via TA/TO are cancelled.
● Almost 30% of City Hotel bookings and 24% of Resort hotel bookings got cancelled.
● Not getting same room as reserved, longer lead time and waiting time do not affect cancel-lation of bookings. Although different room allotment do lowers the adr.
● July-August are the most busiest and profitable months for both of hotels.
● Within a month, adr gradually increases as month ends, with small sudden rise on weekends.
● Couples are the most common guests for hotels; hence, hotels can plan services according to couples needs to increase revenue.
● More number of people in guests results in more number of special requests.
● Bookings made via complementary market segment and adults have on average high no. of special request.
● For customers, generally the longer stays (more than 15 days) can result in better deals in terms of low adr.

Challenges
(1) There was a lot of duplicate data.
(2) Data was present in wrong datatype format.
(3) Choosing appropriate visualization techniques to use was difficult.
(4) A lot of null values were there in the dataset.
