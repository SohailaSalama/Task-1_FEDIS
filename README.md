# Task-1_FEDIS
# Task 1: Movie Recommendation System

## Project Overview
This project demonstrates the development of a movie recommendation system using user-movie interaction data. The goal is to provide personalized movie suggestions based on past interactions, similarity calculations, and vector-based search.

## Steps Implemented

### Step 1: Create the Interaction Matrix
- Extracted user interactions (userId and movieId) from the dataset.
- Converted interactions into binary format: watched = 1, not watched = 0.
- Built a user-item interaction matrix to facilitate similarity calculations.

### Step 2: Calculate Similarity
- Used cosine similarity to measure similarity between users (User-Based Collaborative Filtering) or items (Item-Based CF).
- Represented similarity scores in a matrix format for further processing.

### Step 3: Build the Recommendation Logic
- Selected a target user.
- Identified top-N similar users/items using similarity scores.
- Extracted items interacted by similar users but not yet by the target user.
- Ranked items by frequency/popularity and returned the top-N recommendations.

### Step 4: Improve the Output
- Mapped item IDs (movieId) to movie titles using a secondary dataset.
- Updated recommendation function to return readable movie titles.

### Step 5: Use a Vector Database (ChromaDB)
- Converted each user's interaction row into a binary vector.
- Stored all user vectors in ChromaDB.
- Replaced manual similarity calculations with vector similarity search.
- Queried similar users and retrieved recommendations.

### Step 6: Test the System
- Tested the recommender with different users to ensure valid outputs.
- Considered edge cases:
  - Users with no history
  - Items with very few interactions
  - Extremely popular items

## Libraries and Tools
- Python
- Pandas, NumPy
- Scikit-learn
- ChromaDB
- Jupyter Notebook

## How to Run
1. Clone the repository.
2. Install required libraries (see `requirements.txt` if provided).
3. Open the notebook `Task1-RecommendationSystem.ipynb`.
4. Run each cell to reproduce the analysis and recommendation results.

## Output
The system outputs the top-N recommended movies for a given user, showing movie titles and a relevance score.

