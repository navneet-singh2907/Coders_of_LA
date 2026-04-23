# Coders of LA: Social Graph & Recommendation Engine

**Coders of LA** is a Python-based data engineering project that transforms raw, inconsistent social data into a structured interest graph. 
The engine implements custom recommendation algorithms to simulate the core features of modern social media platforms.

## Key Features

### 🛠 Data Cleaning & Normalization
Real-world data is often incomplete or improperly formatted. This project implements a robust cleaning pipeline to handle:
* **Missing Keys:** Uses defensive programming to prevent crashes when data fields are absent.
* **Null Handling:** Effectively manages `null` values (NoneType) to maintain loop stability.
* **Type Casting:** Ensures IDs and metrics are normalized for mathematical operations.
* **Deduplication:** Cleans redundant records and friend lists using efficient set theory.

### People You May Know (PYMK)
A second-degree connection engine that identifies potential social links.
* **Mutual Friend Scoring:** Ranks suggestions based on the frequency of shared connections.
* **Optimized Lookups:** Leverages Python dictionaries and sets for $O(1)$ search performance.

### Pages You Might Like
An interest-based recommendation system utilizing **User-User Collaborative Filtering**.
* **Similarity Weighting:** Calculates a "Taste Similarity" score based on shared liked pages.
* **Weighted Ranking:** Suggestions from users with highly similar profiles are prioritized over generic popular content.

## Tech Stack
- **Language:** Python 3.x
- **Data Storage:** JSON
- **Version Control:** Git & GitHub
- **Algorithms:** Set Theory, Collaborative Filtering, Frequency Ranking

## Engineering Highlights
* **Zero-Library Logic:** Built entirely in pure Python to demonstrate algorithmic mastery without external dependencies.
* **Edge Case Resilience:** Specifically engineered to handle "Orphaned IDs" and "NoneType" objects during data traversal.
* **Scalable Architecture:** Designed with time complexity in mind, prioritizing set intersections over nested list iterations.

