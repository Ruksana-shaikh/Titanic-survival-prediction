# 🚢 Titanic-Survival-Prediction

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-green)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-orange)
![License](https://img.shields.io/badge/License-MIT-brightgreen)

---

## 🌟 Project Overview

The sinking of the **Titanic** is one of the most infamous shipwrecks in history.  
This project explores the **Titanic passenger dataset** to uncover patterns that influenced survival.  

Using **data cleaning, exploration, and visualization**, we aim to answer questions like:

- Who was more likely to survive? Men or women?  
- Did passenger class affect survival?  
- How did age or fare influence chances of survival?  

> 🎯 Objective: Extract meaningful insights and visualize survival patterns.

---

## 📊 Dataset Details

**Dataset:** `train.csv`  
**Rows:** 891 passengers  
**Columns:** 12  

| Column Name   | Description                                   |
|---------------|-----------------------------------------------|
| PassengerId   | Unique ID for each passenger                  |
| Survived      | Survival status (0 = No, 1 = Yes)            |
| Pclass        | Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)    |
| Name          | Passenger name                               |
| Sex           | Gender                                        |
| Age           | Age in years                                  |
| SibSp         | # of siblings/spouses aboard                  |
| Parch         | # of parents/children aboard                  |
| Ticket        | Ticket number                                 |
| Fare          | Passenger fare                               |
| Cabin         | Cabin number                                  |
| Embarked      | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |

> ⚠️ Missing values:  
> - `Age` (177) → imputed with median  
> - `Embarked` (2) → imputed with mode  
> - `Cabin` (687) → often ignored for EDA  

---

## 🛠 Tools & Libraries

- Python 3.x  
- pandas, numpy  
- seaborn, matplotlib  
- Jupyter Notebook  

---

## 🧩 Methodology / Steps

1. **Data Loading & Inspection:** Check shape, datatypes, missing values.  
2. **Data Cleaning:** Impute missing `Age` and `Embarked`; drop duplicates.  
3. **Exploratory Data Analysis (EDA):**  
   - Summary statistics (`describe()`)  
   - Value counts for `Sex`, `Pclass`  
   - Distribution plots for `Age` and `Fare`  
4. **Visualization of Relationships:**  
   - Scatter plots (`Age` vs `Fare` colored by `Survived`)  
   - Count plots (`Survival by Pclass and Sex`)  
   - Correlation heatmap  
5. **Insights Extraction:** Identify patterns and trends.  

---

## 💻 Sample Code Snippets

```python
# Distribution of Age
sns.histplot(train_data['Age'], bins=30, kde=True)
plt.title('Distribution of Age')
plt.show()

# Survival by Pclass and Sex
sns.countplot(x='Pclass', hue='Sex', data=train_data, palette='Set1', hue_order=['male', 'female'])
plt.title('Survival by Pclass and Sex')
plt.show()

# Correlation Heatmap
sns.heatmap(train_data.corr(), annot=True, cmap='coolwarm', fmt='.2f')
plt.title('Correlation Heatmap')
plt.show()
````

---

## 📈 Key Insights

* **Gender:** Females had a higher survival rate than males.
* **Pclass:** Passengers in 1st class survived more than 2nd and 3rd class.
* **Age:** Children and young adults had higher survival probability.
* **Fare:** Higher fare correlated with higher survival.
* **Correlation Heatmap:** `Pclass` and `Fare` show strong relationships with survival.

> 🖼️ **Visualization Placeholder:**
> ![Age Distribution](images/age_distribution.gif)
> ![Survival by Pclass and Sex](images/survival_pclass_sex.gif)

---

## 📂 Project Structure

```
Titanic_EDA/
│
├── data/                  # CSV dataset
├── notebooks/             # Jupyter notebooks for EDA
├── scripts/               # Python scripts
├── images/                # Charts and GIFs
├── README.md              # Project documentation
└── requirements.txt       # Dependencies
```

---

## ⚡ How to Run

1. Clone the repo

```bash
git clone https://github.com/your-username/Titanic_EDA.git
cd Titanic_EDA
```

2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn
```

3. Run Jupyter notebooks in `notebooks/` or scripts in `scripts/`.

---

## 🤝 Contributing

* Bug fixes 🐞
* Adding new visualizations 📊
* Documentation improvements ✍️

Fork → branch → pull request.

---

## 🏆 Fun Fact / Takeaways

* Data tells a story 🌏 — Explore survival patterns by age, sex, and class.
* This project is a **foundation for predictive modeling** (Logistic Regression, Random Forest).
* Great for **portfolio projects** to showcase **data analysis and visualization skills**.

---

## 📄 License

MIT License © 2025 | Your Name

---

## 📬 Contact

* GitHub: [your-username](https://github.com/your-username)
* Email: [your-email@example.com](mailto:your-email@example.com)

---

✨ **Sail through data like a Titanic survivor! 🚢**
