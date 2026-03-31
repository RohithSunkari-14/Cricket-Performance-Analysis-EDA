# Cricket-Performance-Analysis-EDA
Project Context :
I recently took on a project at Innomatics Research Labs to help a sports analytics company make sense of their historical batting data. The raw data was a bit of a mess—inconsistent formatting, missing values, and special characters—which made it impossible to run any real analysis.
My job was to move past the "dirty" data, clean it up using Python, and figure out who the most efficient players across different eras actually are.

What I Wanted to Solve : 
The goal wasn't just to make the data look pretty. I wanted to answer specific questions for the client like:
1.Who are the top 10 all-time run-scorers when you account for strike rates?
2.How does a long career impact a player's total efficiency?
3.Can we statistically separate "Aggressive" players from "Defensive" ones?
4.Which countries have the most consistent performers in the dataset?

The "Dirty Work" (Data Cleaning) :
This was the most time-consuming part of the project. I used Pandas to handle several issues :
1.Fixing the Player Column: I had to use string splitting and regex to separate the Player Names from their Country codes.
2.Cleaning High Scores: Many scores had a * (indicating Not Out), which turned the column into a string. I stripped those characters and converted the column to numeric so I could actually calculate averages.
3.Handling the 'Span': I split the career span into Start Year and End Year to calculate exactly how many years each player was active.
4.Missing Values: I filled or derived missing values in the Balls Faced (BF) and Strike Rate (SR) columns to keep the dataset complete.

Engineering New Metrics :
To get a better picture of performance, I created a few new columns :
1.Boundary Percentage: Calculated how much of a player's total runs came only from 4s and 6s.
2.Batting Efficiency: A custom metric (Runs / Innings) to see who makes the most of their time at the crease.
3.Career Longevity: Seeing if staying in the game longer actually leads to better performance or just higher totals.

What the Data Told Me :
I used Matplotlib and Seaborn to visualize the findings :
1.Average vs. Strike Rate: I built a scatter plot that clearly shows the trade-off between playing fast and playing safe.
2.Correlation Heatmap: This helped me see which stats (like Matches vs. Total Runs) are most closely linked.
3.Outlier Detection: Used boxplots to find those "legendary" players whose stats are so high they sit far away from the rest of the group.

Tech I Used :
1.Python (The backbone of the project)
2.Pandas & NumPy (For all the heavy lifting and cleaning)
3.Matplotlib & Seaborn (For the visual storytelling)

A Note of Gratitude :
This project was completed as part of my Data Science journey at Innomatics Research Labs. Huge thanks to my mentors for the guidance and the opportunity to work on real-world sports data...!
