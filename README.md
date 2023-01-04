# cyclistic_bikeshare_study
<h1>How Does a Bike-Share Navigate Speedy Success?</h1>

<h2>Scenario:</h2>
You are a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations

<h2>Business Task:</h2>
How do annual members and casual riders use Cyclistic bikes differently?

<h2> Programming Tool Used:</h2>
<b>RStudio</b>: Great tool for analyzing and visualizing large data-sets 

<h2>Prepare and Process Data:</h2>
<ul>
  <li> Data Source: <a href="https://divvy-tripdata.s3.amazonaws.com/index.html"> Divvy Trip Data </a> </li>
  <li>Data from previous 12 months (2021-12 to 2022-11)</li>
  <li>Data Includes: User IDs, user type, bike type, start & end details (times, positions, station names & IDs)</li>
  <li>Copied data set into separate folder called "data" on my desktop</li>
</ul>

<h2> RStudio </h2>
  <h3> Step 1: Importing Data into R-Studio</h3>
<img width="513" alt="Screenshot 2023-01-03 at 5 26 42 PM" src="https://user-images.githubusercontent.com/114360846/210617334-ceabf5bf-070f-42a8-815a-eb49cd0434b4.png">


  <h3>Step 2: Combining all files into a single DataFrame</h3>
<li>Combined all files into a Single Data frame named "df"</li>
<br><img width="500" alt="Screenshot 2023-01-04 at 9 50 19 AM" src="https://user-images.githubusercontent.com/114360846/210618098-4ebdb7b6-f1aa-4b7f-a94c-22d5d5b95773.png">

  <h3>Step 3: Creating new column:ride_length</h3>
<li>Calculated duration of each ride by subtracting start and end times</li>
<br><img width="440" alt="Screenshot 2023-01-04 at 9 53 23 AM" src="https://user-images.githubusercontent.com/114360846/210618651-3feeb3cd-b7e4-4db7-bea5-1cce2d3b9bf0.png">

  <h3>Step 4: Further Clean-Up and v2</h3>
<li>Making a second version of the data frame since I will be omitting rows with with a negative trip duration as well as any "docked_bikes" since these were taken out of circulation by Cyclistic. This decreased observations from 5733351 to 5552874</li>
<br><img width="600" alt="Screenshot 2023-01-04 at 9 57 27 AM" src="https://user-images.githubusercontent.com/114360846/210619311-e569788f-8ec9-48dd-ac40-7c63038d3b0f.png">

  <h3>Step 5: Adding Columns about Date for Easier Analysis</h3>
<img width="600" alt="Screenshot 2023-01-04 at 10 02 30 AM" src="https://user-images.githubusercontent.com/114360846/210620113-d8c47070-408d-47b0-94a1-813a147056f8.png"><br>
<br> New columns 
<br><img width="351" alt="Screenshot 2023-01-04 at 10 03 20 AM" src="https://user-images.githubusercontent.com/114360846/210620267-03dc5798-a853-49d5-ae87-875467173324.png">

  <h3>Step 6: Calculations</h3>
<b>Total number of rides and average duration by user type (member vs. casual)</b>
<ul>
<b>Input:</b>
<br><img width="381" alt="Screenshot 2023-01-04 at 10 13 36 AM" src="https://user-images.githubusercontent.com/114360846/210621871-2e3420f9-80af-4cfc-bf04-46b2928edb27.png">
<br>
<b>Output:</b>
<br><img width="354" alt="Screenshot 2023-01-04 at 10 22 24 AM" src="https://user-images.githubusercontent.com/114360846/210623338-ee716908-c0d7-40e2-8165-9aeab04529b0.png">
</ul>

<br>
<b>Total number of rides by bike type (classic vs electric) and user type (member vs casual)</b>
<ul>
<b>Input:</b>
<br><img width="332" alt="Screenshot 2023-01-04 at 10 26 13 AM" src="https://user-images.githubusercontent.com/114360846/210624003-8d5750f3-1d09-46be-8e49-f7f36b23da17.png">
<br><br>
<b>Output:</b>
<br><img width="332" alt="Screenshot 2023-01-04 at 10 26 40 AM" src="https://user-images.githubusercontent.com/114360846/210624091-05e53aa9-f2a7-406e-81be-45a2e66ce045.png">

</ul>

  <h3>Step 7: Making Graphs</h3>
<b>1) Total number of rides per day by user type</b>
<ul>
<b>Input:</b>
<br>
<img width="806" alt="Screenshot 2023-01-04 at 11 16 38 AM" src="https://user-images.githubusercontent.com/114360846/210632081-7bff0ed8-3412-4321-bc84-e3bcd3ed52fe.png">
<br>
<b>Output:</b>

![45ed3f87-579d-4a47-ab7f-4b8072243a0a](https://user-images.githubusercontent.com/114360846/210459581-4c24e7ed-ff13-4d32-a707-e4304fd5aa3f.png)
<br>
<b>Analysis:</b>
<ul>
<li>Greatest discrepancies during the <b>weekday</b> (Monday through Friday)</li>
<ul>
<li>Members take take approximately twice the number of rides as casuals do during this time</li>
</ul>
</ul>
</ul>


<b>2) Average duration of rides per day by user type</b>
<ul>
<b>Input:</b>
<br>
<img width="974" alt="Screenshot 2023-01-04 at 11 22 54 AM" src="https://user-images.githubusercontent.com/114360846/210633135-8d681b2e-c0af-4dcb-a3df-67db6fc9ed20.png">

<b>Output:</b>
<br>
![bc2ca5b1-3243-45d8-9e0a-7153ef717914](https://user-images.githubusercontent.com/114360846/210461691-6bfe77ac-9dba-44c3-91e1-c68fc918a9b8.png)

<b>Analysis:</b>
<ul>
<li>Casuals' average ride length is ~2x longer than members', regardless of the day</li>
</ul>
</ul>

<b>3) Bike-share usage by bike and user type</b>
<ul>
<b>Input:</b>
<br>
<img width="781" alt="Screenshot 2023-01-04 at 11 28 12 AM" src="https://user-images.githubusercontent.com/114360846/210634010-492ff091-99c0-4f4b-bc23-37ff2e3ee1ac.png">

<b>Output:</b>
<br>![cf373c6c-4b6b-4468-9db6-4baf85b2a119](https://user-images.githubusercontent.com/114360846/210459284-7b651e95-fdec-441b-8bc1-c504f10c6f4e.png)
<br>
<b>Analysis:</b>
<ul>
<li>Members use classic and electric bikes equally while casuals prefer electric bikes</li>
</ul>
</ul>

<h2>Recommendations</h2>
<b>Problem:</b> Not many casual users during the weekday
<br>
<b>Solution:</b> Run a cheaper, weekday only, membership program
<br>
<br>
<b>Problem:</b> Casual riders average duration is much longer (~2x) than members. This creates a slower "flow" of available bikes.
<br>
<b>Solution:</b> Offer time-sensitive passes that automatically upgrade to provide you the best fare (how bus passes work in Portland, Oregon). Example: First ride gives you an unlimited pass for first 2.5hrs. Then, if you need to purchase another pass after the 2.5hr window during the same day, you automatically get upgraded to an unlimited Day Pass (unlimited rides until 11:59pm that day). If you acquire more than a set number of Day Passes (i.e. 20), then you get automatically upgraded to a "Member" for the month. This will organically create more monthly pass holders since users will know that they will:
<br>
<br>
<ul>
<ul>
<b><li>Always get the best fair</li>
<li>Save more by riding more frequently</li>
<li>Not have to pay any upfront costs</li></b>
</ul>
</ul>
<br>
<br>

<b>Problem:</b> Members prefer classic bikes more than casual riders.
<br>
<b>Solution:</b> Offer more electric bikes as there might not be enough in circulation for the all of those who want it (would need further data for this analysis).
