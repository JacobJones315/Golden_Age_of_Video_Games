# Golden Age of Video Games Data Analysis Through SQL

* Video games have exploded into a massive industry, with forecasts suggesting the global gaming market will exceed $300 billion by 2027, according to Mordor Intelligence. With such substantial financial stakes, major game publishers are highly incentivized to produce the next blockbuster. However, amidst this fierce competition, one crucial question persists: Are games improving, or have we already experienced the pinnacle of video gaming's golden era?
* In this analysis I explored video game data from 1977-2020 by utilizing advanced SQL techniques such as table joins, filtering, set theory, and subqueries to delve deep into the history of video games. The original data tables game_sales and game_reviews included over 13,000 games but was reduced to focus on the top 400 best selling videogames over this time period.

* Determing the golden age of video games is very subjective depending on what your genre of choice is and how you want to look at the data. I decided to be as unbiased as posible and stricly looked at data collected from critic scores, user/player scores, and games sold during the year the game launched. As we all know how critics score video games and how players score video games can vary greatley, I had to take this into account. 

# Summary
* Wii Sports, Super Mario Bros. for NES, and Counter-Strike: Global Offensive for PC claim the top three spots on our list for games sold during our testing period.
* The Top 10 years ranked by average critic score with atleast 4 games reviewed from highest to lowest: 1998, 2004, 2002, 1999, 2001, 2011, 2016, 2013, 2008, and 2017.
* The Top 10 years ranked by user/player score from highest to lowest: 1997, 1998, 2010, 2009, 2008, 1996, 2005, 2006, 2002, and 2000.
* The only years where both citics and players agreed were 1998, 2002, and 2008.
* Overall, the Golden age of gaming appears to from the late 90's through the 2000's. With around 175 million games sold in 2008.

# Procedure
* First, I started by selecting the the top 10 games sold in this period filtering by games sold in descending order.
* Next, I performed a left join on my games_sold and reviews data tables in order to visualize the critic and user reviews by year.
* Next, I wanted to determine how many out of my top 400 games did not have critic scores attached to them. I determined there was only 31/400, less than 8% which I was happy with.
* Next, I created a table of the TOP 10 years by average critic reviews. (top_critic_years)
* Next, I created a seperate table of the TOP 10 years by average critic reviews in which the year had more than 4 games reviewed. This was done in order to get out the years where only a couple games were reviewed.(top_critic_years_more_than_four_games)
* Next, I wanted to determine which years fell out of my top_critic_years table when looking at my top_critic_years_more_than_four_games table, to determine if their was a significant difference. I utilized a sub query to filter out the years that were not present in my top_critic_years_more_than_four_games table. Only 3 years remained in my table with more than 4 games reviewed.
* Next, I created a seperate table lookin at the Top 10 games by year for average user/player score in years with more than 4 games released. (top_user_years_more_than_four_games)
* Next, I wanted to determin which years did both critics and users agree were great years. Using set theory I perfomed an intersection between my two tables top_critic_years_more_than_four_games and top_user_years_more_than_four_games to see the years that were included in both tables. Three years were agreed on.
* Finally, I wanted to see the sum of games sold in each of these three years, I utilized my query from the previous step as a subquery in my final query. I selected year and sum of games sold ordering by total games sold in descending order for years that were in my previous query to find the golden age of gaming.  
