# Cricket-Data-Analytics

### Dashboard Link : https://app.powerbi.com/links/wRS3ocSB45?ctid=610fd202-9529-4e97-adcc-43f743489e09&pbi_source=linkShare

## Problem Statement

This dashboard helps cricket analysts, selectors, and fans evaluate players more objectively. Instead of relying solely on batting averages or personal biases, this dashboard uses real performance metrics from the T20 World Cup 2022 to:

Compare and analyze players based on strike rate, boundary percentage, wickets, economy rate, and more.

Build a balanced playing XI based on real data.

Understand how player performances vary across different match stages.

With modern cricket becoming increasingly data-driven, this dashboard brings data storytelling to the game in an interactive, insightful way.



### Steps followed 

Step 1: Collected Data via Web Scraping 
- Used Bright Data to scrape player and match-level data from ESPNcricinfo. 

- Exported the scraped data in JSON format for further use.

Step 2: Cleaned & Structured Data using Python
- Loaded JSON into Python using the pandas library.

- Flattened nested structures into CSV format.

- Cleaned missing/null values, removed duplicates, and calculated custom metrics like:

        Strike Rate

        Boundary %

        Bowling Economy

        Economy

- Player Roles & Match Phases

Step 3: Created Calculated Columns & Measures in Power BI
Imported structured CSVs into Power BI.

- Built relationships using match_id, player_name, etc.

- Created DAX Measures like:

        Batting Average

        Boundary %

        Bowling Economy

- Player Role Classification

- Selection Flags for Top XI

Step 4: Designed Dashboard Layout
Used bar charts, KPI cards, tables, and slicers.

- Added filters for:

- Match Stage (Group, Semifinals, Final)

- Player Role (Opener, All-rounder, Specialist Bowler)

- Team

Step 5: Added Tooltips, Conditional Formatting & Dynamic Views
Tooltips display detailed match-wise stats.

- Conditional formatting highlights top performers.

- Each category (Openers, Anchors, Finishers, All-Rounders, Bowlers) got its own visual section.


# Snapshot of Dashboard (Power BI Service)

![dashboard_snapo](https://user-images.githubusercontent.com/102996550/174096257-11f1aae5-203d-44fc-bfca-25d37faf3237.jpg)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://user-images.githubusercontent.com/102996550/174074051-4f08287a-0568-4fdf-8ac9-6762e0d8fa94.jpg)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 129880

   Number of satisfied Customers (Male) = 28159 (21.68 %)

   Number of satisfied Customers (Female) = 28269 (21.76 %)

   Number of neutral/unsatisfied customers (Male) = 35822 (27.58 %)

   Number of neutral/unsatisfied customers (Female) = 37630 (28.97 %)


           thus, higher number of customers are neutral/unsatisfied.
           
### [2] Average Ratings

    a) Baggage Handling - 3.63/5
    b) Check-in Service - 3.31/5
    c) Cleanliness - 3.29/5
    d) Ease of online booking - 2.88/5
    e) Food & Drink - 3.21/5
    f) In-flight Entertainment - 3.36/5
    g) In-flight service - 3.64/5
    h) In-flight Wifi service - 2.81/5
    i) Leg room service - 3.37/5
    j) On-board service - 3.38/5
    k) Online boarding - 3.33/5
    l) Seat comfort - 3.44/5
    m) Departure & arrival convenience - 3.22/5
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  
  ### [3] Average Delay 
  
      a) Average delay in arrival(minutes) - 15.09
      b) Average delay in departure(minutes) - 14.71
Average delay will change if different visual filters will be applied.

 ### [4] Some other insights
 
 ### Class
 
 1.1) 47.87 % customers travelled by Business class.
 
 1.2) 44.89 % customers travelled by Economy class.
 
 1.3) 7.25 % customers travelled by Economy plus class.
 
         thus, maximum customers travelled by Business class.
 
 ### Age Group
 
 2.1)  21.69 % customers belong to '0-25' age group.
 
 2.2)  52.44 % customers belong to '25-50' age group.
 
 2.3)  25.57 % customers belong to '50-75' age group.
 
 2.4)  0.31 % customers belong to '75-100' age group.
 
         thus, maximum customers belong to '25-50' age group.
         
### Customer Type

3.1) 18.31 % customers have customer type 'First time'.

3.2) 81.69 % customers have customer type 'returning'.
       
       thus, more customers have customer type 'returning'.

### Type of travel

4.1) 69.06 % customers have travel type 'Business'.

4.2) 30.94 % customers have travel type 'Personal'.

        thus, more customers have travel type 'Business'.
