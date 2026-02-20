# Task-5
Data analysis on CSV files
import pandas as pd
from io import StringIO
# Create CSV data inside Python
csv_data = """Name,Age,Marks
Arun,20,85
Ravi,22,90
Sita,19,88
Kumar,21,76
"""

# Read the CSV data
data = pd.read_csv(StringIO(csv_data))

# Show data
print("Full Data:")
print(data)

# Find average marks
print("\nAverage Marks:", data["Marks"].mean())

# Find highest marks
print("Highest Marks:", data["Marks"].max())

# Students with marks above 80
print("\nStudents with Marks above 80:")
print(data[data["Marks"] > 80])
