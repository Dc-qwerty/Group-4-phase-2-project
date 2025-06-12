# Film Industry Analysis for New Studio Strategy

![Movie Studio image](https://github.com/user-attachments/assets/ccbbc3e6-7a17-4e9d-9db5-263164a909f2)

# Authors 

1. David Clement Ngangu
2. Olive Njeri
3. Kungu Wakaimba Washington
4. kelly Wanjiku Kihige 
5. Steve Opar
6. Mercy Chepkorir

<sub><i>Phase 2 Project, Moringa Data Science Program.</i></sub>

# Project Overview

With the growing  demand for creation of original video content , many leading companies are increasinngly investing heavily in creating their own entertainment ventures . In response to this trend, our company aims to  launch a new movie studio but lacks industry insights . This project explores current box office trends to provide strategic insights for launching a successful movie studio. By analyzing data from major film industry sources, we identify what types of movies are currently performing best financially and critically.

# Stake holders
* Executive Leadership Team
* Head of the New Studio 
* Production Planning Team
* Investors and Board Members

  ## Business Objectives
  To successfully launch our new movie studio, we need to base decisions on proven industry trends. Our objectives are to:
* Understand the characteristics of successful films, including genre, length, and audience reception.
* Identify the most profitable film genres to prioritize in production.
* Determine budget ranges

  By meeting these objectives, we aim to minimize financial risk and position the studio for long-term success in a competitive industry.

# Data Understanding 
To guide our strategic recommendations, we analyzed data from two trusted sources in the film industry—Box Office Mojo and IMDb. These datasets provide both financial performance and audience sentiment, giving us a well-rounded view of what makes a movie successful.

# Data Source 
The data set was sourced from :  

# 1 . Box Office Mojo (bom.movie_gross.csv)  
This is a compressed CSV file containing box office performance data for a wide range of films. It includes both domestic and international gross earnings by year and studio.
# 2. IMDb SQLite Database (im.db.zip) 
This is a zipped SQLite database that contains metadata and user rating information for movies. The relevant tables, movie_basics and movie_ratings, were merged to support deeper insights.
# 3. The Numbers Table (tn.movie_budget.csv)
This dataset provides detailed financial performance metrics for films, especially focusing on production costs and box office returns.

The data sources were sufficient for our analysis because it combined financial performance metrics with audiences and films meta data .This allows us to identify trends in what types of films are both commercially successful and well-received by viewers—critical insights for a company looking to make informed decisions about the kinds of films their new studio should produce.

# Feature Understanding and Documentation
To support the analysis of film performance and guide our studio’s content strategy, we use features from two datasets

## Box Office Mojo (bom.movie_gross.csv.gz)
This dataset provides financial performance data for films.

## IMDb Datasets (movie_basic + movie_ratings)

Metadata and user-generated feedback, this dataset provides financial performance data for films.

## The Numbers Table: tn.movie_budgets.csv
This dataset provides detailed financial performance metrics for films, especially focusing on production costs and box office returns.

# Data Preparation 

To ensure that the data set was reliable for analysis  , we did data cleaning and preprocessing of our data.
The data cleaning involved  :

* checking for any missing values .
* checking for duplicate rows and columns . 
*  Converted data types for consistency
*  Merge Box Office Mojo and IMDb datasets using common keys (e.g., titles and years)
*  Calculated total gross revenue (domestic + foreign )

  #  Film Industry Analysis for New Movie Studio
  
# Analysis Introduction

This analysis aims to identify what types of films are currently performing best at the box office and which studios are the best to guide our new movie studio's content strategy. We'll examine four key relationships:
# 1. Genre Popularity & Trends
# * Key Variables:
genres
averagerating
total_gross

Why These Matter:
Determine which genres are most profitable (highest revenue) and most appreciated by audiences (highest ratings).

# 2. Studio Performance Analysis
Key Variables:
average_rating
total_gross

Why These Matter:
Studio perfomance helps a new movie studio identify, succesful production and distribution partners and potential competitive positioning

# 3. Audience Preferences Analysis
Key Variables:
averagerating
 
 Why These Matter:
Understand the relationship between ratings and revenue to balance artistic quality and commercial success.

# 4. ROI Analysis
Key Variables:
production budget
worldwide gross Why These Matter:
ROI (Return on Investment) matters because it shows how efficiently money is being used to generate profit.

# Expected Insights
By the end of this analysis, we'll provide actionable recommendations on:

Which genres to prioritize for production
Which studios are most succesful
Do high ratings lead to higher revenue
Return efficiency relative to cost
 
** These specific variables were chosen because they:
* Are consistently available across datasets
* Represent controllable business decisions (genre, release timing)
* Directly measure success (revenue, ratings)
* These variables naturally led to the 3 chosen approaches


# Analysis 

This analysis aims to identify what types of films are currently performing best at the box office and which studios are the best to guide our new movie studio's content strategy. We'll examine three key relationships :
1.  Genre Profitability Analysis
2.  Studio Performance Analysis
3. Audience Preferences (Ratings vs. Revenue)
4. ROI Analysis 


# 1.  Genre Profitability Analysis
 our main goal was to :
- Understand which movie genres are most profitable (highest average revenue)
- Understand which genres are most appreciated by audiences (highest average rating)
# Key Findings:
- Sci-Fi, Adventure & Animation genres generate the highest average revenue.
- Sci-Fi genres achieve both high revenues and high IMDb ratings a good commercial and critical performance.
- Animation also shows strong ratings and very high revenue a good genre for both family and general audience markets.
   
# 2.  Studio Performance Analysis
### Goal:
This helps identify which studios consistently produce highly-rated films. Understanding studio performance is crucial for strategic partnerships, distribution planning, and benchmarking success.
# Key Findings:
The two studios P/DW and BV have the best average revenue which makes them the best candidates to partner with

# 3. Audience Preferences (Ratings vs. Revenue)
### Goal:
- Understand relationship between IMDb ratings and total revenue
- Identify which rating ranges are most commercially successful
 # Key Findings:
- Weak positive correlation (r=0.20) between ratings and revenue — higher ratings are slightly associated with higher revenue.
- range 6-7 performs best commercially mass-appeal films that attract large audiences.
- Blockbuster franchises perform well even with mid-range ratings.
- Highest rated movies (>8) have more modest commercial performance.

 # 4. ROI Analysis
### Goal:
Understand which genres and studios provide the best return on investment
Help the studio make financially sound production decisions 


# Key Findings

we created a tableau dashboard to represent our analysis 
![Dashboard 1 (1)](https://github.com/user-attachments/assets/c1657a33-6cc2-45ac-9f18-7f00257ad1d0)

# summary of our Findings 

 After analyzing the combined financial and audience data, we uncovered several important insights to guide the studio's strategy: 
 
# 1. Genre Performance

Sci-Fi, Adventure, and Animation genres consistently generated the highest average gross revenue.
These genres also performed well in terms of audience ratings, indicating both commercial and critical success.
Drama and Documentary genres received high ratings but showed lower box office performance—ideal for prestige projects, not profit centers.

# 2. Studio Benchmarking
Certain studios have a strong track record of releasing high-grossing and well-rated films.
These studios could be ideal partners for co-productions, distribution deals, or mentorship in early stages.
Repeated success across multiple years signals strong production and marketing capabilities.

# 3. Audience Preferences vs. Revenue
There is a weak positive correlation (r ≈ 0.20) between IMDb ratings and box office revenue.
Films rated 6–7 performed best commercially—suggesting mass appeal outweighs critical acclaim in revenue terms.
Highly rated films (8+) often have strong critical reception but more modest revenue, possibly due to niche appeal.
Some blockbuster franchises performed well despite mid-range ratings, driven by brand loyalty and strong marketing.

These findings highlight the need for a balanced portfolio strategy—combining high-revenue genre films with critically respected projects to grow both profit and reputation.

# Strategic Recommendations
Based on our analysis of box office trends and audience preferences, we propose the following strategic actions to guide the launch and growth of the new movie studio:

 1. Focus on High-Performing Genres
Prioritize Action, Adventure, Sci-Fi, and Animation films, which consistently deliver strong box office returns.

Develop franchise-ready content in these genres to build long-term audience engagement and brand equity.

2. Adopt a Balanced Production Strategy
Allocate larger budgets to blockbuster genres with proven commercial success.

Invest in mid-range budget films in genres like Drama and Documentary to build critical acclaim and diversify the studio's portfolio.

3. Optimize Release Timing
Schedule major releases around holiday seasons (e.g., summer, December), when audience turnout and revenue potential are highest.

Avoid crowded release periods dominated by major competitors unless backed by strong marketing.

 4. Pursue Strategic Partnerships
Collaborate with top-performing studios for co-productions, knowledge transfer, and wider distribution networks.
Leverage industry partnerships to reduce risk and increase exposure for debut releases.

 5. Build a Data-Driven Culture
Continue monitoring audience trends, ratings, and financial metrics post-release to refine future strategies.
Incorporate feedback loops and predictive analytics into decision-making processes.

By following these recommendations, the new studio can position itself for both short-term box office success and long-term brand growth—creating content that resonates with audiences and generates sustainable profits.

# Conclusion

Our analysis offers a data-driven roadmap for launching a successful and competitive movie studio. By combining financial performance metrics from Box Office Mojo with audience insights from IMDb, we identified what makes certain films commercially successful and critically appreciated.
The analysis reveals:
1. Action, Adventure, Sci-Fi, and Animation genres offer the highest potential for profitability.
Films with average IMDb ratings between 6 and 7 tend to perform best at the box office, indicating a preference for broad audience appeal.
2. Strategic partnerships with established studios can improve production quality and boost distribution reach.
3. Mid-range budget planning and seasonal release timing are key to maximizing return on investment.

While the analysis yielded valuable insights, several limitations were encountered some of them are : we had Incomplete Data, Some films were missing key fields  which reduced the sample size after cleaning. we also encountered Data Merging Issues , Matching films across datasets required aligning titles and release years, which introduced potential for mismatches or dropped records. Genre Ambiguity , many films were tagged with multiple genres, making it difficult to assign clear labels. We addressed this by "exploding" genres, but this may dilute genre-specific insights. International Market Complexity, Foreign gross data lacked regional breakdowns, limiting our ability to analyze performance in specific countries or continents.Rating Bias,IMDb ratings reflect viewer sentiment but may skew toward more active or niche audiences, potentially biasing our interpretation of popularity.

Despite these challenges, our findings provide a solid strategic foundation for decision-making. Future work could include integrating streaming platform performance, social media sentiment, or production cost data for a more holistic view.











