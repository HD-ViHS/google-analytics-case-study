# Google Analytics Case Study

## Ask
Cyclistic wants to know the differences between members and casual riders in order to learn how to convert casual riders into members.

## Prepare
The data sources used were provided from Divvy under their Data License agreement. They describe trip data (as listed below) for Q1 (January 1st to March 31st) of 2019 and 2020. The files are too big to upload so I have provided a summary of the raw data as well as modifications made to the data. These modifications can also be found in the included R script.

### Divvy_Trips_2019_Q1
Columns
* trip_id (id # for a single bike trip; integer)
* start_time (what date and time did the trip start?; datetime)
* end_time (what date and time did the trip finish?; datetime)
* bikeid (id # for the bike which made the trip; integer)
* tripduration (how long was the trip in seconds?; integer)
* from_station_id (id # of the station the trip started at; integer)
* from_station_name (name of the station the trip started at, usually an intersection ot two streets; string)
* to_station_id (id # of the station the trip ended at; integer)
* to_station_name (name of the station the trip ended at, usually an intersection ot two streets; string)
* usertype (was the user a customer or subscriber; boolean)
* gender (gender of rider, Male, Female, or N/A; string)
* birthyear (birth year of rider; integer)
Modified Cols
* ride_length (how long was the ride as a time; duration)
* day_of_week (day of the week bike ride occurred; 1=Sunday, 7=Saturday)

### Divvy_Trips_2020_Q1
Columns
* ride_id (id # for a single bike trip; integer)
* rideable_type (type of bike the ride was taken on; string)
* started_at (what date and time did the trip start?; datetime)
* ended_at (what date and time did the trip finish?; datetime)
* start_station_name (name of the station the trip started at, usually an intersection ot two streets; string)
* start_station_id (id # of the station the trip started at; integer)
* end_station_name (name of the station the trip ended at, usually an intersection ot two streets; string)
* end_station_id (id # of the station the trip ended at; integer)
* start_lat (GPS latitude of the starting station; decimal)
* start_lng (GPS longitude of the starting station; decimal)
* end_lat (GPS latitude of the destination station; decimal)
* end_lng (GPS longitude of the destination station; decimal)
* member_casual (was the rider a subscriber (member) or a casual rider; boolean)
Modified Cols
* ride_length (how long was the ride as a time; duration)
* day_of_week (day of the week bike ride occurred; 1=Sunday, 7=Saturday)


## Analyze
Analysis shows that while members tend to take much shorter rides when compared to casual riders, they also tend to take more rides. Additionally, members take more rides on the weekdays than weekends, most likely due to biking as a form of transportation to and from work as compared to leisure. To summarize, member bikers tend to take far more and far shorter weekday rides, while casual bikers tend to take far fewer longer rides, peaking on the weekends.

## Share
![Ride Count by Day of Week](https://github.com/user-attachments/assets/27a29f24-d3b4-41ca-9c9d-ec99cdabf9e2)
## Act
I reccommend the following actions as methods to convert casual bikers to member bikers:
1. Place more Cyclistic stations in residential neighborhoods so to allow more people to become commuting bikers, who are far more likely to be members.
2. Lower bike prices on weekdays to encourage weekday riding, which can encourage casual riders to become regular commuting riders, who are more likely to become members.
3. Create a price model which charges based on ride length instead of a per-month or a per-use model. This encourages the type of riding member riders tend to exhibit: a higher volume of shorter rides.
