# Facebook Marketplace Live Sellers — Data Analysis

An exploratory data analysis project examining engagement patterns, correlations, and clustering insights from 7,050 Facebook Live Seller posts spanning 2012–2018.

---

## Overview

This project analyses a dataset of Facebook Live Seller posts sourced from the **UCI Machine Learning Repository**. The goal is to uncover what drives engagement — reactions, comments, and shares — and to segment posts into meaningful clusters using unsupervised machine learning.

The analysis addresses six core questions:

1. How does upload time (hour, day, year) affect the number of reactions?
2. What is the correlation between reactions, comments, and shares?
3. How do posts cluster using K-Means on engagement features?
4. What is the optimal number of clusters, determined by the Elbow Method?
5. What is the distribution of post types in the dataset?
6. How does average engagement vary across post types?

---

## Dataset

| Attribute       | Details                              |
|-----------------|--------------------------------------|
| **Source**      | UCI Machine Learning Repository      |
| **Total Posts** | 7,050                                |
| **Columns**     | 16                                   |
| **Date Range**  | 2012–2018                            |
| **Post Types**  | Photo, Video, Status, Link           |

### Column Reference

| Column             | Description                                      |
|--------------------|--------------------------------------------------|
| `status_id`        | Unique identifier for each post                  |
| `status_type`      | Type of post: photo, video, status, or link      |
| `status_published` | Timestamp when the post was published            |
| `num_reactions`    | Total number of reactions                        |
| `num_comments`     | Total number of comments                         |
| `num_shares`       | Total number of shares                           |
| `num_likes`        | Number of "Like" reactions                       |
| `num_loves`        | Number of "Love" reactions                       |
| `num_wows`         | Number of "Wow" reactions                        |
| `num_hahas`        | Number of "Haha" reactions                       |
| `num_sads`         | Number of "Sad" reactions                        |
| `num_angrys`       | Number of "Angry" reactions                      |

---

## Key Findings

**Timing matters.** Engagement peaks between 18:00–20:00 (6–8 PM), with Thursday consistently driving the highest average reactions. The year 2015 represented a historic peak, after which engagement stabilised at a lower baseline through 2018.

**Comments drive shares, not reactions.** Pearson correlation analysis reveals a strong positive relationship between comments and shares (r = 0.64), while the reaction–comment and reaction–share links are both weak. Sparking conversation is the most reliable predictor of virality.

**Six meaningful audience segments exist.** The Elbow Method identifies K = 6 as the optimal number of clusters, revealing audience segments that go beyond the simple photo/video split.

**Content type shapes engagement profile.** Photos are the most common post type (60.8%), but link posts generate the highest average reactions per post. Video excels at driving both comments and shares. Status (text-only) posts show the lowest engagement across all metrics.

---

## Project Structure

```
├── Facebook_Marketplace_Analysis.pdf   # Presentation summarising findings
├── Facebook_Marketplace_data.csv       # Raw dataset (7,050 posts)
├── [Facebook_Marketplace_data.ipynb](https://colab.research.google.com/drive/1pZQGjB1uIe9bPXK9vpC5Tyb5JsHpKHMh?usp=sharing)     # Analysis notebook (full code)
└── README.md
```


---

## Technologies Used

- **Python 3**
- **Pandas** — data loading, cleaning, and feature engineering
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **Scikit-learn** — K-Means clustering, OneHotEncoder, StandardScaler, ColumnTransformer

---

## Methodology

**Q1 — Upload Time vs. Reactions:** The `status_published` timestamp was parsed into hour, day of week, and year features. Average reactions were computed across each dimension and visualised as line plots.

**Q2 — Correlation Analysis:** Pearson correlation coefficients were computed for all pairwise combinations of `num_reactions`, `num_comments`, and `num_shares`. A custom function classifies each result by strength (weak/moderate/strong) and direction (positive/negative).

**Q3 & Q4 — K-Means Clustering:** Ten features were selected (`status_type` plus nine engagement metrics). `status_type` was one-hot encoded via `ColumnTransformer`; all numerical features were standardized with `StandardScaler`. K-Means was first trained with K = 3, then the Elbow Method was applied over K = 1–10 to identify K = 6 as optimal. The final model was trained with `n_clusters=6` and `init='k-means++'`.

**Q5 & Q6 — Post Type Analysis:** Post counts and average engagement metrics (reactions, comments, shares) were computed by post type and visualised as bar charts.

---

## Author

**Om A. Channawar**
MIT Academy of Engineering

---

## Copyright

© 2024 Om A. Channawar.

This project is shared for **educational and portfolio purposes**.  
The dataset used in this project is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/) and follows its usage terms.
