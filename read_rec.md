## Reading Recommender

![](read_rec_gif.gif)

#### Summary:
Are you ready to take your next literary journey? With the Reading Recommender app, fill out a short survey on
your reading preferences and get recommended one of the top rated books in all of history. [VISIT APP HERE](https://ceareads.netlify.com/), [VIEW CODE HERE](https://github.com/reading-recommender)

#### Technical Overview:
The goal of this project was to use Machine Learning models to recommend a book based on a user's survey results. To quickly pull in book data, the Python package Beautiful Soup was used to scrape a book list online. Hand-labeling books with survey responses was a not-so-quick task, as it took reading the synopsis of each book to come up with the correct survey responses. The responses were then used to train a Random Forest Classifier model.

The model was pickled (serialized) to be used in production. Flask was used to build an API that received a JSON object of survey responses from the front-end, then pass the JSON object to the pickled Random Forest Classifier model and then return a JSON object of the recommended book.

The biggest challenge of this project was the inability to label enough data due to time constraints. A more automated data labeling approach -- possibly through topic modeling or rule-based classification -- would have given users a wider range of book recommendations.

#### Technology Used:
- Pandas
- Beautiful Soup
- Scikit-learn
- Flask
