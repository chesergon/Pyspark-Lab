#  pyspark_lab

A hands-on PySpark learning lab using the **Breast Cancer Wisconsin Dataset** to explore big data processing, SQL querying, and data analysis with PySpark, Pandas, and NumPy.

---

## 📌 Overview

This repository contains two Jupyter notebooks designed to help data science students learn PySpark through practical, real-world medical data analysis. Each notebook builds progressively on core PySpark concepts, from basic DataFrame operations to feature engineering and statistical analysis.

---

## 🎯 Learning Objectives

By working through these notebooks, you will be able to:

- Set up and use a PySpark session in a Jupyter environment
- Load and explore datasets using PySpark DataFrames
- Use `pyspark.sql` to run SQL queries on DataFrames
- Perform aggregations, filtering, and feature engineering with PySpark
- Convert between PySpark and Pandas DataFrames
- Visualize data distributions using Matplotlib
- Apply NumPy operations alongside PySpark for numerical analysis
- Compute descriptive statistics including mean, min, max, and standard deviation

---

## 📂 Repository Structure

```
pyspark_lab/
│
├── CGLabC4M3.ipynb       # PySpark with Pandas
├── CGLabC4M4.ipynb # PySpark with NumPy and Pandas
├── breast_cancer.csv                 # Breast Cancer Wisconsin Dataset
│  
└── README.md
```

---

##  Notebooks

### Notebook 1 — PySpark with Pandas
This notebook introduces PySpark fundamentals using the Breast Cancer dataset, with a focus on integrating PySpark with Pandas for data manipulation and visualization.

**Topics covered:**
- Loading CSV data into a PySpark DataFrame
- Exploring data with `.describe()` and `.show()`
- Registering temp views with `createOrReplaceTempView()`
- Running SQL queries using `spark.sql()`
- Counting and comparing diagnosis classes (Benign vs Malignant)
- Visualizing class distribution with a bar plot using Matplotlib
- Computing aggregations: `AVG`, `MAX`, `MIN`, `STDDEV`
- Feature engineering: computing ratios, products, and rounded means via SQL
- Converting PySpark DataFrames to Pandas with `.toPandas()`

---

### Notebook 2 — PySpark with NumPy and Pandas
This notebook extends the analysis by incorporating NumPy alongside PySpark and Pandas for numerical operations and deeper statistical exploration.

**Topics covered:**
- Integrating NumPy with PySpark workflows
- Array operations and numerical transformations using NumPy
- Combining PySpark aggregations with NumPy computations
- Comparative analysis between PySpark and NumPy results

---

##  Dataset

**Breast Cancer Wisconsin (Diagnostic) Dataset**

The dataset contains features computed from digitized images of fine needle aspirates (FNA) of breast masses, used to predict whether a tumor is **Benign (B)** or **Malignant (M)**.

| Feature | Description |
|---|---|
| `diagnosis` | Target variable — B (Benign) or M (Malignant) |
| `radius_mean` | Mean of distances from center to perimeter |
| `texture_mean` | Standard deviation of gray-scale values |
| `perimeter_mean` | Mean perimeter of the tumor |
| `smoothness_mean` | Local variation in radius lengths |
| `compactness_mean` | Perimeter² / area - 1.0 |
| `symmetry_mean` | Symmetry of the tumor |
| `fractal_dimension_mean` | Coastline approximation of tumor boundary |

---

## ⚙️ Setup & Installation

### Prerequisites

Make sure you have the following installed:

- Python 3.8+
- Java 8 or 11 (required by PySpark)
- Jupyter Notebook or JupyterLab

### Install dependencies

```bash
pip install pyspark pandas numpy matplotlib
```

### Verify Java installation

```bash
java -version
```

### Clone the repository

```bash
git clone https://github.com/<your-username>/pyspark_lab.git
cd pyspark_lab
```

### Launch Jupyter

```bash
jupyter notebook
```

---

##  Usage

1. Clone the repository and install dependencies (see above)
2. Place the `breast_cancer.csv` dataset in the `data/` folder
3. Open `notebook_1_pyspark_pandas.ipynb` and run cells sequentially
4. Once comfortable, move on to `notebook_2_pyspark_numpy_pandas.ipynb`
5. Each notebook is self-contained with inline explanations for every step

---

## Key PySpark Concepts Used

| Concept | Example |
|---|---|
| Create Spark session | `SparkSession.builder.getOrCreate()` |
| Load CSV | `spark.read.csv(...)` |
| Register temp view | `df.createOrReplaceTempView('df_sql')` |
| SQL query | `spark.sql("SELECT ... FROM df_sql")` |
| Aggregation | `df.agg(max('column')).collect()[0][0]` |
| Convert to Pandas | `df.toPandas()` |
| Show tables | `spark.catalog.listTables()` |

---

##  License

This project is open source and available under the [MIT License](LICENSE).

---

##  Acknowledgements
@chesergon/repositories


- Dataset sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)
- Built as part of a PySpark learning lab for data science students
