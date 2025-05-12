# 🏀 NBA Player Archetypes using PCA and KMeans Clustering

This project analyzes NBA player season statistics from 2000 to the present to discover natural **player archetypes** using **unsupervised learning**. By applying **PCA** for dimensionality reduction and **KMeans clustering**, we segment players into distinct groups based on statistical performance — from All-Stars to role players — and identify **undervalued talent** using efficiency metrics.

---

## 🎯 Project Objective

**What types of NBA player archetypes exist based on statistical production?**  
Using clustering, can we reveal meaningful player types and find undervalued players who produce efficiently despite low scoring?

---

## 📁 Dataset

- **Source**: [Kaggle - Seasons_Stats.csv](https://www.kaggle.com/datasets/drgilermo/nba-players-stats)
- **Timeframe**: Seasons from 2000 to 2017
- **Filtering**:
  - Removed players with fewer than 500 minutes
  - Dropped irrelevant or sparse columns
  - Focused on total season stats

---

## 📊 Features Used

Clustering was performed on the following statistics:
- Points (PTS)
- Assists (AST)
- Total Rebounds (TRB)
- Steals (STL)
- Blocks (BLK)
- Turnovers (TOV)
- Field Goal % (FG%)
- 3-Point % (3P%)
- Free Throw % (FT%)
- Player Efficiency Rating (PER)
- True Shooting % (TS%)

---

## 🧠 Methods

- **Data Cleaning**: `pandas`
- **Scaling**: `StandardScaler` from `sklearn`
- **Dimensionality Reduction**: `PCA` (2 components)
- **Clustering**: `KMeans` with inertia analysis
- **Visualization**: `matplotlib`, `seaborn`

---

## 🔎 Cluster Archetypes

Using **6 clusters**, we identified the following player types:

| Cluster | Archetype | Example Players |
|---------|-----------|-----------------|
| 0 | ⭐ All-Stars / Playmakers | LeBron James (2014), Derrick Rose (2011), Deron Williams (2007) |
| 1 | 🛡️ Efficient Defensive Bigs | Brook Lopez (2014), JaVale McGee (2017), Ekpe Udoh (2013) |
| 2 | 🎯 Secondary Scorers / Wings | Harrison Barnes (2015), J.J. Barea (2013), Dion Waiters (2016) |
| 3 | ⚡ Undervalued Efficient Players | Manu Ginobili (2012), Isaiah Thomas (2015), Carl Landry (2016) |
| 4 | 🔁 Low-Impact Role Players | Anthony Tolliver (2016), Kareem Rush (2004), Chris Mihm (2003) |
| 5 | 🧱 Dominant Big Men | Dwight Howard (2008), Chris Bosh (2011), Josh Smith (2013) |

---

## 💡 Identifying Undervalued Talent

Filtered for players with:
- High **PER** (>15)
- High **TS%** (>0.55)
- Low **PTS** (<500)
- Belonging to non-star clusters (e.g., 1 or 3)

This surfaced **high-efficiency, low-usage players** like:
- Brook Lopez (2014)
- JaVale McGee (2017)
- Manu Ginobili (2012)
- Brandan Wright (2012)

These players deliver elite production with fewer opportunities — a potential goldmine for teams optimizing rosters.

---

## 📦 Files

- `NBA_Player_Analysis.ipynb`: Full notebook with analysis and visualizations
- `Seasons_Stats.csv`: Original dataset
- `README.md`: This file

---

## 🚀 Getting Started

To run locally:

```bash
git clone https://github.com/jaggerrobles-holmes/NBA_Player_Analysis.git
cd NBA_Player_Analysis
jupyter notebook
