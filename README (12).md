
# 📊 Data Visualization Project – README.md

## 📌 Project Overview
This project is a **Python-based Data Analysis and Visualization tool** built using:
- NumPy
- Pandas
- Matplotlib
- Seaborn

The main goal of this project is to load a CSV dataset, perform basic data analysis, and generate visualizations that can be **saved as image files**.

This README explains **step-by-step execution**, **inputs**, **outputs**, and **working of the `save_visualization()` function** in detail.

---

## 📂 Project Structure
```
project/
│
├── visualizer.py
├── data.csv
├── README.md
└── output_plot.png
```

---

## 🔧 Required Libraries
Install required libraries using:

```bash
pip install numpy pandas matplotlib seaborn
```

---

## 🧠 save_visualization() Function

### 🔹 Function Code
```python
def save_visualization(self):
    A = input("Enter x-axis column: ")
    B = input("Enter y-axis column: ")
    C = input("Enter title: ")
    filename = input("Enter filename (e.g., plot.png): ")

    plt.plot(self.data[A], self.data[B])
    plt.title(C)
    plt.savefig(filename, dpi=4000, bbox_inches='tight')
    print(f"Plot saved as {filename}")
```

---

## ▶️ Step-by-Step Execution

### Step 1: Dataset Load
Before calling this function, the dataset **must be loaded** into `self.data`.

Example CSV:
```csv
Name,Age,Salary,Department
Amit,25,30000,IT
Ravi,30,40000,HR
Neha,28,35000,IT
Pooja,35,50000,Finance
```

---

### Step 2: Function Call
```python
X.save_visualization()
```

---

### Step 3: User Inputs

#### Input 1 – X-axis Column
```
Enter x-axis column: Age
```

#### Input 2 – Y-axis Column
```
Enter y-axis column: Salary
```

#### Input 3 – Title
```
Enter title: Age vs Salary
```

#### Input 4 – Filename
```
Enter filename (e.g., plot.png): age_salary.png
```

---

## 📈 Internal Execution Flow

1. Python reads user input
2. Extracts columns from DataFrame
3. Generates line plot using Matplotlib
4. Applies title
5. Saves plot as image file
6. Prints confirmation message

---

## ✅ Output

### Terminal Output
```
Plot saved as age_salary.png
```

### File Output
An image file named:
```
age_salary.png
```
is created in the project directory.

---

## ⚠️ Common Errors & Solutions

### ❌ KeyError
Occurs when column name is incorrect.

✔️ Solution:
```python
print(self.data.columns)
```

---

### ❌ Dataset Not Loaded
```
AttributeError: 'NoneType' object has no attribute
```

✔️ Solution:
Load dataset before visualization.

---

## 🎓 Viva / Exam Explanation
> This function takes column names from the user, generates a line plot using matplotlib, and saves the visualization as an image file with high resolution.

---

## 🚀 Conclusion
This function helps in:
- Creating reusable visualizations
- Saving plots for reports and presentations
- Understanding real-world data visualization workflow

---

## ✨ Author
**Student Data Science Project**  
Python | Pandas | Matplotlib
