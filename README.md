## ⚽ International Football Analysis  
*A Data-Driven Exploration of 150 Years of Global Football*  

This project visualizes over **48,000 international football matches (1872–2023)** to uncover long-term patterns in **goal scoring, competitiveness, and tournament evolution**.  
It combines global trends with detailed **country-level dashboards**, offering a complete view of how football evolved from regional pastime to the world’s most popular sport.

---

### 📊 Key Insights  

- **Home advantage remains dominant:** Home teams win about **49%** of all international matches, confirming a consistent global trend across 150 years.  
- **Low-scoring nature of football:** Most matches end with **2–3 total goals**, reflecting football’s inherently tactical and defensive balance.  
- **Tactical evolution:** Average goals per match declined from **5+ in the late 19th century** to **under 3 today**, illustrating the rise of structured defensive systems.  
- **Tournament diversity:** *Copa América* averages the highest scoring rate (**3.14 goals/match**), while the *UEFA Euro* remains the most defensive (**2.44 goals/match**).  
- **Competitive balance:** The *UEFA Euro* shows the **lowest average goal difference (1.22)** — matches are tighter and more unpredictable; *Copa América*’s 1.82 reflects more disparity.  
- **Friendly dominance:** With over **18,000 friendlies**, nearly half of all matches occurred outside tournaments — highlighting football’s social and diplomatic role.  
- **Historical disruptions:** Sharp declines during **WWI and WWII** reveal how global conflict halted football competition.  
- **Post-1950 expansion:** After WWII, international football exploded in popularity — driven by television, global tournaments, and new federations.  
- **Regional imbalance:** **Europe** has hosted over 15,000 matches, but **Asia** and **Africa** are rapidly catching up with modern growth.  
- **Goal correlations:** Total goals correlate strongly with home (0.75) and away (0.55) goals; the slight negative correlation (−0.14) between home and away shows one’s dominance suppresses the other.  
- **Evolving parity:** The gap between stronger and weaker nations has narrowed — underdogs now lose by smaller margins.  
- **Cultural contrasts:** South American football emphasizes flair and offense; European football values tactical precision and structure.  

---

### 🌍 Country-Level Dashboards  

In addition to global analyses, the project features **10 national dashboards**, each visualizing:  
- Win, loss, and draw rates  
- Total and average goals scored  
- Most frequent opponents and rivalries  
- Historical performance trends  

Countries analyzed include **Brazil, Germany, Argentina, Italy, France, Netherlands, England, Spain, Portugal, and Uruguay.**

Each dashboard was generated using a reusable Python function for consistent data filtering and visualization:

```python
def get_country_data(df, country):
    """Filter all home & away matches for a given country."""
    df_country = df[
        (df['home_team'] == country) | (df['away_team'] == country)
    ].copy()
    df_country['is_home'] = df_country['home_team'] == country
    return df_country

--- 

### 🧠 Technologies Used

Python — core programming and analysis

NumPy — numerical operations

Pandas — data manipulation and cleaning

Matplotlib — dark-themed custom visualizations

Seaborn — complementary statistical styling

---

### 📂 Repository Structure

international-football-analysis/
│
├── results.csv
├── international.ipynb
├── presentation.pdf
├── README.md
└── requirements.txt

---

### 👨‍💻 Author

Sezer Bayraktar
Software Engineering & Business Student / Aspiring Data Scientist
📍 Istanbul, Türkiye

---

### 🏁 Notes

This project was created for portfolio and educational purposes — demonstrating skills in data analysis, visualization, and storytelling through global and national football analytics.
