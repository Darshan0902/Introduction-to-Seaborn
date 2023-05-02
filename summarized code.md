# Introduction to Data Visualization with Seaborn

_Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.

_

```

# Importing the course packages
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Importing the course datasets
country_data = pd.read_csv('datasets/countries-of-the-world.csv', decimal=",")
mpg = pd.read_csv('datasets/mpg.csv')
student_data = pd.read_csv('datasets/student-alcohol-consumption.csv', index_col=0)
survey = pd.read_csv('datasets/young-people-survey-responses.csv', index_col=0)


```

# Explore the datasets:

Using the datasets imported in the previous or the cell above explore the datasets and try to retreive or gain more information using the data. 

1. From (country_data) create a scatter plot to look at the relationship between GDP and Literacy. Use color to segment the data points by region.
2. Use mpg to create a line plot with model_year on the x-axis and weight on the y-axis. Create differentiating lines for each country of origin (origin).
3. Create a box plot from student_data to explore the relationship between the number of failures (failures) and the average final grade (G3).
4. Create a bar plot from survey to compare how Loneliness differs across values for Internet usage. Format it to have two subplots for gender.
5. Do try to include labels and titles to make the whole data look more lively and presentable as you present those visualization and also make sure to add titles and labels to your plots and adjust their format for readability and better Analytics purpose.


## Making a scatter plot with lists
 
