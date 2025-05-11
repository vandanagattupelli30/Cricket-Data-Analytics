# Airlines-Dashboard

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


![final_11](https://github.com/vandanagattupelli30/Cricket-Data-Analytics/blob/main/final%2011.png)


![power_hitters](https://github.com/vandanagattupelli30/Cricket-Data-Analytics/blob/main/powerHitters.png)


![anchors](https://github.com/vandanagattupelli30/Cricket-Data-Analytics/blob/main/anchors.png)


![finishers](https://github.com/vandanagattupelli30/Cricket-Data-Analytics/blob/main/finishers.png)


![specialist_fast_bowlers](https://github.com/vandanagattupelli30/Cricket-Data-Analytics/blob/main/spec_fast_bowlers.png)

# Insights

### [1] Player Performance
Jos Buttler and Rilee Rossouw dominated as explosive openers.

Suryakumar Yadav and Shadab Khan stood out as reliable middle-order contributors.

Sam Curran and Anrich Nortje led the bowling charts with low economy and high wickets.

### [2] Key Metrics
Strike Rate & Boundary % revealed aggressive batting potential.

Bowling Economy & Dot Ball % identified control bowlers.

All-Rounder Efficiency was used to evaluate dual-role players.

### [3] Team Trends
Players from England, India, and South Africa dominated several charts.

Insights revealed how stage-wise performance changed player rankings

 
 # DAX Expressions Used
    Strike Rate = DIVIDE([Total Runs], [Total Balls Faced], 0) * 100

    Boundary % = DIVIDE(SUM(fact_batting_summary[boundary runs]), [Total Runs], 0)

    Economy Rate = DIVIDE([Runs Conceded], ([Balls Bowled]/6), 0)

# Data Sources
- Match & Player Data: ESPNcricinfo

- Scraping Tool: Bright Data

- Transformation: Python (Pandas)

- Visualization: Microsoft Power BI

# Some Challenges Faced

- Name mismatches across data sets (e.g. abbreviations, special characters).

- Missing data in rain-affected or shortened matches (handled using fallback logic).

- Match phase identification (solved using logic columns in Power BI).

# Final Output
A fully interactive Power BI dashboard that:

Helps pick the Best XI based on actual stats.

Allows dynamic filtering by team, match stage, and player type.

Offers data-driven storytelling for cricket professionals and enthusiasts.

# Future Scope
- Integrate with live APIs for real-time analytics.

- Add ML-based predictions (e.g., winning probability, fantasy points).

- Host on cloud services for broader accessibility.

- Make it mobile-responsive for tablets and smartphones.

# References
- Codebasics YouTube Channel
- Power BI official Documentation
- Pandas Documentation
