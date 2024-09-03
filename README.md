#  Twitch Analysis
![Twitch icon.](twitch_icon.png) 

## Introduction

This document presents a comprehensive analysis of Twitch streaming data spanning from 2016 to 2023. As one of the leading platforms for live streaming, particularly in the gaming industry, Twitch has seen remarkable growth and evolution over the years. This analysis aims to explore key metrics that define the platform's success and its impact on the gaming community.

The analysis focuses on critical aspects such as:
- **Hours Watched:** A measure of audience engagement over time.
- **Hours Streamed:** An indicator of content creation activity.
- **Peak Viewers and Channels:** Identification of periods with the highest audience and channel activity.
- **Average Viewers and Channels:** Understanding of consistent engagement and content creation.

By examining these metrics, we aim to uncover trends, patterns, and shifts that have shaped the Twitch ecosystem over the past eight years. This analysis not only highlights the platform's growth but also offers insights into the dynamic relationship between content creators and viewers. The findings will be valuable for a wide range of stakeholders, including streamers, game developers, marketers, and analysts, providing them with a deeper understanding of the live-streaming landscape and its trajectory.

Through a detailed examination of the data, this document seeks to provide a clear picture of how Twitch has evolved and what factors have contributed to its position as a dominant platform in the world of live streaming.

## Technology
- Programming Language: Python
- Jupyter Notebook

## Data Overview

- Dataset
Rank - the rank of a game (int)               
Game - the name of a game (string)            
Month - the month of the year (int)             
Year  - the year (int)             
Hours_watched - number of hours watched for a game (int)   
Hours_streamed - number of hours streamed for a game(int)   
Peak_viewers - the peak viewers for a game(int)      
Peak_channels - the peak number of channels for a game (int)     
Streamers - the number of streamers streaming a game (int)    
Avg_viewers - the average viewers for a game (int)          
Avg_channels  the average channels for a game (int)      
Avg_viewer_ratio the aeverage viewer ratio for a game (float)  

The dataset can be found on Kaggle : 
(https://www.kaggle.com/datasets/rankirsh/evolution-of-top-games-on-twitch/data)

## Data Cleaning and Preprocessing
The data did not need any pre-processing nor cleaning as the data was in the correct format and had the correct data types.

## Data Summary
**Hours Watched:**
- Key Insights
 - the average number of hours watched over an 8 year span was 5645920 hours
 - between 2016 and 2021 a steady increase in hours watched was observed, from 2021 onwards the hours watched decreased, we can assume that this decrease is attributed to twitch being a growing platform in its       early years in combination with covid from 2019 people were confined to their homes, once covid ended people were able to resume normal day to day activities thus a decreased viewership was observed.
 -  at lower hours watched, hours streamed were fairly clustered together and had a positive correlation and lower variance ,however as the stream hours increased
    there was more variance and suggests that after a certain amount of hours streamed viewership did not increase.
 - as the average viewers increased so did the hours watched, a very strong correlation was obvserved with little to no outliers.
 - the distribution of the hours watched was negatively skewed, where most values  lied within the 0-10 million hours range.


