<h1> Cyclistic Bike Share Case Study </h1> 

<h2>Google Data Analytics Capstone Project</h2>

### 📖 Overview 
In this project, I take on the role of a Data Analyst at Cyclistic, a bike-share company based in Chicago launched in 2016. The program has since expanded to 5,824 GPS-tracked bicycles and 692 docking stations across Chicago. Riders can unlock bikes at one station and return them to any other station in the system.

Cyclistic’s marketing strategy has focused on building brand awareness and targeting broad consumer groups, supported by flexible pricing plans: single-ride passes, full-day passes, and annual memberships. Casual riders purchase single-ride or full-day passes, while annual members subscribe to long-term plans.

Financial analysis shows that annual members are significantly more profitable than casual riders. While pricing flexibility has attracted a wide customer base, Cyclistic’s future growth depends on increasing annual memberships.

Rather than targeting entirely new customers, Moreno, the marketing director, sees an opportunity to convert casual riders into annual members. Casual riders already know and use Cyclistic’s services, making them ideal candidates for conversion.

### ✏️ Project Overview

The goal of this analysis is to help Cyclistic's marketing team understand the differences between casual riders and annual members. The director of marketing believes that increasing the number of annual memberships is key to Cyclistic’s future success, so identifying how these two groups use the service differently is critical.

### ✅ Business task
Analyze historical trip data to identify behavioral differences between casual riders and annual members, providing actionable insights to guide Cyclistic's marketing strategies and increase the number of annual memberships.

### ✅ Stakeholders:
+ Marketing Team;
+ Marketing Analytics Team;
+ Executive Team.


### ✅ Prepare

To support this analysis, historical trip data for the year 2023 was provided by Motivate International Inc. under their license agreement.
For each month of trip data, a ZIP file was provided. 

During this phase of the data analysis, the following steps were performed:

+ Download ZIP folders from the web repository through this link <https://divvy-tripdata.s3.amazonaws.com/index.html>. 
+ Extract the CSV files from the ZIP folders, storing them appropriately.
+ Transform text columns within each CSV file to ensure consistency.
+ Convert the data type of the started_at and ended_at columns after analysis:
    Previous format: dd/mm/yyyy hh:mm
    Converted format: YYYY-MM-DD HH:MM:SS
+ Save each CSV file as XLSX to create a working file version.
+ Save each XLSX file as a TXT file for importing into SQL.

### ✅ Process

Considering the size of data, MYSQL was the tool chosen for this phase. 
Steps performed are described below:

#### Environment SetUp
+ Create a database to host our data - database cyclistic_bike_share
+ Create table to import data from txt files - table Tripdata_2023.
+ Load data into the created table.

#### Cleaning Process
+ Check for null values
+ Creating a new table to work with - Tripdata_2023_v1. First table will be kept as backup.
+ Checking again for null values, this time on the new table.

Results as below:

<table>
    <tr>
        <td> NULL_or_empty_ride_id</td>
        <td> NULL_or_empty_rideable_type</td>
        <td> NULL_or_empty_started_at</td>
        <td> NULL_or_empty_endeded_at</td>
        <td> NULL_or_empty_start_station_name</td>
        <td> NULL_or_empty_start_station_id</td>
        <td> NULL_or_empty_end_station_name</td>
        <td> NULL_or_empty_end_station_id</td>
        <td> NULL_or_empty_start_lat</td>
        <td> NULL_or_empty_start_lng</td>
        <td>NULL_or_empty_end_lat</td>
        <td>NULL_or_empty_end_lng</td>
        <td>NULL_or_empty_end_member_casual</td>
    </tr>
    <tr>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>875716</td>
        <td>875848</td>
        <td>929202</td>
        <td>929343</td>
        <td>0</td>
        <td>0</td>
        <td>6990</td>
        <td>6990</td>
        <td>0</td>
    </tr> 
</table>


+ After analyzing the query results for null values, it was observed that approximately 900k null values were present in the columns start_station_name, start_station_id, end_station_name, and end_station_id. In a real-life situation, I would investigate the root cause of these null values and attempt to resolve the issue. However, for this case study, I decided to drop these columns and work with the remaining variables. I deemed this approach more beneficial than excluding all the affected rows, as doing so would result in a 20% reduction in data.
+ Additionally, approximately 7k null values were present in the columns end_lat and end_lng. These were also excluded from the analysis to ensure data consistency.

### ✅ Analyze & Data Visualization

### Total rides in 2023: 5.711.618
  
### Total rides in 2023 by type of rider

![image](https://github.com/user-attachments/assets/6f27a2b2-596a-45cd-b202-ea70062a28e9)

### Total rides in 2023 by type of rider & month
  
![image](https://github.com/user-attachments/assets/0d0972c1-5742-40da-a75a-2daeaacbf480)

### Total rides in 2023 by type of rider & day of week
![image](https://github.com/user-attachments/assets/7dc8035a-f479-46cc-9015-b4a45e7e6f4d)












