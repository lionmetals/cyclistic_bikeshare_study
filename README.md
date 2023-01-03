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

Step 6: 
