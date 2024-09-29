# Movie Recommendation System 

## Project Overview
This project implements a movie recommendation system that utilizes text vectorization techniques and cosine distance to recommend movies based on user input.

## Basic Steps and Process

### 1. **Data Collection**
   - Gathered a dataset of movies, including titles and associated tags or genres.

### 2. **Text Vectorization**
   - **Techniques Used**:
     - **Bag of Words**: Combined all words from movie tags and calculated the frequency of the top 5000 words to create a word frequency matrix.
     - **TF-IDF**: (Optional) Implemented to give weight to words based on their frequency across all documents.
     - **Word2Vec**: (Optional) Used for generating vector representations of words to capture semantic meanings.

### 3. **Vector Representation of Movies**
   - Constructed a 5000-dimensional vector for each movie, representing the frequency of the top words from the dataset.
   - Example of vector representation:
     ```
     | Movie Title    | w1 (Action) | w2 (Future) | ... | w5000 |
     |----------------|-------------|-------------|-----|-------|
     | First Movie    | 5           | 3           | ... | 0     |
     | Second Movie   | 4           | 2           | ... | 8     |
     ```
   - Data shape: (Number of Movies, 5000)

### 4. **Calculating Cosine Distance**
   - Used cosine distance to evaluate the similarity between movie vectors.
   - Calculated the cosine of the angle between vectors to measure similarity:
     \[
     \text{cosine\_similarity}(A, B) = \frac{A \cdot B}{||A|| \cdot ||B||}
     \]
   - Generated a cosine distance matrix for all movie pairs.

### 5. **Fetching Recommendations**
   - Implemented a function to find the closest 5 movie vectors to the user's input.
   - Presented recommendations based on the calculated cosine distances.

### 6. **Visualization**
   - Created visualizations (such as scatter plots) to illustrate the distribution of movie vectors and the similarity between them.

### 7. **Challenges Faced**
   - High-dimensional data complexity and the limitations of Euclidean distance.
   - Ensuring efficient calculations for cosine distance across potentially large datasets.

### 8. **Learning Outcomes**
   - Gained experience with text vectorization techniques and their application in real-world problems.
   - Improved understanding of cosine distance and its advantages over Euclidean distance in high-dimensional spaces.

## Conclusion
This project demonstrates how to effectively utilize text vectorization and similarity measures to create a recommendation system that can provide personalized movie suggestions based on user preferences.
