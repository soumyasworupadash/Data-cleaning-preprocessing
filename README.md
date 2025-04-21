# Data Cleaning and Preprocessing of Netflix Movies and TV Shows

This project focuses on cleaning and preprocessing a dataset containing information about Netflix Movies and TV Shows. The dataset includes features like title, type, director, cast, country, release year, rating, duration, and more.

---

## 🧹 Data Preprocessing Steps

### ✅ 1. Handling Missing Values
- Used `.isnull()` to identify missing values.
- Columns with all values missing were removed using:
  ```python
  data = data.loc[:, ~data.isnull().all()]
  ```

### ✅ 2. Removing Unnamed/Empty Columns
- Dropped unnamed or empty columns using `.isnull().all()` to clean the dataset.

### ✅ 3. Standardizing the `country` Column
- Converted all country names to lowercase.
- Removed leading/trailing whitespace.
- Applied formatting to ensure consistency in naming.

### ✅ 4. Date Format Conversion
- Reformatted the `date_added` column to `dd-mm-yyyy` using:
  ```python
  data['date_added'] = pd.to_datetime(data['date_added'], errors='coerce')
  ```

### ✅ 5. Renaming Column Headers
- Converted all column headers to lowercase.
- Replaced spaces with underscores for consistency.

### ✅ 6. Data Type Fixes
- `date_added`: Converted to `datetime64`.
- `rating`: Converted to `category` type to optimize memory usage.

---

## 📁 Output

The cleaned dataset is saved as:
- `cleaned_dataset.csv` or `cleaned_dataset.xlsx`

You can find the cleaned version inside this repository.

---

## 🛠 Tools Used

- **Python** 🐍  
- **Pandas** 🐼  
- **Jupyter Notebook** / **VS Code**  


Feel free to contribute or fork this project for your own data cleaning tasks!
