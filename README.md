# Movie Recommendation Engine (Content-Based)

A personalized movie recommender system built using a **content-based filtering approach**.  
This system analyzes movie features (genre, director, cast, description, etc.) and suggests titles that share similar characteristics with the movies a user already likes.

---

##  How It Works

Unlike collaborative filtering, which depends on the preferences of other users, **content-based filtering** focuses solely on the **attributes of the items** themselves.  

For example, if you liked *Inception*, the system may recommend *Interstellar* because both share a similar genre, director, and thematic style.

---

##  API Setup for Movie Data & Images

This project uses the **TMDB API** to fetch posters and additional details.  

1. Create an account at [The Movie Database (TMDB)](https://www.themoviedb.org/).  
2. Go to **Account Settings → API**.  
3. Submit the application (you can put `"NA"` for Website URL if you don’t have one).  
4. Copy the API key from the dashboard after approval.  

---

## Similarity Score

The system measures similarity between movies using **cosine similarity**, which returns a score between **0 and 1**:  

- **0** → no similarity  
- **1** → perfect similarity  

###  Why Cosine Similarity?  
- Considers the **angle between vectors**, not their magnitude.  
- Works well for text data of varying lengths.  
- Smaller angles = higher similarity.  

---

##  Workflow

1. **Dataset** → [TMDB 5000 Movies Dataset](https://www.kaggle.com/tmdb/tmdb-movie-metadata)  
2. **Feature Engineering** → Combine metadata such as genre, keywords, cast, and crew  
3. **Vectorization** → Transform text data into numerical vectors  
4. **Similarity Calculation** → Apply cosine similarity  
5. **Recommendation** → Suggest top-N similar movies  

---

## Installation & Setup

Clone the repository:

```bash
git clone https://github.com/your-username/movie-recommender.git
cd movie-recommender
