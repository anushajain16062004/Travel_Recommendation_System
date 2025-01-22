# Travel_Recommendation_System


### Step 1: Data Preparation
- **Import Libraries**: Key libraries include `pandas`, `numpy`, `scikit-learn`, and `matplotlib`.
- **Load Data**: Datasets such as `destinations_df`, `reviews_df`, `userhistory_df`, and `users_df` are loaded from CSV files.
- **Merge Datasets**: The data is merged step-by-step based on common columns like `DestinationID` and `UserID` to create a comprehensive dataset.

### Step 2: Data Visualization
- **Popularity of Destinations**: A bar plot shows the most popular destinations.
- **Distribution of Destination Types**: A count plot visualizes the distribution of different types of destinations.
- **Best Time to Visit**: A count plot shows the most common times to visit each destination.
- **Ratings Distribution**: A histogram displays the distribution of ratings given by users.

### Step 3: Recommendation Models
#### 3.1 Content-Based Filtering
- **Feature Creation**: Combine features like `Type`, `State`, `BestTimeToVisit`, and `Preferences` into a single text feature.
- **TF-IDF Vectorization**: Apply `TfidfVectorizer` to create feature vectors for destinations.
- **Cosine Similarity**: Compute the cosine similarity between destinations based on these features.

#### 3.2 Collaborative Filtering
- **User-Item Matrix**: Create a matrix representing user ratings or experiences with destinations.
- **Cosine Similarity Between Users**: Calculate similarity between users based on the user-item matrix.
- **Recommendation Function**: Recommend destinations based on the similarity scores of similar users.

### Step 4: User Input-Based Recommendation
- **Random Forest Regressor**: Use a machine learning model to predict the popularity of a destination based on user input.
- **Encode Categorical Variables**: Use `LabelEncoder` to encode categorical variables such as `State`, `Type`, and `Preferences`.
- **Model Training**: Split the data into training and test sets, train a Random Forest model, and evaluate its performance using metrics like Mean Squared Error and R² Score.

### Step 5: Final Prediction
- **User Input**: The user provides input such as destination name, type, state, and preferences.
- **Prediction**: The model predicts the popularity of the destination based on the user input.

### Step 6: Saving Models
- **Save Model**: Save the trained model and label encoders using `pickle` for future use.

This project provides a comprehensive approach to building a recommendation system using machine learning, blending content-based filtering, collaborative filtering, and user input-based recommendations.
