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

The dataset can be found on Kaggle: 
> https://www.kaggle.com/datasets/rankirsh/evolution-of-top-games-on-twitch/data

## Data Cleaning and Preprocessing
The data did not need any pre-processing nor cleaning as the data was in the correct format and had the correct data types.

## Data Summary
> **Hours Watched:**
- Key Insights
 - the average number of hours watched over an 8 year span was 5645920 hours
 - between 2016 and 2021 a steady increase in hours watched was observed, from 2021 onwards the hours watched decreased, we can assume that this decrease is 
   attributed to twitch being a growing platform in its early years in combination with covid from 2019 people were confined to their homes,as well
   social media competitors like Youtube, TikTok  Facebook and Instagram.
 - at lower hours watched, hours streamed were fairly clustered together and had a positive correlation and lower variance ,however as the stream hours increased
   there was more variance and suggests that after a certain amount of hours streamed viewership did not increase.
 - as the average viewers increased so did the hours watched, a very strong correlation was obvserved with little to no outliers.
 - the distribution of the hours watched was negatively skewed, where most values  lied within the 0-10 million hours range.

> **Viewership:**
 - The same patterns can be observed between 2021 to 2023 where peak viewership and average viewership steadily decreasing.

> **Games:**
- From 2016 to 2021 the number of games streamed saw a steady increase, However, from 2021 and beyond the number of games streamed steadily decreased.
- Over several years,With respect to hours watched most people enjoyed watching the "Just Chatting" channels with the exception of the rank 1 game League
  of Legends and Grand Theft Auto 4, suggesting that most viewers enjoy variety streams than channels with games.

> **Channels:**
 - an interesting observation to note is that while number of streamers decreased from 2022 onward, the average number of channels increased.
   The rise in the number of channels could be due to the creation of automated or thematic channels that don't require active streamers, such as music   
   streams, reruns, or automated content. This could reflect a trend towards more passive or continuous content that doesn't rely on live streamers.
- Consolidation of viewership, If fewer streamers are active but the number of channels has increased, it might indicate that viewership is consolidating around a 
  smaller group of highly popular streamers


### Predicting Hours Watched
> **Model Selection:**
 - Linear Regression Model
> **Feature Selection:**
- Hours_streamed: Correlation = 0.75
- Streamers: Correlation = 0.73
- Avg_viewers: Correlation = 0.75
- Avg_channels: Correlation = 0.75
  
### Excluded Features
- a correlation matrix was created based all the numeric features and then further supplemented by a heat map for feature selection
The following features were excluded or given less priority due to their weak or negligible correlations with `Hours_watched`:
- **Month**
- **Year**
- **Avg_viewer_ratio**

By focusing on the selected features, the predictive model is better positioned to deliver accurate results.

### Model Analysis
- Mean Absolute Error : 73591.29
  - a fairly low MAE which suggests the model is fairly accurate
- R-squared Score: 0.99
  - indicating that the model fits the data very well
- Scatter Plot: plotting actual values vs Predicted values
  - the scatter plot with a perfect line visible, shows that the predicted and actual values almost perfectly fit the line, indicating an accurate model.

 ![image](https://github.com/user-attachments/assets/054d4ac8-a200-4e20-ab0a-434eca10ed26)

 ### Conclusion
 > **Key Findings:**
   - Twitch experienced major growth in its platform in the initial years, especially with covid pandemic which confined people to their homes.
   - 2021 saw the platform lose streamers and viewership, which could be for a number of reasons such streaming competitors like Youtube,TikTok and Kick,
     to name a few,people also having the freedom to leave their homes after the pandemic could possibly be contributing factor.
   - ultimately Twitch has solidified its user base and as it being the primary streaming platform for users.
 > **Limitations:**
   - The analysis could be more accurate with the aid of data pertaining to other streaming and social media platforms to guage whether their platforms
     also suffered from loss in user engagement.

 ### Closing Statement
 > In conclusion, this analysis provides valuable insights into the key factors driving viewer engagement.
