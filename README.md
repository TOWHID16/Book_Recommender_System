## Book Recommender System 📚
A web-based book recommendation system that suggests books to users based on overall popularity and personalized collaborative filtering. This project is built with Python, Pandas, and Scikit-learn, with a user-friendly interface created using Flask.

## 🚀 Live Demo
You can view the live deployed application here: </br>
https://book-recommender-system-v20n.onrender.com/

## Features
This recommender system operates in two modes:

 Popularity-Based Recommendations: Provides a list of the top 50 most popular and highly-rated books. This is perfect for new users who are looking for a generally good read.

 Collaborative Filtering Recommendations: When a user selects a book they like, the system suggests similar books. This personalized recommendation is based on the preferences of other users who also enjoyed the selected book (Item-Based Collaborative Filtering).

## Screenshots
Here's a glimpse of the application in action.</br>
Homepage & Top 50 Books:</br>
A user can browse the most popular books or select one to get recommendations.

![Alt text](https://github.com/TOWHID16/Book_Recommender_System/blob/main/assets/page%201.PNG)

Recommendation Results:</br>
After selecting a book, the system displays a list of similar books with their covers and authors.

![Alt text](https://github.com/TOWHID16/Book_Recommender_System/blob/main/assets/page%202.PNG)

## Technologies Used
<b>Backend:</b> Python, Flask

<b>Data Manipulation:</b> Pandas, NumPy

<b>Machine Learning:</b> Scikit-learn (for K-Nearest Neighbors and Cosine Similarity)

<b>Deployment:</b> Gunicorn, Render

<b>Dataset:</b> [Book-Crossing Dataset on Kaggle](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset)

## How It Works
The recommendation logic is based on two different models:

1. Popularity-Based Model
This model identifies books that are both highly rated and have a significant number of ratings.

Books with less than 250 total ratings are filtered out to ensure statistical significance.

The remaining books are ranked based on their average rating.

The top 50 books from this list are presented to the user.

2. Collaborative Filtering Model
This model finds books that are "similar" based on user rating patterns.

A user-item matrix is created from the ratings data, with users as rows and book titles as columns.

The matrix is extremely sparse, so it's filtered to include only users who have rated more than 200 books.

Cosine Similarity is used to calculate a similarity score between every pair of books.

When a user selects a book, the system retrieves the top 5 most similar books from the pre-computed similarity matrix to provide a personalized recommendation.

## How to Run This Project Locally
To set up and run this project on your local machine, follow these steps:

<b>1. Clone the repository:</b>

<b>Bash<b>

```https://github.com/TOWHID16/Book_Recommender_System.git``` </br>
```cd your-repo-name``` </br>


<b>2. Create a virtual environment:</b>

<b>Bash</b>

```python -m venv venv``` </br>
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`


<b>3. Install the required dependencies:</b>

<b>Bash</b>

```pip install -r requirements.txt```


<b>4. Run the Flask application:</b>

<b>Bash</b>

```python app.py```</br>
Open your web browser and navigate to ```http://127.0.0.1:5000``` to see the application.

## Acknowledgements
This project is based on the Book-Crossing Dataset.

Inspiration and guidance from various data science and web development tutorials.
