# 📊 Beginner’s Guide to Python Visualization: Matplotlib vs Pandas

## 1. 🧭 Library Overview

### Matplotlib
Matplotlib is a powerful and flexible plotting library in Python. It allows users to create static, animated, and interactive visualizations with fine-grained control over every element.

- **Unique Features**:
  - Highly customizable
  - Supports multiple output formats (PNG, PDF, SVG)
  - Works well with NumPy and Pandas

- **Use Cases**:
  - Scientific plotting
  - Publication-quality figures
  - Custom dashboards

### Pandas
Pandas is primarily a data manipulation library, but it integrates with Matplotlib to offer quick and intuitive plotting from DataFrames and Series.

- **Unique Features**:
  - Built-in `.plot()` method
  - Simplifies plotting directly from tabular data
  - Ideal for quick exploratory analysis

- **Use Cases**:
  - Exploratory data analysis
  - Time series visualization
  - Quick summaries of tabular data

---

### 2. 📈 Graph Types with Examples

### * Line Plot
**Use Case**: Showing trends over time

### Matplotlib
import matplotlib.pyplot as plt
x = [1, 2, 3]
y = [2, 4, 1]
plt.plot(x, y)
plt.title("Line Plot")
plt.show()

**Pandas**
import pandas as pd
df = pd.DataFrame({'x': [1, 2, 3], 'y': [2, 4, 1]})
df.plot(x='x', y='y', title="Line Plot")
![output](Screenshot 2025-08-17 132455-1.png)

### * Bar Chart
**Use Case**:Comparing Categories

**Matplotlib**
import matplotlib.pyplot as plt
category=['a','g','d','e']
sales=[23,43,56,46]
plt.bar(category,sales,color='red')
plt.title("Bar Chart")
plt.show()

**Pandas**
import pandas as pd
data={
    'category':['a','g','d','e'],
     'sales':[23, 43, 56, 46]
    }
df=pd.DataFrame(data)
df.plot.bar(x='category',y='sales')
![Output](screenshots/Screenshot 2025-08-17 132533.png)

### * Histogram
**Use Case**:Distribution of Numeric Data

**matplotlib**
import matplotlib.pyplot as plt
x=[23,43,54,13,47]
plt.hist(x,bins=5)
plt.title('Histogram')
plt.show()

**Pandas**
import pandas as pd
data={
    'sales':[23,43,54,65,35]
}
df=pd.DataFrame(data)
df['sales'].plot(kind='hist',bins=5,title='Histogram')
![output](screenshots/Screenshot 2025-08-17 132633.png)

### * PieChart
***Use Case**:Proportional Data

**matplotlib**
import matplotlib.pyplot as plt
city=['a','b','c','d']
sales=[30,43,65,32]
plt.pie(sales,labels=city,autopct='%1.1f%%')
plt.title('pie chart')
plt.show()

**Pandas**
import pandas as pd
data={
    'city':['a','b','c','d'],
    'sales':[30,43,65,32]
    }
df=pd.DataFrame(data)
df.set_index('city').plot.pie(y='sales',autopct='%1.1f%%',title='PieChart')
![output](screenshots/Screenshot 2025-08-17 132744.png)

### * Scatter Plot
**Use Case**:Relate Two Variables

**matplotlib**
import matplotlib.pyplot as plt
temperature=[32,43,21,33]
humidity=[54,32,45,33]
plt.scatter(temperature,humidity)
plt.title('Scatter Plot')
plt.show()

**Pandas**
import pandas as pd
df=pd.DataFrame({'temperature':[32,43,21,33],'humidity':[54,32,45,33]})
df.plot(kind='scatter',x='temperature',y='humidity',title='Scatter Plot')
![output](screenshots/Screenshot 2025-08-17 132901.png)

### COMPARISION TABLE ###

**Feature**	     |    **Matplotlib**	      |     **Pandas**
Ease of Use 	 |  Moderate (manual setup)   |  High (one-liner plots)
Customization	 |  Extensive	              |  Limited (via Matplotlib)
Interactivity	 |  Low (static plots)	      |  Low
Performance	     |  Good for large data	      | Depends on DataFrame size
Learning Curve	 |  Steeper	                  | Beginner-friendly

### Resources ###

- [Matplotlib Quick Start Guide](https://matplotlib.org/stable/users/explain/quick_start.html#quick-start)
- [Pandas User Guide](https://pandas.pydata.org/docs/user_guide/index.html)
- [Pandas Plotting Tutorial](https://studyopedia.com/pandas/pandas-plotting/)

---

## 🙋‍♂️ About Me
**Karunakar Tappa** — Aspiring Data Scientist  
Currently exploring Python, DSA, and visualization libraries to build strong foundations in data science.

---

## 📣 Connect With Me
- 📧 tkarunakar999@gmail.com




