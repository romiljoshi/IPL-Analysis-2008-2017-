# 🏏 IPL Data Analysis (2008–2017) — Power BI Project

## 📘 Overview
This project presents a comprehensive *data analysis and visualization of the Indian Premier League (IPL)* from *2008 to 2017* using *Power BI*.  
The goal is to explore patterns and performance insights of teams, players, and matches through interactive dashboards and DAX-based measures.

---

## 🎯 Objectives
- Analyze IPL data at both *match* and *delivery* levels.
- Identify *top-performing batsmen, bowlers, and teams* across seasons.
- Visualize trends such as:
  - Win percentage after winning the toss  
  - Most sixes and fours by players  
  - Bowlers with most wickets (overall and per season)  
  - Highest and lowest individual scores per season  
  - Team performance by venue and season

---

## 🧩 Dataset Details
- *Datasets Used:*  
  - matches.csv → Match-level data (teams, results, venue, toss, etc.)  
  - deliveries.csv → Ball-by-ball data (runs, wickets, extras, players involved)
- *Data Source:* Public IPL Dataset (Kaggle / Open-source)
- *Duration Covered:* 2008–2017  
- *Size:* ~600 matches and over 150,000 deliveries

---

## 🛠 Tools & Technologies
| Category | Tools / Languages |
|-----------|-------------------|
| Data Visualization | Power BI Desktop |
| Data Transformation | Power Query Editor |
| Data Modeling | Star Schema Design |
| Calculations | DAX (Data Analysis Expressions) |
| Source Control | Git & GitHub |
| Dataset Format | CSV |

---

## 🧮 Data Modeling
A *Star Schema* model was used for optimal performance and clear relationships.

*Fact Table:*
- deliveries (ball-by-ball data)

*Dimension Tables:*
- matches  
- Teams  
- Players  
- Venues  
- Seasons

*Key Relationships:*
- matches[id] → deliveries[match_id] (1-to-many, active)  
- matches[team1] / matches[team2] → Teams[Team_Name] (active)  
- matches[season] → Seasons[Season] (active)  
- deliveries[batting_team] / deliveries[bowling_team] → Teams[Team_Name] (inactive, used with USERELATIONSHIP)

---

## 📊 Dashboards & Insights

### 🏠 Overview Page
- Total Matches, Runs, Wickets  
- Win % after Toss  
- Top Teams by Win Rate  

### 🏏 Batting Analysis
- Top 10 Batsmen by Runs, Sixes, and Fours  
- Highest Individual Scores per Season  
- Boundary Contribution Percentage  

### 🎯 Bowling Analysis
- Top 10 Bowlers by Wickets  
- Economy Rate & Strike Rate comparison  
- Season-wise Wicket Leaders  

### 🧠 Team Insights
- Win/Loss Trends per Season  
- Performance by Venue  
- Toss Decision Impact  

### 👤 Player Profile (Optional)
- Individual player stats with photo URLs  
- Key performance metrics and highlights

---

### 🎨 Visualization Highlights

- Interactive slicers for Season, Team, and Venue

- KPI Cards showing overall stats

- Bar charts for Top Batsmen & Bowlers

- Donut charts for Toss vs Win %

- Conditional formatting for economy and strike rates

- Drill-through pages for detailed player insights



---

### 💡 Key Insights

- Teams winning the toss had a ~52% chance of winning the match.

- Chris Gayle dominated with the highest number of sixes (2008–2017).

- Bhuvneshwar Kumar and Lasith Malinga were consistent top wicket takers.

- High-scoring venues include Chinnaswamy Stadium and Eden Gardens.

- In early IPL seasons, batting first often led to a higher win probability.




