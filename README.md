# 🎬 Movie Mashup: Hybrid Recommendation System

![Pipeline Overview](https://github.com/RidhyHira/The-Movie-Mashup/blob/master/Overview.png)

A unified movie recommendation system that combines **IMDb ratings** and **TMDB regional metadata** to deliver personalized suggestions with regional and cultural relevance.

## 🚀 Key Features

- **Dual-Source Integration**: Leverages both IMDb (ratings/popularity) and TMDB (regional metadata).
- **Smart Filtering**: User-specific filters for language, region, content ratings, and genres.
- **Data Enrichment**: Cleans and standardizes multi-source data for consistency.
- **Hybrid Recommendations**: Combines ratings + content-based filtering.

## 📊 Pipeline Architecture

1. **Data Ingestion**  
   - IMDb: Content ratings, movie ratings (`averageRating`, `numVotes`).  
   - TMDB: Region-specific details (dubbed languages, local titles).  

2. **Data Processing**  
   - **Genre Ranking**: Genre based ranking of movies.  
   - **Missing Value Handling**: Imputes gaps in year, language, genre or ratings.  

3. **User Filtering**  
   - Applies preferences (e.g., "Exclude R-rated", "Only Spanish-language").  
  

## 📂 Dataset

- **Source**: [IMDb Non-Commercial Datasets](https://www.imdb.com/interfaces/)  
