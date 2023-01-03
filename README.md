# cyclistic_bikeshare_study
How Does a Bike-Share Navigate Speedy Success? 

Scenario: 
You are a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations


Business Task:
How do annual members and casual riders use Cyclistic bikes differently?

Prepare and Process Data:
-Data Source: Divvy trip data (https://divvy-tripdata.s3.amazonaws.com/index.html)
-Data from previous 12 months: 2021-12 to 2022-11
-Data Includes: User IDs, user type, bike type, start & end details (times, positions, station names & IDs)
-Copied data set into separate folder called "data" on my desktop


Tool Used:
-Rstudio: Great tool for analyzing and visualizing large data-sets

Step 1: Importing Data into R-Studio
Uploaded files using "readr" package
![Screenshot 2023-01-03 at 1 38 16 PM](https://user-images.githubusercontent.com/114360846/210445546-fca6ea99-e6dc-4b8f-aabe-603f2863f777.png)


Step 2: Combining all files into a single DataFrame
-Combined all files into a Single Data frame named "df"
![Screenshot 2023-01-03 at 1 39 24 PM](https://user-images.githubusercontent.com/114360846/210445691-da16ad95-aa57-4dfd-9ed2-1fafd9a1a0cd.png)

Step 3: Created new column:ride_length
![Screenshot 2023-01-03 at 2 07 40 PM](https://user-images.githubusercontent.com/114360846/210449303-fe171ce7-b95c-42ee-a43d-452fa571f0a9.png)

Step 4: Further Clean-Up and v2
-Various trips where ride_length returns a negative duration. These entries were omitted from the data_frame.
-The rideable_type "docked_bike" designates bikes that were taken out of circulation by Cyclistic to assess for quality control
-Decreased from 5733351 to 5552874 observations
![Screenshot 2023-01-03 at 2 24 20 PM](https://user-images.githubusercontent.com/114360846/210451330-29ce7149-44f8-4daf-9f90-8d6a8c973219.png)

Step 5: Add Data
![Screenshot 2023-01-03 at 2 19 04 PM](https://user-images.githubusercontent.com/114360846/210450653-69e9206d-fa87-4f23-96e2-f9f38fb51c00.png)

Step 6: Analysis
Input:
![Screenshot 2023-01-03 at 2 31 11 PM](https://user-images.githubusercontent.com/114360846/210452135-319ec348-d0e9-4940-b07f-d447378b603f.png)

Output:
![Screenshot 2023-01-03 at 2 30 54 PM](https://user-images.githubusercontent.com/114360846/210452105-18282c71-22c9-44a0-9151-cd4942678fbe.png)

Input:
![Screenshot 2023-01-03 at 2 32 03 PM](https://user-images.githubusercontent.com/114360846/210452226-45d9b958-db62-4181-a18a-90a3fad45dc5.png)
Output:
![Screenshot 2023-01-03 at 2 32 19 PM](https://user-images.githubusercontent.com/114360846/210452259-a525a285-6c96-4a0f-811c-2941bb1bcd0f.png)


Step 7: Making Graphs:
Number of Rides by Day of Week and User Type
Input:
![Screenshot 2023-01-03 at 3 43 31 PM](https://user-images.githubusercontent.com/114360846/210459541-e0ba01fb-d00e-4d39-814b-c23ad5cec26e.png)

Output
![45ed3f87-579d-4a47-ab7f-4b8072243a0a](https://user-images.githubusercontent.com/114360846/210459581-4c24e7ed-ff13-4d32-a707-e4304fd5aa3f.png)

Analysis:
-Greatest discrepancies during the weekday (Monday through Friday)
  -Members take take approximately twice the number of rides as casuals do during this time

Average Duration 
Input:
![Screenshot 2023-01-03 at 3 46 35 PM](https://user-images.githubusercontent.com/114360846/210459839-e09cdd84-6bbf-4c44-992c-12a405a9c874.png)

Output:
![b06356fe-33f5-4f4f-9f61-53db2659feba](https://user-images.githubusercontent.com/114360846/210459913-8dfb6ddb-8769-41fd-887f-a5ed0dcf1808.png)

Analysis:
-Casuals ride for a longer duration, regardless of the day

Bike Type vs. User Type
Input:
![Screenshot 2023-01-03 at 3 39 44 PM](https://user-images.githubusercontent.com/114360846/210459199-4b93df65-9cd2-4a36-bfb7-6a04c4bffe1c.png)

Output:
![cf373c6c-4b6b-4468-9db6-4baf85b2a119](https://user-images.githubusercontent.com/114360846/210459284-7b651e95-fdec-441b-8bc1-c504f10c6f4e.png)


Recommendations
-
