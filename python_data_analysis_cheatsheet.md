
# 🧰 Frequently Used Python Functions and Methods for Data Analysis

This cheat sheet includes common Python functions, methods, and idioms you’ll likely use in your data analysis work, along with links to official documentation for further exploration.

---

## 📦 General Python

- [Built-in Functions](https://docs.python.org/3/library/functions.html)
- [Python Standard Library](https://docs.python.org/3/library/index.html)

```python
print(x)                # Display output
type(x)                 # Show the type of a variable
len(x)                  # Length of a list or string
range(5)                # Range from 0 to 4
sum([1, 2, 3])          # Sum of a list
sorted(list)            # Sort a list
```

---

## 🐼 `pandas` for DataFrames  
🔗 [pandas documentation](https://pandas.pydata.org/docs/)

```python
import pandas as pd

pd.read_csv("file.csv")     # Read CSV into DataFrame
df.to_csv("file.csv")       # Save DataFrame to CSV
df.head()                   # First 5 rows
df.tail()                   # Last 5 rows
df.info()                   # Column info
df.describe()               # Summary stats
df.columns                  # List column names
df.shape                    # Rows and columns

df['col']                   # Access column
df[['col1', 'col2']]        # Multiple columns
df.loc[0]                   # First row by label
df.iloc[0]                  # First row by position

df['col'].unique()          # Unique values
df['col'].value_counts()    # Count of each value
df.isna().sum()             # Missing values per column
df.dropna()                 # Drop rows with missing values
df.fillna(0)                # Replace NA with 0

df['col'] = df['col'].astype(str)           # Convert type
df['col'] = pd.to_numeric(df['col'])        # Ensure numeric
df['col'] = df['col'].str.strip()           # Remove spaces
df['col'] = df['col'].str.lower()           # Lowercase
```

---

## 🔢 `numpy` for Numerical Computation  
🔗 [NumPy documentation](https://numpy.org/doc/)

```python
import numpy as np

np.mean(array)             # Average
np.median(array)           # Median
np.std(array)              # Standard deviation
np.array([1, 2, 3])        # Create array
```

---

## 📈 `matplotlib` for Basic Plotting  
🔗 [Matplotlib documentation](https://matplotlib.org/stable/contents.html)

```python
import matplotlib.pyplot as plt

plt.plot([1, 2, 3], [4, 1, 5])
plt.title("Plot Title")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.show()
```

---

## 🌊 `seaborn` for Statistical Plots  
🔗 [Seaborn documentation](https://seaborn.pydata.org/)

```python
import seaborn as sns

sns.barplot(data=df, x="col1", y="col2")
sns.boxplot(data=df, x="group", y="value")
sns.histplot(df['col'], bins=10, kde=True)
sns.scatterplot(data=df, x="x", y="y", hue="group")
```

---

## 🧪 `scipy.stats` for Statistical Tests  
🔗 [SciPy stats documentation](https://docs.scipy.org/doc/scipy/reference/stats.html)

```python
from scipy import stats

stats.ttest_ind(group1, group2)        # Independent t-test
stats.chi2_contingency(table)          # Chi-squared test
```

---

## 📉 `statsmodels` for Regression and ANOVA  
🔗 [statsmodels documentation](https://www.statsmodels.org/stable/index.html)

```python
import statsmodels.formula.api as smf

model = smf.ols("Y ~ X1 + X2", data=df).fit()
print(model.summary())

import statsmodels.api as sm
sm.stats.anova_lm(model, typ=2)        # ANOVA table
```

---

*Keep this cheat sheet handy while working on your notebooks!* 🧪📊🦛
