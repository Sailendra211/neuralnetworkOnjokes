Predicting the Funniest Joke: A Machine Learning Approach
This project implements a joke recommendation system using a combination of word-based predictions, neural embeddings, and a Random Forest classifier. The goal is to predict the best joke for a user based on the content of their next four favorite jokes.

📂 Project Structure
Dataset3JokeSet.xlsx — Dataset containing a collection of jokes.

jester-data-1.xls — Dataset containing user ratings for 100 jokes.

neuralnet_on_jokes.ipynb — Jupyter Notebook with data preprocessing, transformation, and model training.

📊 Datasets
Jokes Dataset:
Contains text jokes in a list format.

Ratings Dataset (Jester Dataset):
A matrix of user ratings for jokes, where:

Rows represent users.

Columns represent jokes.

Ratings range from -10 to 10, with 99 indicating missing values.

📝 Approach
This project takes a unique approach to joke recommendation:

Data Preparation

Load and clean both jokes and ratings datasets.

Convert ratings from wide to long format.

Joke Selection

For each user, identify their top 5 rated jokes.

Use the next 4 best jokes to predict the content (words) of their best-rated joke.

Word-Based Prediction

Predict the words of the user's favorite joke based on the words from their next four favorite jokes.

Neural Embedding

Create embeddings for joke IDs to represent them in a continuous space.

Classification Model

Use a Random Forest classifier to predict the user's top joke based on:

Neural embeddings of the next four favorite jokes.

Word prediction features.

🚀 Getting Started
Dependencies
Python 3.x

Pandas

Scikit-learn

(Optional) TensorFlow / Keras for embedding generation

Run Instructions
Clone the repository or download the files.

Install dependencies:

bash
Copy
Edit
pip install pandas scikit-learn
Open the notebook neuralnet_on_jokes.ipynb and run the cells sequentially.

📈 Model Highlights
Random Forest Classifier:
Trained on features generated from:

Predicted joke words.

Neural joke embeddings.

No collaborative filtering used.
The model relies entirely on content-based prediction and embedding features.

📚 Acknowledgments
Jester Joke Dataset

Inspired by text-based recommender systems and feature-based classification.

