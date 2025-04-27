# IMT542-i3

## Overview
This application analyzes and visualizes the top 20 most popular pet names from the Seattle Pet Licenses dataset in a bar chart. 

Details:
- Loads a CSV dataset of pet licenses issued in Seattle.
- Counts the frequency of each pet name.
- Identifies and displays the top 20 most common names.
- Visualizes the result in a bar chart for easy interpretation.

## Instruction
The repo contains the Seattle Pet Licenses CSV dataset and a Python Notebook file that can be opened in Google Colab. Download and import the dataset into Colab, copy and paste the code in Code Example, or click i3_Pet Licenses.ipynb. The script reads the CSV dataset, processes the dataset using `pandas`, and displays the results in a bar graph using `matplotlib` and `seaborn`.

## Dataset
Ensure the dataset file `new_Seattle_Pet_Licenses_20250203_raw.csv` is located in your project directory folder. If you're using a platform like Google Colab or Jupyter Notebook, make sure the path to the file is correctly specified (`/content/new_Seattle_Pet_Licenses_20250203_raw.csv`).

## Why Use This
This script is a quick and insightful way to:
- Practice data visualization and basic analysis using real-world datasets.
- Discover fun trends in local pet naming culture.
- Serve as a starting point for more advanced analyses such as breed/popularity trends or geographic distributions.

## Code Example
```
# Gives the top 20 most popular pet names and visualizes in a bar graph for /content/Seattle_Pet_Licenses_20250203_raw.csv

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataframe.
df = pd.read_csv('/content/new_Seattle_Pet_Licenses_20250203_raw.csv')

# Count occurrences of each name.
name_counts = df['Animal Name'].value_counts()

# Get the top 20 most popular names.
top_20_names = name_counts.head(20)

# Create the bar graph.
plt.figure(figsize=(12, 6))
sns.barplot(x=top_20_names.index, y=top_20_names.values)
plt.xlabel("Pet Names")
plt.ylabel("Number of Pets")
plt.title("Top 20 Most Popular Pet Names in Seattle")
plt.xticks(rotation=45, ha='right')  # Rotate x-axis labels for better readability
plt.tight_layout()
plt.show()
```
