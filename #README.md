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

#### Setting up environment
+ Create a database to host our data.
+ Create table to import data from txt files.
+ Load data into the created table.
  



