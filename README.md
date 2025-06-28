## Project Overview

This Power BI dashboard provides a comprehensive analysis of Uber trip data, offering insights into various aspects such as booking trends, financial performance, vehicle utilization, and location-based patterns. The goal of this project is to visualize key metrics and identify actionable trends that can inform business decisions.

## Data Sources

The dashboard utilizes data from two primary sources, structured as follows:

1.  **Trip Details Table:** Contains granular information about each individual trip.
    * `Trip ID`: Unique identifier for each trip.
    * `Pickup_Date`: Date the trip started.
    * `Pickup Time / Pickup Hour`: Time or hour the trip was picked up.
    * `Drop Off Time`: When the trip ended.
    * `Passenger_count`: Number of passengers on the trip.
    * `Payment_type`: Payment method (cash, card, etc.).
    * `PULocationID`: Pickup Location ID (links to Location Table).
    * `DOLocationID`: Drop-off Location ID (links to Location Table).
    * `Total_Trip_distance`: Trip distance in km or miles.
    * `fare_amount`: Fare charged for the trip.
    * `Surge Fee`: Any surge pricing amount applied.
    * `Vehicle`: Vehicle category (UberX, UberXL, etc).

2.  **Location Table:** Provides lookup details for location IDs.
    * `LocationID`: Unique ID for a location (numeric key).
    * `Location`: A friendly name for the location (e.g., “Times Square”).
    * `City`: The city name, if multiple cities are supported.

## Data Model & Relationships

The Power BI data model establishes relationships between the two tables:

* **Active Relationship:** `Trip Details[PULocationID]` connects to `Location[LocationID]`. This allows direct filtering and analysis based on the trip's starting point.
* **Inactive Relationship:** `Trip Details[DOLocationID]` connects to `Location[LocationID]`. Due to Power BI's limitation of only one active relationship between two tables, `LOOKUPVALUE` DAX function is used to dynamically retrieve the `Drop-off Location` name.

## Dashboard Pages

The dashboard is structured into three main pages for intuitive navigation:

### 1. Overview Analysis

This page provides a high-level summary of the entire dataset.

* **Key Performance Indicators (KPIs):** Displays total bookings, total booking value, average booking value, total trip distance, average trip distance, and average trip duration.
* **Booking Trends:** Visualizes total bookings by day to show daily fluctuations.
* **Payment Type Distribution:** A donut chart showing the breakdown of bookings by payment method (e.g., Uber Pay, Cash).
* **Trip Type Distribution:** A donut chart showing the split between Day and Night trips.
* **Location Insights:** Highlights the most frequent pickup and drop-off points, as well as the farthest recorded trip.
* **Vehicle Performance:** A table showing bookings, value, and distance by vehicle category (e.g., UberXL, UberX, Uber Black).
* **Location & Vehicle Preferences:** Bar charts illustrating total bookings by location and the most preferred vehicle types by location.

### 2. Time Analysis

This page focuses on temporal patterns and trends in trip data.

* **Booking Volume by Hour:** An area chart illustrating the distribution of bookings throughout a 24-hour cycle, revealing peak and off-peak hours.
* **Bookings by Hour & Day Heatmap:** A detailed grid showing booking density across hours of the day and days of the week, allowing for identification of specific busy periods.
* **Weekly Booking Trends:** A line chart displaying the total bookings for each day of the week, highlighting weekly patterns and busy days (e.g., weekends vs. weekdays).

### 3. Details

This page provides a granular, row-level view of individual trips.

* **Detailed Table:** Displays specific information for each trip, including: Trip ID, Pickup Date, Vehicle, Payment Type, Number of Passengers, Total Trip Distance, Total Booking Value, Pickup Location (friendly name), and Drop-off Location (friendly name).
* **Total Summary:** Provides a sum of total trips, total distance, and total booking value across all displayed records.

## Key Insights (Examples - **Customize these with your actual findings!**)

* **Peak Hours:** Trips generally peak between 3 PM and 6 PM.
* **Weekend Rush:** Saturdays and Sundays consistently show the highest booking volumes.
* **Payment Preferences:** The majority of users prefer `[e.g., Uber Pay]` over `[e.g., Cash]`.
* **Most Popular Vehicle:** `[e.g., UberX]` is the most frequently booked vehicle category.
* **High Traffic Areas:** `[e.g., Penn Station/Madison Sq West]` is a consistently high-volume pickup point.

## Technologies Used

* **Power BI Desktop:** For data modeling, transformation (Power Query), DAX calculations, and visualization.
* **DAX (Data Analysis Expressions):** For creating custom measures and calculated columns.

## Screenshots

### Overview Analysis
![Screenshot 2025-06-28 164334](https://github.com/user-attachments/assets/fe8fe8a8-2746-46a3-a650-96eacf72299a)


### Time Analysis
![Screenshot 2025-06-28 164354](https://github.com/user-attachments/assets/fde9ceb3-2f68-4be5-848d-02a7e4295d24)


### Details
![Screenshot 2025-06-28 164407](https://github.com/user-attachments/assets/7dce6e54-bd29-4d13-b502-156d9ac6920c)


## Contact

Feel free to connect with me for any questions or collaborations:

* **[Your Name/Username]** Vijayasaravanan C
* **LinkedIn:** [[LinkedIn]](https://www.linkedin.com/in/vijayasaravanan-c/)
* **GitHub:** [[GitHub]](https://github.com/vijayasaravana?tab=repositories)

---
