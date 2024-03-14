# Golden Age of Video Games Data Analysis Through SQL

* Video games have exploded into a massive industry, with forecasts suggesting the global gaming market will exceed $300 billion by 2027, according to Mordor Intelligence. With such substantial financial stakes, major game publishers are highly incentivized to produce the next blockbuster. However, amidst this fierce competition, one crucial question persists: Are games improving, or have we already experienced the pinnacle of video gaming's golden era?
* In this analysis I explored video game data from 1977-2020 by utilizing advanced SQL techniques such as table joins, filtering, set theory, and subqueries to delve deep into the history of video games. The original data tables game_sales and game_reviews included over 13,000 games but was reduced to focus on the top 400 best selling videogames over this time period.

* Determining the golden age of video games remains a subjective endeavor, heavily influenced by individual preferences and analytical approaches. To mitigate bias, I adopted a methodology relying solely on objective data sourced from critic scores, user/player ratings, and sales figures corresponding to each game's launch year. Acknowledging the disparity between how critics and players assess games, I ensured a balanced assessment, recognizing the nuanced perspectives inherent in each evaluation metric.

# Summary
* Wii Sports, Super Mario Bros. for NES, and Counter-Strike: Global Offensive for PC claim the top three spots on our list for games sold during our testing period.
* The Top 10 years ranked by average critic score with atleast 4 games reviewed from highest to lowest: 1998, 2004, 2002, 1999, 2001, 2011, 2016, 2013, 2008, and 2017.
* The Top 10 years ranked by user/player score from highest to lowest: 1997, 1998, 2010, 2009, 2008, 1996, 2005, 2006, 2002, and 2000.
* The only years where both citics and players agreed were 1998, 2002, and 2008.
* Overall, the Golden age of gaming appears to from the late 90's through the 2000's. With around 175 million games sold in 2008.

# Procedure
* Top 10 Games Selection: Started by identifying the top 10 best-selling games within our specified period, sorting them by sales volume in descending order.
* Visualizing Reviews: Conducted a left join between the tables containing game sales and reviews data to visualize both critic and user reviews by game over the years.
* Critic Score Analysis: Investigated the presence of critic scores for the top 400 games. Found that only 31 out of 400 games lacked critic scores, accounting for less than 8%, indicating satisfactory data coverage.
* Top Years by Critic Reviews: Created a table showcasing the top 10 years based on average critic reviews.
* Refining Critic Reviews Analysis: Developed a separate table focusing on the top 10 years with more than four games reviewed, filtering out years with limited data to ensure robust analysis (top_critic_years_more_than_four_games).
* Comparative Analysis: Utilized a subquery to compare the top years from the general critic reviews table with the refined table, identifying any significant deviations. Only three years remained in the refined table.
* Top Years by User Scores: Established a separate table highlighting the top 10 years for average user scores, specifically in years with more than four games released (top_user_years_more_than_four_games).
* Consensus Analysis: Employed set theory more specifically table intersection to identify the years where both critics and users agreed on exceptional gaming experiences, resulting in three mutually agreed-upon years.
* Sales Volume Examination: Finally, assessed the total games sold in each of the three agreed-upon years. Utilized the previous query as a subquery to extract the sum of games sold per year, providing insight into the golden age of gaming.
