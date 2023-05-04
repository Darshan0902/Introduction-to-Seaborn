# <h1>Introduction to Data Visualization with Seaborn</h1>

<h1>Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.</h1>

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
 
<br>Import Matplotlib and Seaborn using the standard naming conventions.
<br>Use Seaborn to create a count plot with region on the y-axis.
<br>Display the plot.

```
# Import Matplotlib and Seaborn
import seaborn as sns
import matplotlib.pyplot as plt


# Create count plot with region on the y-axis
sns.countplot(y=region)
# Show plot
plt.show()

```

# "Tidy" vs. "untidy" data

```
# Import pandas
import pandas as pd

# Create a DataFrame from csv file
df = pd.read_csv(csv_filepath)

# Print the head of df
print(df.head())

```

<h2> Making a count plot with a DataFrame </h2>

```
# Import Matplotlib, pandas, and Seaborn
import matplotlib.pyplot as plt 
import pandas as pd 
import seaborn as sns 

# Create a DataFrame from csv file
df = pd.read_csv(csv_filepath)

# Create a count plot with "Spiders" on the x-axis
x_column = "Spiders"
sns.countplot(x=x_column,data=df)

# Display the plot
plt.show()

```


# Hue and scatter plots

```
# Import Matplotlib and Seaborn
import matplotlib.pyplot as plt
import seaborn as sns

# Change the legend order in the scatter plot
sns.scatterplot(x="absences", y="G3", 
                data=student_data, 
                hue="location",hue_order=["Rural","Urban"])

# Show plot
plt.show()
```

# Hue and count plots

<br> Fill in the palette_colors dictionary to map the "Rural" location value to the color "green" and the "Urban" location value to the color "blue". <br> 

```


# Import Matplotlib and Seaborn
import matplotlib.pyplot as plt
import seaborn as sns

# Create a dictionary mapping subgroup values to colors
palette_colors = {"Rural": "green", "Urban": "blue"}

# Create a count plot of school with location subgroups

sns.countplot(x="school",data=student_data,hue="location",palette=palette_colors)


# Display plot
plt.show()


```
