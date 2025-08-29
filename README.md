<img width="405" height="764" alt="image" src="https://github.com/user-attachments/assets/4472942d-0b37-4f25-9779-8c5647aa9cba" /># IMDB_Movie_Analysis
**Project Description**
The IMDB Movie Analysis project focused on exploring different aspects of movies such as genres, durations, languages, directors, and budgets to evaluate their impact on IMDB scores and overall financial success.
•	Before performing the analysis, data cleaning was carried out:
•	Removed blank rows from the dataset.
•	Deleted duplicate values to maintain accuracy.
•	Handled missing values and reformatted columns.
•	Separated multiple genres in the genres column for accurate analysis.
The goal of the project was to apply Excel-based analytical and statistical techniques to derive meaningful insights and highlight trends in the movie industry.
________________________________________
•	**Approach**
A structured step-by-step workflow was followed to complete the project:
1.	**Data Cleaning & Preparation**
o	Removed blank rows, duplicates, and corrected missing entries.
o	Reformatted the dataset and split multiple genres for accurate categorization.
2.	**Genre Analysis**
o	Used COUNTIF to identify the most common genres.
o	Calculated descriptive statistics of IMDB scores (mean, median, mode, variance, standard deviation, range) for each genre.
3.	**Duration Analysis**
o	Computed mean, median, and standard deviation for movie durations.
o	Designed a scatter plot of duration vs IMDB score with a trendline to study correlation.
4.	**Language Analysis**
o	Applied COUNTIF to find the most frequent movie languages.
o	Calculated descriptive statistics of IMDB scores by language and compared results.
5.	**Director Analysis**
o	Calculated the average IMDB score per director.
o	Ranked directors using PERCENTILE calculations.
o	Compared top-performing directors to the overall score distribution.
6.	**Budget Analysis**
o	Used CORREL to measure the relationship between budget and gross earnings.
o	Calculated profit (Gross – Budget) and profit margin (Profit / Budget × 100).
o	Identified the Top 10 movies with the highest profit margins using MAX and LARGE.
________________________________________
•	**Tech-Stack Used**
•	Microsoft Excel (Office 365)
________________________________________

•	**Insights**
•	Genres: Drama and Action were the most common, but some niche genres scored higher in IMDB ratings.
•	Durations: Medium-length movies generally performed better than very short or very long ones.
•	Languages: English dominated the dataset, though some regional languages had competitive ratings.
Task 1
Determine the most common genres of movies in the dataset. Then, for each genre, calculate descriptive statistics (mean, median, mode, range, variance, standard deviation) of the IMDB scores.
Result
=COUNTIF(A:A,"*Action*")
=COUNTIF(A:A,"*Adventure*")
=COUNTIF(A:A,"*Drama*")
And so on
<img width="405" height="764" alt="image" src="https://github.com/user-attachments/assets/6fad968c-1f05-4d53-8da5-85372512c306" />
Most common genres
 <img width="586" height="88" alt="image" src="https://github.com/user-attachments/assets/a80dddb7-61df-4fa4-a22e-78133d54d53e" />
Descriptive statistics (mean, median, mode, range, variance, standard deviation) of the IMDB scores.
<img width="1111" height="263" alt="image" src="https://github.com/user-attachments/assets/c3c75e28-7a87-4116-a576-4140dc8faf73" />

 
________________________________________
Task 2 Analyze the distribution of movie durations and identify the relationship between movie duration and IMDB score.
Result:

 <img width="1089" height="334" alt="image" src="https://github.com/user-attachments/assets/fbb9db34-20d3-49a1-ade0-428acb5e4604" />
 <img width="1016" height="614" alt="image" src="https://github.com/user-attachments/assets/c133a762-5c48-4d43-9ad4-7b52c5e527f6" />



 
________________________________________

Task3 Determine the most common languages used in movies and analyze their impact on the IMDB score using descriptive statistics.

Result: 
In this task firstly I remove all duplicates value and for removing the duplicates value I used remove duplicates formula. And then I used Countif formula.
=COUNTIF(A:A, "English")
And so on for all language
<img width="786" height="1033" alt="image" src="https://github.com/user-attachments/assets/6f73a40e-d58c-4d84-a1c2-00271b651103" />
 
Then I extract descriptive analytics for each language
1.	Mean (Average IMDb score per language) 


2.	Median  IMDB score per language
3.	Standard Deviation (Variation in scores per language)
=AVERAGEIF(A:A,D2,B:B)
=MEDIAN(IF(A:A=D2,B:B))
=STDEV.S(IF(A:A=D2,B:B))
We get some result (#DIV/0!) in stdev.s because the language analysis is 1.
=COUNTIF(A:A, "English") (for each languge) use for language analysis.
<img width="1089" height="759" alt="image" src="https://github.com/user-attachments/assets/3af3d039-8b88-475d-b205-a9affdfa0904" />
 
____________________________________
 
Task 4 Identify the top directors based on their average IMDB score and analyze their contribution to the success of movies using percentile calculations.
Result
The objective of this analysis is to evaluate the influence of directors on movie success by calculating their average IMDB scores, number of movies directed, and their percentile ranking among all directors.
 
<img width="1090" height="613" alt="image" src="https://github.com/user-attachments/assets/e42d8b12-4221-4f8b-8387-60a01af6df2b" />


And then I extract comparision of average IMDB vs percentile.inc
And then I use pivot table to get top 10 director name
To get Unique Director Name by Remove Duplicates Function
And for comparision of averageIMDB vs percentile.inc I use
=IF(F2>=Table13[@[PERCENTILE.INC]],"Top 10%","Others")

 <img width="1089" height="1175" alt="image" src="https://github.com/user-attachments/assets/eb83dfb3-3d7f-47f5-ba65-90992665d263" />

  and the result of the pivot table is 
  <img width="394" height="389" alt="image" src="https://github.com/user-attachments/assets/d3c23c52-455b-4af4-9211-df6b46f37f8f" />

 
________________________________________
Task5 : Analyze the correlation between movie budgets and gross earnings, and identify the movies with the highest profit margin.
Result:
For this analysis I found profit by substracting gross into budgets
=A2-B2  and for correlation I use =CORREL(A:A,B:B) 

 <img width="1031" height="766" alt="image" src="https://github.com/user-attachments/assets/bb51666e-3ace-4fce-91ed-cfedc5e1a083" />

And than to identify the movies with the highest profit margin. I use MAX function and (=profit/budget*100)
<img width="423" height="1112" alt="image" src="https://github.com/user-attachments/assets/72039377-4dbc-4cdb-92db-a631977ccba2" />

 
For this I use (=profit/budget*100)
<img width="550" height="317" alt="image" src="https://github.com/user-attachments/assets/57fe9ff1-1a88-45e4-b7fc-0e2287a688f6" />

 
Hight profit margin by Max function






•	Directors: A few directors consistently ranked in the top percentiles, showing their strong influence on ratings.
•	Budgets: Large budgets often resulted in higher grosses, but ROI was higher for several low- to mid-budget movies.
