# Measuring the Pulse of Prosperity: An Index of Economic Freedom
# Sample Python Code for Economic Freedom Analysis

import pandas as pd
import matplotlib.pyplot as plt

# Sample dataset of economic freedom indicators
data = {
    "Country": ["USA", "India", "Germany", "Japan", "Australia"],
    "Property_Rights": [80, 55, 78, 75, 82],
    "Government_Integrity": [75, 50, 72, 70, 80],
    "Tax_Burden": [65, 60, 68, 67, 70],
    "Business_Freedom": [85, 70, 80, 78, 84],
    "Trade_Freedom": [82, 65, 79, 77, 83]
}

# Create DataFrame
df = pd.DataFrame(data)

# Calculate Economic Freedom Index (average of indicators)
df["Economic_Freedom_Index"] = df.iloc[:, 1:].mean(axis=1)

# Display the dataset
print("Economic Freedom Index Data")
print(df)

# Visualization
plt.figure(figsize=(8,5))
plt.bar(df["Country"], df["Economic_Freedom_Index"])
plt.title("Economic Freedom Index Comparison")
plt.xlabel("Country")
plt.ylabel("Economic Freedom Score")
plt.show()
