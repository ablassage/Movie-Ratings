# Movie-Ratings 

The goal of this study was to find a correlation between Budget, revenue, and total rating.  I started my project by looking at "The Movie Database" dataset of 5,000 movies from 2018.
I first cleaned the data in Excel removing movies that had 0$ in their budget or revenue.  After that I took the data to SQL to parse out extraneous columns before moving the study back to excel

Select 
budget, id, original_title, popularity, production_companies, release_date, revenue, runtime, title, vote_average, vote_count
FROM 
`concise-haven-314917.Movie_ratings.movie_ratings`
where 
vote_count > 1500
order by
budget DESC 

This was the SQL query I used to transform the Data. As there were a lot of datapoints with few votes and extremely high ratings.  Multiple movies had sub 200 votes with a rating of 9 or higher.
For comparison, after this SQL query was utilized and I took the clean data back to Excel, the highest rating of any movie was 8.5.  

The relationships between movies and rating was less standard than would be expected For example, the movies with the highest budget did not have the highest rating.
In fact, if a movies budget was over $100 million it brought the average rating down to 6.6 from 6.8.
The highest budgets spent the most per point while not leading in any other category.  Though, as a trend, most movies with a high budget at the very least recoup their spendings.
With only one movie In the top 300 having a higher budget than revenue that came in.

Movies with a longer runtime saw higher avg_ratings, if a movies runtime was over 150 minutes the average rating shot up to 7.34
