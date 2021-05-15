# YouTube and Netflix Viewership Analysis
- Author(s): [Chau Hoang](https://www.linkedin.com/in/chau-jo-hoang-227ba991/) & [Tanay Mukherjee](https://www.linkedin.com/in/tanay-mukherjee-96206861/)
- Date created: 17th March, 2021
- Class: CIS 9440

----

**Project Objective:** 
<p> Follow the Kimball Lifecycle to design and develop a public, cloud-based Data Warehouse with a functioning BI Applications. </p>

**Project Tools:**
The tools used to build this Data Warehouse were:
1. For data integration - Python
2. For data warehousing - Google BigQuery
3. For Business Intelligence - Tableau

## Kimball Lifecycle Project Stages

### Project Planning

**1. Motivation for project:**
<p> We want to analyze YouTube trending videos statistics in 10 different countries to learn more about different trends and topics that people from different parts of the world are interested in at the same time frame. Now do comparison with Netflix data by countries, category and time period. </p>

**2. Description of the issues or opportunities the project will address:**

The dataset gives us a lot of avenues to analyze the videos people watch across the globe.
1. What category of videos really trend on a daily basis? Is there a connection between multiple Geos?
2. Does the number of views have a relationship with total interaction (like, dislikes or comments)?
3. What kind of videos have a high frequency of restriction enabled on likes or comments?
4. What are the top topics for viewership - entertainment, politics, sports, etc?
5. An opportunity to keep the date format consistent across all countries for which we analyse.
6. Next, we redo these above analyses for Netflix data and compare it with YouTube result by joining the data to see if we can manage to get some nice insights about people’s choice on free video entertainment platform like YouTube v/s OTT platforms like Netflix.


**3. Project Business or Organization Value:**

- High-level Business Initiative:
<p> To see any correlation between top trending videos in countries with high YouTube viewership and what are the preferences on Netflix for those countries. </p>
  

- BI Sponsors and Stakeholders (who will own this project?)
<p> Analytics team of a consulting firm who are trying to do some market research on visual content across various countries and then do profiling based on category of the content. </p>
  

- What’s the Business Value?
<p> Can this exercise be used to extend a possible collaboration with Ad agencies to figure out what kind of videos might bring more traction to their Product Ads for future campaign strategy on trending YouTube videos. How can OTT platforms like Netflix make benefit out of this? </p>


### Data Sources:
1. [Netflix Data](https://www.kaggle.com/shivamb/netflix-shows)
2. [YouTube Data](https://www.kaggle.com/datasnaek/youtube-new)


### Business Requirements Definition

List of Data Warehouse KPI's:
1. Total views by category
2. Top channels with most trending videos
    - With filters for categories
3. Interactions by video views
    - Likes and dislikes per view
    - Grouped by category
4. Total Likes and Total Dislikes by Geo
5. YoY Comparison [2017 vs 2018] of key metrics by category
    - Comment count
    - Total Likes
    - Total Dislikes
    - Total Views
6. Total Likes and Total Dislikes by Year & Month
7. Content heatmap for Netflix for by Year & Month
8. Total records in Netflix by Geo


### Dimensional Model

1. This project's Dimensional Model consists of 3 Facts and 4 Dimensions:

![image](https://user-images.githubusercontent.com/6689256/118370255-e2c00180-b574-11eb-84e1-c2caa7712350.png)

2. This project's Kimball Bus Matrix:

![image](https://user-images.githubusercontent.com/6689256/118370261-eb183c80-b574-11eb-8ecb-876fb301cf8f.png)

### Business Intelligence Design and Development

**A) List of Visualizations for each KPI:**
1. Total views by category
    - Tree map: This viz. helps us not only measure the share of views for each category but also how big the share is with respect to overall data sample. 

2. Top channels with most trending videos
    - Bar chart: This viz. help us compare the top 10 channels for any category.

3. Interactions by video views
    - Bubble Chart (Scatter plot): This viz is useful as we can measure our dimensions against multiple metrics by size of the bubble, color of the bubble and positioning of the bubble across multiple x-axes and y-axis as it is in this case.

4. Total Likes and Total Dislikes by Geo
    - Map View: This is to use the inbuilt world map from Tableau and plot the metrics against each country for YouTube.

5. YoY Comparison of key metrics by category
    - Stacked bar chart: Just to compare various performance metrics for periods. In this case 2017 vs 2018.

6. Total Likes and Total Dislikes by Year & Month
    - Multiple Bar chart: Comparison amongst bar charts for multiple metrics and how they stand against each other.

7. Content heatmap for Netflix for by Year & Month
    - Heatmap: It will explain the spread of total content records across months and years and how the spread is higher or lower to their neighbours.

8. Total records in Netflix by Geo
    - Map View: This is to use the inbuilt world map from Tableau and plot the metrics against each country for Netflix.


**B) BI Application Wireframe design:**

![image](https://user-images.githubusercontent.com/6689256/118370395-814c6280-b575-11eb-8a64-2995f7cc9600.png)


**C) Picture of final Dashboard:**

- Analyzing key KPIs

![image](https://user-images.githubusercontent.com/6689256/118370435-ac36b680-b575-11eb-9e42-2cff57440b5e.png)

- Distribution of content by Geos

![image](https://user-images.githubusercontent.com/6689256/118370482-e0aa7280-b575-11eb-8afd-0762ef059718.png)

### Deployment

The project was deployed on Tableau Public: [Click Here!](https://public.tableau.com/profile/tanay.mukherjee#!/vizhome/CIS_9440_Project_Group_12/PerformanceDashboard)
