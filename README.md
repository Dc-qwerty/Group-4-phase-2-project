# Film Industry Analysis for New Studio Strategy

![Movie Studio image](https://github.com/user-attachments/assets/ccbbc3e6-7a17-4e9d-9db5-263164a909f2)

# Project Overview

As the demand for creation of original video content continues to grow, many leading companies are investing heavily in creating their own entertainment ventures . In response to this trend, our company plans to  launch a new movie studio but lacks industry insights . 
This project explores current box office trends to provide strategic insights for launching a successful movie studio. By analyzing data from major film industry sources, we identify what types of movies are currently performing best financially and critically.

# Data Understanding 
# Data Source 
The data set was sourced from two main sources 

* [Box Office Mojo](https://www.boxofficemojo.com/) it Offers box office performance data for a wide range of films and  included domestic and international grosses.
* [IMDb Datasets](https://www.imdb.com/interfaces/) it contains meta data and user rating information for a movie .

The data sources were sufficient for our analysis because it combined financial performance metrics with audiences and films meta data .This allows us to identify trends in what types of films are both commercially successful and well-received by viewers—critical insights for a company looking to make informed decisions about the kinds of films their new studio should produce.

# Feature Understanding and Documentation
To support the analysis of film performance and guide our studio’s content strategy, we use features from two datasets
  # bom.movie_gross.csv.gz`
This dataset provides financial performance data for films.
- **Identification :**
    - *title*: The name of the film (string)
- **Production :**
    - *studio*: The production or distribution studio responsible for the film (string).
- **Finanicial Metrics :**
    - *domestic_gross*: Total box office revenue earned in the domestic (U.S.) market
    - *foreign_gross*: Total box office revenue earned in international markets *(integer or float)*.

#### 2. IMDb Merged Table: `movie_basic` + `movie_ratings`
This dataset provides financial performance data for films.
- **Identification :**
    - *movie_id*: A unique identifier for each film(string)
- **Titles :**
    - *primary_title* : The title most commonly used(string).
    - *original_title* : The title most commonly used(string).
- **Time :**
    - *start_year*: The year the film was first released
- **Content Characteristics :**
    - *runtime_minutes* : The duration of the film in minutes
    - *genres* : The genre or genres associated with the film.
- **Audience Feedback :**
    - *averagerating* : The average IMDb user rating for the film
    - *numvotes* : The total number of IMDb users who rated the film

Together, these features provide a comprehensive view of each film's
commercial success, genre and runtime characteristics, viewer sentiment, and release context.
  
# Data Preparation 

To ensure that the data set was reliable for analysis  , we did data cleaning and preprocessing of our data.
The data cleaning involved  :

* checking for any missing values .
* checking for duplicate rows and columns . 
*  Converted data types for consistency
*  Merge Box Office Mojo and IMDb datasets using common keys (e.g., titles and years)
*  Calculated total gross revenue (domestic + foreign )

# Analysis Overview 

## Analysis Introduction

This analysis aims to identify what types of films are currently performing best at the box office and which studios are the best to guide our new movie studio's content strategy. We'll examine three key relationships :
1.  Genre Profitability Analysis
2.  Studio Performance Analysis
3. Audience Preferences (Ratings vs. Revenue)

 ## Expected Insights
 By the end of this analysis, we'll provide actionable recommendations on:  
 1. Which genres to prioritize for production  
 2. Which studios are most succesful
 3. Do high ratings lead to higher revenue

We choose these specific variables because they:  
 - Are consistently available across datasets  
 - Represent controllable business decisions (genre, release timing)  
 - Directly measure success (revenue, ratings)  
 - These variables naturally led to the 3 chosen approaches

# 1.  Genre Profitability Analysis
 our main goal was to :
- Understand which movie genres are most profitable (highest average revenue)
- Understand which genres are most appreciated by audiences (highest average rating)
# Method used for analysis :
- Some movies have multiple genres we explode them so each genre appears in a separate row
- Group data by genre and calculate:
    - Average gross revenue
    - Median gross revenue
    - Movie count per genre
    - Average IMDb rating
      
# 2.  Studio Performance Analysis
### Goal:
This helps identify which studios consistently produce highly-rated films. Understanding studio performance is crucial for strategic partnerships, distribution planning, and benchmarking success.

# 3. Audience Preferences (Ratings vs. Revenue)
### Goal:
- Understand relationship between IMDb ratings and total revenue
- Identify which rating ranges are most commercially successful
  ### Method:
- Create rating tiers:
    - <5
    - 5-6
    - 6-7
    - 7-8
    - 8+
- Group data by rating tier and calculate:
    - Average revenue
    - Median revenue
    - Movie count per tier
    - Average rating
- Plot scatter of individual movie ratings vs. total gross
- Compute correlation between rating and revenue

  **Key Findings:**
1. Weak positive correlation (r=0.20) between ratings and revenue — higher ratings are slightly associated with higher revenue.
2. range 6-7 performs best commercially mass-appeal films that attract large audiences.
3. Blockbuster franchises perform well even with mid-range ratings.
4. Highest rated movies (>8) have more modest commercial performance.


# Key Variables used in analysis
 The key variables used included :
 * Title - the name of the film
 * Release_date	- Original theatrical release date
 * Genre -primary content type , narrative style of each film. 
 * Average rating - 	IMDb average user rating
 * domestic_gross	Domestic box office gross 
 * foreign_gross	Foreign box office gross 
 * Total gross - 


# Relevance of the Analysis

The findings help inform what kinds of films to produce, how to allocate budgets, and when to release them maximizing both financial return and brand value.


 # Summary of Findings
 
1. Sci-Fi, Adventure, and Animation are the best genres for profitability and audience appeal.
2. Partnering with top-performing studios can enhance production quality and distribution.
3. Balancing revenue and ratings requires a mixed strategy—focusing on blockbusters for income and critically acclaimed projects for reputation.

These insights inform the recommendation that the studio prioritize action and adventure franchises, carefully budget mid-tier original films, and strategically time releases around holiday seasons.

# Strategic Recommendations

- Prioritize **action, adventure, and animation** projects for blockbuster returns  
- Allocate mid-range budgets to **critically acclaimed genres** such as drama or documentary  
- **Time releases strategically**—especially around holiday periods  
- Establish **strategic partnerships** with successful studios for enhanced production and distribution

These insights will serve as the foundation for building a **successful and data-informed movie studio**.

# Conclusion

By analyzing financial trends and viewer sentiment, we’ve developed a strategic blueprint for launching a data-informed and competitive movie studio. This foundation equips leadership with the evidence needed to make profitable, creative, and impactful decisions.









