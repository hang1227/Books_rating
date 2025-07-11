# Books_rating
Goodreads established in 2007, which is one of the largest platform that allow readers to discover, rate, and review the books. With million of users, Goodreads acts as a book discovery engine and a community hub for a literature lovers worlwide. The company have significant amount of data on its book details, user rating and review. This project thoroughly analyze the data in order to uncover the critical insight that will improve the Goodreads platform in its business. 

Insights and recommendations are provided on the following key areas:
  - the top rating of the books by readers - the average rating of the books
  - the popularity of books in Goodreads platform - the count of the reader rating
  - the rating consistency of each book - the standard deviation of the rating 

Data Structure:
Goodreads data structure consists of five tables: books, ratings, to_read, book_tags, and tags with each table contains more than 900k data. (Datasource: https://www.kaggle.com/datasets/zygmunt/goodbooks-10k)
<img width="1035" height="524" alt="image" src="https://github.com/user-attachments/assets/5dc7bd9e-f5c5-403a-bb35-26f1b989ef1a" />
Prior to beginning the analysis, data cleaning had been performed in python to screen through the data if have any null values and replace it with the correct data format. The code is presented as below:
<img width="784" height="306" alt="image" src="https://github.com/user-attachments/assets/76c41ae5-f192-4b5f-adc3-9e6ad68499c8" />

After done cleaning, the data is transformed to CSV again for data analysis in PostgreSQL. Analysis is started with the ratings table to generate the average ratings for each book, the reader rating count, and the standard deviation of the rating in one table using CTE and consolidate it with the books table. The consolidated table will be used for data visualization in Tableau. 

The sql code is shown as below:
<img width="1022" height="279" alt="image" src="https://github.com/user-attachments/assets/5ce1181f-fe14-4702-9191-12086b9a0d96" />

The joining table:
<img width="1498" height="772" alt="image" src="https://github.com/user-attachments/assets/454ce579-8af2-4676-8e36-651c2ffc5b79" />

Executive summary:
Top ten rated books in Goodreads platform has been summarized with its average rating, std rating, and number of rating for each book by readers.Below is the chart that genearated in Tableau. 

<img width="1216" height="809" alt="Sheet 2" src="https://github.com/user-attachments/assets/610aa7cc-e5be-4fc6-9aa7-f34796ad1781" />

Average book rating:
1. Most of the books fall within a tight range between 4.50 and 4.66, suggesting consistently positive reception across the list.
2. "Still Life with Woodpecker" has the highest average rating at 4.7778, indicating strong reader satisfaction.

Standard deviation of rating:
1. Standard deviation reveals how consistent the ratings are among readers.
2. "Still Life with Woodpecker" again stands out with the lowest std dev (0.4641), which means that the readers are mostly have a good review on this books.
3. "Peter and the Shadow Thieves" has the highest std dev (0.8100), indicates more diverse or polarized opinions.
4. Most books have a moderate deviation (around 0.6–0.7), showing some variation but generally consistent feedback.

Rating count 
1. All books have high engagement, with most receiving 96–100 ratings.
2. "Peter and the Shadow Thieves" has the lowest count (70), which might explain its high standard deviation due to fewer ratings often show more variability.
3. 

