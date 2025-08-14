# 🎬 Movie Mashup: Hybrid Recommendation System

![Pipeline Overview](https://github.com/RidhyHira/The-Movie-Mashup/blob/master/Overview.png)

A unified movie recommendation engine that combines **IMDb ratings** and **TMDB regional metadata** to deliver hyper-personalized suggestions with regional and cultural relevance.

## 🚀 Key Features

- **Dual-Source Integration**: Leverages both IMDb (ratings/popularity) and TMDB (regional metadata).
- **Smart Filtering**: User-specific filters for language, region, content ratings, and genres.
- **Data Enrichment**: Cleans and standardizes multi-source data for consistency.
- **Hybrid Recommendations**: Combines collaborative + content-based filtering.

## 📊 Pipeline Architecture

1. **Data Ingestion**  
   - IMDb: Content ratings, movie ratings (`averageRating`, `numVotes`).  
   - TMDB: Region-specific details (dubbed languages, local titles).  

2. **Data Processing**  
   - **Genre Cleaning**: Normalizes genres (e.g., "Sci-Fi" → "Science Fiction").  
   - **Missing Value Handling**: Imputes gaps in year, language, or ratings.  

3. **User Filtering**  
   - Applies preferences (e.g., "Exclude R-rated", "Only Spanish-language").  

4. **Recommendation Engine**  
   - Hybrid model using:  
     - **Content-Based**: Cosine similarity on genres/year/language.  
     - **Collaborative**: KNN on user-movie interactions (if available).  

## 📂 Dataset

- **Source**: [IMDb Non-Commercial Datasets](https://www.imdb.com/interfaces/)  
- **Sample Schema:**
  ```csv
  tconst,titleType,primaryTitle,startYear,genres,averageRating,numVotes
  tt0111161,movie,The Shawshank Redemption,1994,Drama,9.3,2500000
