
# 📊 NumPy Analyzer

## 📌 Project Overview
The **NumPy Analyzer** is a Python-based, menu-driven console application that combines **NumPy functionalities** with **Object-Oriented Programming (OOP)** principles. It lets the user create arrays, perform mathematical operations, combine or split arrays, search, sort and filter data, and compute aggregate and statistical values, all from a simple text menu.

This project is built to demonstrate **NumPy array handling**, **OOP concepts** (class, constructor, encapsulation, `@classmethod`, `@staticmethod`) and a **menu-driven user interface** in Python.

---

## 🎯 Objectives
- Build a toolkit for common data operations using NumPy arrays
- Encapsulate all functionality inside a single `DataAnalytics` class
- Apply OOP principles: constructors, private methods, class methods and static methods
- Provide a clear, menu-driven console interface with a proper exit option

---

## 🛠️ Features
- 🔢 **Array Creation:** create 1D, 2D or 3D arrays from user input
- 🎯 **Indexing and Slicing:** access specific elements, rows, columns or slices
- ➕ **Mathematical Operations:** element-wise addition, subtraction, multiplication and division
- ✖️ **Matrix Operations:** dot product and matrix multiplication for 2D arrays
- 🔗 **Combine and Split:** concatenate multiple arrays or split an array into smaller arrays
- 🔍 **Search:** find a specific value in an array
- ↕️ **Sort:** sort in ascending or descending order
- 🧪 **Filter:** keep only the values that meet a user-defined condition
- 📈 **Aggregates:** sum, mean, median, standard deviation and variance
- 📉 **Statistics:** minimum, maximum, percentiles and correlation coefficient between arrays
- 🚪 **Exit** option from the main menu

---

## 🧠 Concepts Used

### ✅ NumPy
- Array creation (`np.array`, `reshape`)
- Indexing and slicing (1D, 2D and 3D)
- Combining and splitting (`np.concatenate`, `np.vstack`, `np.split`)
- Element-wise operations, `np.dot`, `np.matmul`
- Searching, sorting and filtering (`np.where`, `np.sort`, boolean masking)
- Aggregates and statistics (`np.sum`, `np.mean`, `np.median`, `np.std`, `np.var`, `np.min`, `np.max`, `np.percentile`, `np.corrcoef`)

### ✅ Object-Oriented Programming
- **Class and Object:** one `DataAnalytics` class holds all the functionality
- **Constructor (`__init__`):** initializes the array when an object is created
- **Encapsulation:** the array is stored as a private attribute, and internal calculations are written as private methods (names start with `__`)
- **`@classmethod`:** alternative ways to create an object, for example from a list or from user input
- **`@staticmethod`:** utility helpers that do not need object data, for example input validation

### ✅ Python Fundamentals
- `input()` and `print()`, type casting
- Loops and conditions for the menu
- Functions and exception handling (`try` / `except`) for invalid input

---

## 🧾 Program Structure

```
NumPy_Analyzer/
│
├── numpy_analyzer.py   # Main Python program
└── README.md           # Project documentation
```

---

## ▶️ How to Run the Program
1. Install **Python 3.x** on your system
2. Install NumPy:
   ```
   pip install numpy
   ```
3. Save the program file as `numpy_analyzer.py`
4. Open terminal / command prompt
5. Navigate to the project folder
6. Run the command:

```
python numpy_analyzer.py
```

---

## 🖥️ Sample Console Interaction

**Main menu**
```
Welcome to the NumPy Analyzer!
==========================================
Choose an option:
1. Create a Numpy Array
2. Perform Mathematical Operations
3. Combine or Split Arrays
4. Search, Sort, or Filter Arrays
5. Compute Aggregates and Statistics
6. Exit
Enter your choice: 1
```

**Array creation**
```
Select the type of array to create:
1. 1D Array
2. 2D Array
3. 3D Array
Enter your choice: 2

Enter the number of rows: 2
Enter the number of columns: 3
Enter 6 elements for the array separated by space: 10 20 30 40 50 60

Array created successfully:
[[10 20 30]
 [40 50 60]]
```

**Slicing**
```
Choose an operation:
1. Indexing
2. Slicing
3. Go Back
Enter your choice: 2

Enter the row range (start:end): 0:2
Enter the column range (start:end): 1:3

Sliced Array:
[[20 30]
 [50 60]]
```

**Mathematical operation (addition)**
```
Choose a mathematical operation:
1. Addition
2. Subtraction
3. Multiplication
4. Division
Enter your choice: 1

Enter the same-size array elements (6 elements separated by space): 5 5 5 5 5 5

Original Array:
[[10 20 30]
 [40 50 60]]

Second Array:
[[5 5 5]
 [5 5 5]]

Result of Addition:
[[15 25 35]
 [45 55 65]]
```

**Combine arrays (vertical stack)**
```
Choose an option:
1. Combine Arrays
2. Split Array
Enter your choice: 1

Enter the elements of another array to combine (6 elements separated by space): 1 2 3 4 5 6

Combined Array (Vertical Stack):
[[10 20 30]
 [40 50 60]
 [ 1  2  3]
 [ 4  5  6]]
```

**Sort**
```
Choose an option:
1. Search a value
2. Sort the array
3. Filter values
Enter your choice: 2

Sorted Array:
[[10 20 30]
 [40 50 60]]
(Sorting applied row-wise.)
```

**Aggregate (median)**
```
Choose an aggregate/statistical operation:
1. Sum
2. Mean
3. Median
4. Standard Deviation
5. Variance
Enter your choice: 3

Median of Array: 35.0
```

**Exit**
```
Enter your choice: 6

Thank you for using the NumPy Analyzer! Goodbye!
```

---

## 🔐 Program Flow
1. **Welcome and Menu:** display a welcome message and the main menu with six options
2. **Create Array:** the user picks 1D, 2D or 3D, enters the size and the elements, and the array is stored in a `DataAnalytics` object
3. **Choose an Operation:** the program calls the matching method of the class (math, combine/split, search/sort/filter, aggregates/statistics)
4. **Display Results:** the original array, any second array and the result are printed in a clear format
5. **Repeat or Exit:** the menu is shown again until the user chooses **6. Exit**, which ends with a thank-you message

---

## 📝 Assumptions
- NumPy must be installed before running the program (`pip install numpy`)
- The user must create an array (option 1) before using the other options
- Elements are entered **separated by spaces** and are treated as numbers
- For element-wise operations, the second array must have the **same size** as the original, and it is reshaped to the original's shape
- Division by zero is handled with a warning message instead of crashing
- Dot product and matrix multiplication are available for **2D arrays**, and the shapes must be compatible
- Combining arrays uses a **vertical stack** by default, so the arrays need the same number of columns
- Sorting on a 2D array is applied **row-wise**
- Correlation needs two arrays with the same number of elements
- Invalid menu choices or inputs show an error message and the menu is shown again
- Data is stored only in memory and is lost when the program closes

---

## 🚀 Future Enhancements
- Saving and loading arrays using **CSV / JSON** files
- Stricter input validation for type and range checking
- A **GUI version** using Tkinter or PyQt
- Charts and graphs using Matplotlib
- Support for working with multiple arrays at the same time

---

## 👨‍💻 Author
Python Developer | Apeksha

---

## 📄 License
This project is created for **educational purposes** and is free to use and modify.

---

✨ *Happy Coding!* ✨
