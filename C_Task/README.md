# Task B
Design and develop a recommendation system using collaborative filtering or content-based filtering techniques. Explain how you would handle data preprocessing, similarity calculations, and recommendation generation.

## My Approach
I have here developed a collaborative filtering model. It makes prediction about interest of a user by collecting preferences from many users.<br>

### Steps Involved
• I started by reading and merging the dataset from the various `.dat` files into a single DataFrame. The database contains data of 11350 users from steam across 360 Games.<br>
• Initially I merged the databse and created a pivot table named `data_pivot` whose each row represents a unique user, each column represents a unique game, and the values represent the number of hours that the user has played that game.<br> 
• A NumPy array based `data_matrix` is created with rows representing users, columns representing games, and values representing the number of hours played. Any missing value is replaced with a 0. It has the same shape as `data_pivot`.<br>
• Similarity calculations are performed using the `pairwise_distances` function from scikit-learn with the cosine similarity metric. This calculates the pairwise cosine similarities between all users in the `data_matrix`.
• The `predict` function takes as input a `data_matrix` and a similarity matrix. It makes predictions and returns the predicted ratings for all users by taking a weighted average of all other user's ratings.
