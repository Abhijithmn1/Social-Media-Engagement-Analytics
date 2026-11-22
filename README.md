Social Media Engagement Analytics (Module-End Assignment 5)
A complete exploratory data analysis (EDA) and statistical modeling project built in Python using Pandas, NumPy, Matplotlib, Seaborn, and Plotly to analyze engagement patterns across 5,000 social media posts.
📋 Project OverviewDataset: social_media_engagement_5000.csv ($5,000$ rows $\times 19$ attributes)Deliverable: Social_Media_Engagement_Analytics.ipynb (Jupyter Notebook)Objective: Clean raw engagement metrics, engineer new analytical features, compute descriptive statistics, build 13 static and interactive visualizations, and summarize actionable content insights.

🛠️ Step-by-Step Workflow

Phase 1. Project Environment Setup
Place the social_media_engagement_5000.csv file inside a dedicated project folder.
Open that root folder in VS Code.
Create a virtual environment with Python 3.12 version.
Install pandas, numpy, matplotlib, seaborn, plotly, and nbformat in the virtual environment.
Create social_media_engagement_analytics.ipynb in the project folder.
Select the virtual environment kernel.

Phase 2: Data Import and Cleaning
Import social_media_engagement_5000.csv using pd.read_csv.
Convert post_created_at from text to datetime.
Run NumPy array operations (mean, maximum) on the likes column.
Detect 150 missing records each in age, gender, likes, comments, shares, and sent_time.
Fill numeric gaps with the median and categorical gaps with the mode.
Verify duplicate rows with drop_duplicates.
Standardize gender, sent_time, post_type, and post_category casing and whitespaces.
Identify 600 rows where total interactions (likes + comments + shares) exceed the impression count.
Scale those interactions proportionally to stay within the impression limit and recalculate the engagement rate.
Parse the hashtag column to create a numeric hashtag count feature.

Phase 3: Exploration, Wrangling, and Statistics
Inspect dataset structure and distributions using .head(), .tail(), .shape, .info(), .describe(), .value_counts(), .corr(), and .groupby().
Create a weighted engagement score (likes * 2 + comments + shares * 3).
Create a log impression feature using np.log1p.
Merge a regional market tier lookup table using pd.merge().
Compute mean, median, mode, standard deviation, variance, percentiles, skewness, and kurtosis across likes, comments, shares, watch_time, engagement_rate, and follower_count.

Phase 4: Visualization and Final Reporting
Generate 13 visualizations across three libraries:
Matplotlib (6 plots):
Scatter plot (likes vs. impression)
Line plot (monthly engagement trend)
Bar chart (posts by category)
Pie chart (gender distribution)
Histogram (age)
Box plot (engagement_rate)
Seaborn (6 plots):
Count plot (post_type)
Bar plot (average likes by category)
Violin plot (followers vs. sentiment)
Swarm plot (engagement_rate vs. device)
Heatmap (correlation matrix)
Pair plot
Plotly (1 interactive plot):
Interactive bubble chart comparing average impression, engagement rate, and likes by country.
