# WQI-Polynomial-Regression

A college Data Science project focused on calculating **Water Quality Index (WQI)** and modelling it using **Linear Regression and Polynomial Regression**.

The project includes data cleaning, WQI calculation, feature engineering, model training, evaluation, and visualization. This work was also presented as a college poster.

---

## 📌 Project Overview

Water quality depends on different parameters such as **Dissolved Oxygen (DO), pH, Electrical Conductivity (EC), and Nitrate**. In this project, I use these parameters to calculate the **Water Quality Index (WQI)** and then apply Linear Regression and Polynomial Regression to model the calculated WQI.

The main goal is to use **Data Science and Machine Learning** to understand the relationship between water-quality parameters and the calculated WQI.

---

## 👥 Team

- **Talha Shaikh** — Data cleaning, feature engineering, WQI calculation, Linear and Polynomial Regression, model evaluation, and visualization.
- **Nafil Ajameri** — Data collection, supporting research from published papers, and poster design.

**Students, School of Emerging Science and Technology, Gujarat University**

---

## 🎯 Project Objectives

The main objectives of this project are:

1. To understand and calculate the Water Quality Index using selected water-quality parameters.
2. To clean and prepare water-quality data for analysis.
3. To study the relationship between water-quality parameters and the calculated WQI.
4. To apply Linear Regression as a baseline model.
5. To apply Polynomial Regression to model non-linear relationships.
6. To evaluate the models using R².
7. To visualize the data and model results.

---

## 💧 What is WQI?

The **Water Quality Index (WQI)** is a mathematical method used to represent the overall quality of water using a single numerical value.

Water quality depends on many physical and chemical parameters. Looking at each parameter separately can make it difficult to understand the overall condition of the water. WQI combines these parameters into one value, making it easier to understand and compare water quality.

In this project, I calculate WQI using the **Weighted Arithmetic Water Quality Index (WAWQI) method**. The calculated WQI is then used for regression modelling.

---

## 📁 Dataset Information

The dataset used in this project is taken from **government water-quality data**. For this project, I used a small portion of the available data that matched the required parameters for WQI calculation and regression modelling.

The dataset contains the following columns:

| Column | Description |
|---|---|
| **Station Code** | Identification code of the monitoring station |
| **Monitoring Location** | Location where the water sample was monitored |
| **State** | State of the monitoring location |
| **Min DO / Max DO** | Minimum and maximum Dissolved Oxygen values |
| **Min pH / Max pH** | Minimum and maximum pH values |
| **Min EC / Max EC** | Minimum and maximum Electrical Conductivity values |
| **Min N / Max N** | Minimum and maximum Nitrate values |

These values are used to prepare the data for **WQI calculation and regression modelling**.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas** — for data cleaning and data manipulation
- **NumPy** — for numerical calculations
- **Matplotlib** — for visualization
- **Seaborn** — for the correlation heatmap
- **Scikit-learn** — for machine learning and preprocessing

---

## 📂 Project Structure

```text
WQI-Polynomial-Regression/
│
├── README.md
├── requirements.txt
│
├── data/
│   └── water quality dataset
│
├── notebooks/
│   └── WQI and regression analysis
│
├── poster/
│   └── college project poster
│
└── ...
```

The exact file and folder names may be different depending on the current version of the project.

---

## 🔄 Project Workflow

The overall workflow of my project is:

**Water Quality Dataset**  
↓  
**Data Cleaning**  
↓  
**Parameter Selection**  
↓  
**WQI Calculation**  
↓  
**Feature Engineering**  
↓  
**Train / Test / Validation Split**  
↓  
**Feature Scaling (StandardScaler)**  
↓  
**Linear Regression**  
↓  
**Polynomial Feature Transformation**  
↓  
**Polynomial Regression**  
↓  
**Model Evaluation**  
↓  
**Visualization**

---

## 🧪 Parameters Used

### pH (Potential of Hydrogen)

pH tells us whether water is acidic, neutral, or alkaline. It is measured on a scale from 0 to 14, where 7 is considered neutral.

I used pH as one of the parameters because changes in pH can affect aquatic life and the chemical properties of water.

For my project, the **ideal value is 7.0** and the **standard value is 8.5**.

### DO (Dissolved Oxygen)

Dissolved Oxygen (DO) represents the amount of oxygen present in water. It is important for fish, microorganisms, and other aquatic organisms.

Low DO can be related to pollution and the decomposition of organic matter in water. DO can also change depending on factors such as temperature and water movement.

For my project, the **ideal value is 14.6 mg/L** and the **standard value is 6 mg/L**.

### EC (Electrical Conductivity)

Electrical Conductivity (EC) shows how easily water can conduct electricity. It mainly depends on the amount of dissolved ions and salts present in the water.

I used EC because it can help indicate changes in the chemical composition of water. Higher EC can indicate a higher amount of dissolved substances in water.

For my project, the **ideal value is 0 µS/cm** and the **standard value is 1000 µS/cm**.

### Nitrate (NO₃⁻)

Nitrate is a form of nitrogen that can naturally occur in water. It can also enter water through fertilizers, agricultural runoff, wastewater, manure, and decomposition of waste.

A high amount of nitrate can indicate nutrient pollution and can contribute to excessive plant and algae growth.

For my project, the **ideal value is 0 mg/L** and the **standard value is 45 mg/L**.

---

## 📊 WQI Parameters and Values

| Parameter | Unit | Ideal Value | Standard Value |
|---|---|---:|---:|
| **pH** | – | 7.0 | 8.5 |
| **Dissolved Oxygen (DO)** | mg/L | 14.6 | 6 |
| **Electrical Conductivity (EC)** | µS/cm | 0 | 1000 |
| **Nitrate (NO₃⁻)** | mg/L | 0 | 45 |

---

## 🧮 WQI Calculation

For calculating WQI, I used the **Weighted Arithmetic Water Quality Index (WAWQI)** method.

The method uses the observed value, ideal value, and standard value of each parameter to calculate the quality rating and weight.

### 1. Quality Rating (Qi)

The quality rating is calculated using:

**Qi = |Vi − V0| / |Si − V0| × 100**

Where:

- **Vi** = Observed value
- **V0** = Ideal value
- **Si** = Standard value

### 2. Unit Weight (Wi)

The unit weight is calculated using:

**Wi = k / Si**

Where:

**k = 1 / Σ(1 / Si)**

### 3. Final WQI

The final WQI is calculated using:

**WQI = Σ(Qi × Wi) / ΣWi**

After calculating these values for all four parameters, I obtained the final WQI value for each data record.

---

## 📋 Water Quality Classification

| WQI Range | Quality of Water |
|---|---|
| **0–25** | Excellent |
| **26–50** | Good |
| **51–75** | Poor |
| **76–100** | Very Poor |
| **>100** | Unsuitable for Drinking |

---

## 🤖 Machine Learning Models

### Linear Regression

I first used **Linear Regression** as a baseline model. It helped me understand how well a simple linear relationship could represent the relationship between the selected water-quality parameters and WQI.

### Polynomial Regression

After Linear Regression, I used **Polynomial Regression** because the relationship between water-quality parameters and WQI may not always be completely linear.

For example, a degree-2 polynomial model can include terms such as:

**DO², pH², EC², Nitrate², DO×pH, DO×EC, ...**

A degree-3 model includes additional higher-order terms.

---

## 📈 Model Evaluation

I used **R² (R-squared)** as the main evaluation metric.

R² tells me how much of the variation in WQI is explained by the model on the evaluated data. A value closer to 1 means that the model explains more of the variation in that dataset.

### Results

| Model | Train R² | Test R² | Validation R² |
|---|---:|---:|---:|
| **Linear Regression** | 0.4559 | 0.5175 | 0.3546 |
| **Polynomial Degree 2** | 0.9614 | 0.9538 | 0.9361 |
| **Polynomial Degree 3** | 0.9879 | 0.9067 | 0.9584 |

For my project, I selected **Polynomial Regression Degree 2** as the final model. It gives a strong test R² and has balanced performance across the different data splits.

Degree 3 gives a higher training R², but its test R² is lower than Degree 2.

These results are based on the dataset and methodology used in this project. The same performance may not be obtained on a different dataset.

---

## 🔍 Correlation Analysis

Correlation was used to understand the relationship between the selected parameters and the calculated WQI.

| Parameter | Correlation with WQI |
|---|---:|
| **Dissolved Oxygen (DO)** | -0.6320 |
| **pH** | -0.1906 |
| **Electrical Conductivity (EC)** | 0.1701 |
| **Nitrate** | 0.2132 |

These values represent the linear correlation between each parameter and the calculated WQI in the dataset.

---

## 📊 Visualizations

I created different visualizations to understand the data and model results, such as:

- Feature distributions
- Correlation heatmap
- Partial residual / model relationship plots
- Actual vs. predicted values
- Residual plots

These plots helped me understand the relationship between the water-quality parameters and WQI and also helped me check the model results.

---

## 📚 What I Learned from This Project

Working on this project helped me learn and practice:

- Data cleaning and preprocessing
- Working with water-quality data
- WQI calculation
- Feature engineering
- Data standardization
- Linear Regression
- Polynomial Regression
- Model evaluation using R²
- Train, test, and validation splitting
- Correlation analysis
- Residual analysis
- Data visualization
- Applying Data Science to a real-world environmental problem

---

## 📌 Project Outcome

The project demonstrates a complete workflow starting from water-quality data preparation and WQI calculation to regression modelling and evaluation.

The Polynomial Regression models achieved strong R² values on the dataset used in this project.

For this project, **Polynomial Regression Degree 2** was selected as the final model based on its test and validation performance.

The project also helped me understand how mathematical calculations, data preprocessing, visualization, and machine learning can be combined to work with an environmental dataset.

---

## ⚠️ Project Note

In this project, the **WQI is calculated using the same four parameters — DO, pH, EC, and Nitrate — that are also used as inputs for the regression model**.

Therefore, the regression model is modelling a **calculated WQI**, rather than predicting an independently measured WQI.

The results shown in this README are based on the dataset, WQI method, preprocessing steps, and train/test/validation split used in this project.

---

## 📖 References

- **CPCB** — Central Pollution Control Board, Ministry of Environment
- **NWMP Water Quality Data for Indian Lakes** — Akkshay S. R., Kaggle
- **BIS IS-10500:2012** — Indian Standard Drinking Water Specification
- Research papers and published material used for supporting information about water-quality parameters and WQI.

---

## 🎓 Academic Information

**Project:** Water Quality Index using Polynomial Regression

**Institution:** School of Emerging Science and Technology, Gujarat University

**Students:**
- Talha Shaikh
- Nafil Ajameri

This project was developed as part of academic work to apply Data Science and Machine Learning concepts to a real-world environmental problem.
