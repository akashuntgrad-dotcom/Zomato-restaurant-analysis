# 🍽️ Zomato Restaurant Analysis

End-to-end data analysis project exploring restaurant performance on Zomato covering online ordering, table booking, pricing strategy, restaurant format, and market positioning. Built in Python using Jupyter Notebook.

## 📌 Business Problem

Does going digital (online ordering, table booking) actually pay off for restaurants on Zomato? And more broadly what combination of format, price, and features gives a restaurant the best odds of success on the platform?

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
- **Price is a weak predictor of quality:** Cost-for-two has only a weak correlation with rating (r = 0.275) charging more doesn't reliably buy a better reputation.
- **Format matters:** Restaurant type significantly affects rating (ANOVA, p = 0.0116). Dining restaurants combine solid ratings with by far the highest vote volumes the most reliable format at scale.
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

<img width="635" height="470" alt="download" src="https://github.com/user-attachments/assets/ad147343-e0b4-4b46-839e-3f8f88f0694d" />

<img width="1387" height="487" alt="download" src="https://github.com/user-attachments/assets/727d01ee-3b23-4825-90ed-ee61714a484c" />

<img width="506" height="451" alt="download" src="https://github.com/user-attachments/assets/1da257b8-7d49-415a-abbe-2e98dc11547d" />

<img width="1037" height="487" alt="download" src="https://github.com/user-attachments/assets/dac58c0d-20c2-4296-945f-45f1fc5db870" />

<img width="626" height="549" alt="download" src="https://github.com/user-attachments/assets/94e6dd76-0eb3-4a40-aeef-d3321dfbed8a" />



## ⚠️ Limitations

- Sample size (148 restaurants) is modest — segment-level conclusions for rare categories (e.g. Buffet) are directional, not definitive.
- No location, cuisine, or time-series data — these could be confounding variables.
- Clustering and scoring are descriptive tools, not predictive/causal models.

## 👤 Author

Akashdeep Boxi · [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/akashdeep-boxi-130a803a4) · akashuntgrad@gmail.com
