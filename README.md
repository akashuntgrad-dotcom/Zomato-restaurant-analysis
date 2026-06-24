# 🍽️ Zomato Restaurant Analysis

End-to-end data analysis project exploring restaurant performance on Zomato — covering online ordering, table booking, pricing strategy, restaurant format, and market positioning. Built in Python using Jupyter Notebook.

## 📌 Business Problem

Does going digital (online ordering, table booking) actually pay off for restaurants on Zomato? And more broadly — what combination of format, price, and features gives a restaurant the best odds of success on the platform?

## 📊 Dataset

148 restaurants listed on Zomato, with the following fields:

| Column | Description |
|---|---|
| `name` | Restaurant name |
| `online_order` | Accepts online orders (Yes/No) |
| `book_table` | Allows table booking (Yes/No) |
| `rate` | Customer rating (out of 5) |
| `votes` | Number of customer votes |
| `approx_cost(for two people)` | Approximate cost for two people (₹) |
| `listed_in(type)` | Restaurant format (Dining, Cafes, Buffet, Other) |

## 🔍 Key Insights

- **Digital features drive ratings:** Both online ordering (p < 0.0001) and table booking (p = 0.0011) are statistically significantly linked to higher restaurant ratings.
- **Price is a weak predictor of quality:** Cost-for-two has only a weak correlation with rating (r = 0.275) — charging more doesn't reliably buy a better reputation.
- **Format matters:** Restaurant type significantly affects rating (ANOVA, p = 0.0116). Dining restaurants combine solid ratings with by far the highest vote volumes — the most reliable format at scale.
- **Votes and ratings reinforce each other:** Popular restaurants tend to be rated higher, suggesting a feedback loop between visibility and perceived quality.
- **Table booking is a "premium" signal:** It's adopted mostly by higher-cost, full-service "Dining" restaurants, not casual cafes or buffets.
- **Market segmentation:** K-Means clustering on rating, votes, and cost reveals natural restaurant archetypes (e.g., "hidden gems," "premium leaders," "mass-market reliable") beyond simple price tiers.

## 🛠️ Tools Used

Python · Pandas · NumPy · Matplotlib · Seaborn · SciPy (hypothesis testing) · Scikit-learn (clustering) · Jupyter Notebook

## 📁 Project Structure

```
zomato-restaurant-analysis/
├── README.md
├── Zomato_Analysis.ipynb              # Focused analysis: online ordering & table booking impact
├── Zomato_Multi_Lens_Analysis.ipynb   # Multi-angle analysis: format strategy, pricing, clustering, opportunity scoring
├── Zomato-data-.csv                   # Dataset
├── requirements.txt
└── .gitignore
```

### Notebook 1 — `Zomato_Analysis.ipynb`
Focused storytelling around Zomato's platform strategy: does online ordering / table booking adoption correlate with better restaurant performance? Includes data cleaning, EDA, hypothesis testing, and business recommendations.

### Notebook 2 — `Zomato_Multi_Lens_Analysis.ipynb`
A deeper, multi-stakeholder analysis covering:
- 🏗️ Format strategy (which restaurant type performs best)
- 💰 Pricing & value-for-money analysis
- 🎯 Quality consistency (what actually drives ratings)
- 📈 Market-entry / investor lens (best format × price combination)
- 🧩 K-Means clustering for market segmentation
- 🏆 A composite "Opportunity Score" ranking restaurants holistically

## 🚀 How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/zomato-restaurant-analysis.git
   cd zomato-restaurant-analysis
   ```
2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```
3. Launch Jupyter and open either notebook
   ```bash
   jupyter notebook
   ```
4. Run all cells (`Kernel → Restart & Run All`)

## 📈 Sample Visuals
<img width="642" height="472" alt="download" src="https://github.com/user-attachments/assets/0a9a37ec-8f68-47e0-a820-51bc0f020062" />

<img width="1587" height="487" alt="download" src="https://github.com/user-attachments/assets/9dffa724-2631-423e-9a9b-90af83ad1cbb" />

<img width="626" height="549" alt="download" src="https://github.com/user-attachments/assets/21afb9cf-a030-4d69-954c-1315e3d142c5" />

<img width="626" height="549" alt="download" src="https://github.com/user-attachments/assets/516c7bf7-bc25-468f-a0ec-bf719903e67f" />



## ⚠️ Limitations

- Sample size (148 restaurants) is modest — segment-level conclusions for rare categories (e.g. Buffet) are directional, not definitive.
- No location, cuisine, or time-series data — these could be confounding variables.
- Clustering and scoring are descriptive tools, not predictive/causal models.

## 👤 Author

Akashdeep Boxi · [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/akashdeep-boxi-130a803a4)<img width="642" height="472" alt="download" src="https://github.com/user-attachments/assets/492fe703-053d-4bbc-ae6f-898d290f5dbf" />
 · akashuntgrad@gmail.com
