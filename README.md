# tmdb-movie-analysis
Analysing the tmdb movie database to get some insights.

### Data Cleaning

There are missing data in the following columns: imdb_id, cast, homepage, director, tagline, keywords, overview, genres, production_companies.

I removed the columns. There was also a duplicate row. I removed the duplicate row.

There were 10866 records and 21 columns in the dataset. After cleaning, there were 10865 records and 10 columns.

### Results

The top 10 movies with the highest runtime are:
* The Story of Film: An Odyssey,
* Taken,
* Band of Brothers,
* Shoah,
* North and South, Book I,
* Planet Earth,
* The Pacific,
* John Adams,
* Life,
* Generation Kill

The top 10 movies with the highest revenue are:
* Avatar,
* Star Wars: The Force Awakens,
* Titanic,
* The Avengers,
* Jurassic World,
* Furious 7,
* Avengers: Age of Ultron,
* Harry Potter and the Deathly Hallows: Part 2,
* Frozen,
* Iron Man 3

The top 10 movies with the highest budgets are:
* The Warrior's Way,
* Pirates of the Caribbean: On Stranger Tides,
* Pirates of the Caribbean: At World's End,
* Avengers: Age of Ultron,
* Superman Returns,
* John Carter,
* Tangled,
* Spider-Man 3,
* The Lone Ranger,
* The Hobbit: An Unexpected Journey

Based on the popularity score, the most popular movies are:
* Jurassic World,
* Mad Max: Fury Road,
* Interstellar,
* Guardians of the Galaxy,
* Insurgent,
* Captain America: The Winter Soldier,
* Star Wars,
* John Wick,
* Star Wars: The Force Awakens,
* The Hunger Games: Mockingjay - Part 1


In the year 2015, the highest revenue was generated ($26,762,450,518).

From 1961 to 2015, the highest number of movies were released in 2014 (700 movies).

Compared to other year, a lot of money was budgetted for movies in the year 2010 ($9,355,001,006).

To analyze the runtime, budget and revenue columns, I created a subset of the original dataset without any 0 value in the revenue and budget columns. After removing the 0 values, there were 3854 records.

The correlation between the budget and runtime variables is 0.26. There is a weak relationship between those variables.

The correlation between the revenue and runtime variables is 0.25. There is also a weak relationship between those variables.

The correlation between the revenue and budget variables is 0.69. There is a positive relationship between those variables. Further investigation is needed.

There is a strong positive correlation between the revenue and revenue_adj. The correlation coefficient is 0.90.

There is a strong positive correlation between the budget and budget_adj. The correlation coefficient is 0.96.

There is a weak relationship between vote_count and vote_average. The correlation coefficient is 0.25.

There is a high positive correlation between the vote count and popularity. The correlation coefficient is 0.80.

There is a positive correlation between the popularity of a movie and the revenue it generates. The correlation coefficient is 0.62. Remember, we are working with a subset of the original dataset (df_copy) with only 3854 records.

Between the years 1961 and 2015, the drama and comedy movie genres have the highest number of movies released. This comparison is limited to 14 genres which include Thriller, Action, Adventure, Sci-Fi, Animation, Comedy, Crime, Documentary, Drama, Fantasy, Horror, Music, Mystery, Romance.

Out of the following movie genres (Action, Adventure, Thriller, Drama, Sci-Fi)

* Adventure genre has generated the highest average revenue.
* Adventure, Action and Sci-Fi genres have the highest average budget.
* Adventure and Sci-Fi genres have the highest average vote count.
* Drama and Adventure genres have the highest average vote average.
* Drama and Adventure genres have the highest average runtime.


### Limitations

* 5696 movies in the dataset have 0 budget. 6016 movies in the dataset have 0 revenue. 31 movies have a runtime of 0. It is one of the limitations in the project. Movies do not have 0 runtime or 0 revenue. Although there are cases where a movies can have low-budget. To improve the result of the analysis, the 0 values need to be updated to the actual movie budget, and revenue.

* This dataset is limited to movies from 1961 to 2015. For better results, the dataset should be updated to include movies from 2016 to 2022.

* The analysis of the movie genres is limited to Action, Adventure, Thriller, Drama, and Sci-Fi.
