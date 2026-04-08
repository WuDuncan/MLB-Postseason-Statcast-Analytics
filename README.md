# MLB-Postseason-Statcast-Analytics
# ⚾ 2025 MLB Postseason Statcast Analysis: Pitch Velocity and Batted Ball Profiles

## 📌 Project Objective
With the rise of the "Fly Ball Revolution" and advanced analytics, understanding the impact of Exit Velocity and Launch Angle on the game is crucial. Utilizing the 2025 MLB Postseason Statcast Pitch-by-Pitch data, this project aims to analyze:
1. Pitch velocity distributions and pitch type characteristics in the high-leverage environment of the postseason.
2. The batter's "Sweet Spot" distribution, exploring the data conditions that generate highly destructive (hard-hit) batted balls.

## 🛠️ Tech Stack
* **Language:** R
* **Core Packages:** `tidyverse` (Data Cleaning & Engineering), `ggplot2` (Data Visualization), `psych` (Descriptive Statistics), `lubridate` (Date/Time Parsing)
* **Statistical Methods:** Descriptive Statistics, One-Sample t-test, Proportion Test

## 📊 Key Insights & Visualizations

### 1. Finding the Optimal Contact: Exit Velocity vs. Launch Angle (The Sweet Spot)
*(Note: Insert your generated Figure 5 image here)*
* **Insight:** By cross-referencing the scatter plot, we can clearly see that when the Launch Angle is between **8 and 32 degrees**, and the Exit Velocity exceeds **95 mph (Hard Hit)**, it is most likely to result in damaging extra-base hits. This provides a clear quantitative target for hitting coaches when adjusting players' swing paths.

### 2. Pitch Velocity Analysis and Hypothesis Testing
*(Note: Insert your generated Test 1 plot here)*
* **Insight:** Postseason Mean Velocity Test. We conducted a One-Sample t-test to determine if the overall postseason average pitch speed significantly differed from 90.5 mph. Additionally, we compared the velocity distributions of the top 8 most frequent pitch types using boxplots, helping us understand the speed tiers of different pitches in game situations.

## 📂 Data Source & Methodology
* **Dataset:** 2025 MLB Statcast Postseason Pitch-by-Pitch Data.
* **Data Engineering:** * Removed deprecated or unnecessary columns such as `spin_dir` and `umpire` to optimize computation.
  * Imputed missing values for baserunner status (converted NAs to 0/1) and batting event outcomes.
  * Filtered for `type == "X"` (batted balls put into play) to conduct targeted hit quality analysis.
