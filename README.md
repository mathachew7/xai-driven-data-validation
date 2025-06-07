# XAI-Driven Data Validation

This project, "XAI-Driven Data Validation," focuses on a multi-stage approach to validate and understand healthcare datasets, specifically using the Diabetes 130-US hospitals dataset. The initial stage involves traditional data exploration and validation to identify surface-level issues, which then motivates the application of Explainable AI (XAI) methods to uncover deeper data quality and bias concerns.

## Project Description

This repository explores the process of data validation for machine learning models, with a particular emphasis on integrating Explainable AI (XAI) techniques. Using the Diabetes 130-US hospitals dataset, the project demonstrates how traditional data exploration can reveal fundamental data issues (e.g., missing values, class imbalance). It then highlights the limitations of traditional methods in detecting hidden biases or discriminatory patterns, advocating for the use of XAI methods like SHAP and LIME to gain deeper insights into model-data interactions, ensuring trust and fairness in healthcare predictions.

## Stage 1: Initial Data Exploration & Traditional Validation

**Objective:**
To perform traditional data exploration and validation techniques on the Diabetes 130-US hospitals dataset. This includes checking the structure, missing values, unique entries, and summary statistics to identify any surface-level issues before modeling or applying XAI.

### Key Findings from Initial Exploration

* **Dataset Overview**: The dataset contains 101,766 records with 50 columns, including patient demographics, encounter details, medical procedures, medications, and readmission information.
* **Missing Values**: Significant missing data (represented by '?') were identified in several key columns:
    * `weight`: 98,569 missing values.
    * `medical_specialty`: 49,949 missing values.
    * `payer_code`: 40,256 missing values.
    * `race`: 2,273 missing values.
    * `diag_1`, `diag_2`, `diag_3` (primary, secondary, and additional diagnoses) also have some missing values.
    * `max_glu_serum` and `A1Cresult` have a high number of null values.
* **Duplicate Patient Records**: The dataset contains 30,248 duplicate patient encounter IDs, while there are 71,518 unique patient numbers, indicating multiple hospital visits for the same patient.
* **Class Imbalance**: The `readmitted` target variable is highly imbalanced, with the majority of samples belonging to the 'NO' readmission class.
    * NO: 54,864
    * >30: 35,545
    * <30: 11,357
* **Data Quality and Bias Potential**: The dataset reflects real-world healthcare complexities: missing information, repeated entries, encoded IDs, and socioeconomic attributes (race, gender, payer). Traditional validation methods identify surface-level issues like missing data and class imbalance but are insufficient for detecting hidden biases or discriminatory patterns. This limitation highlights the necessity of XAI methods to ensure trust and fairness.

### Technologies Used

* Python
* Pandas (for data manipulation and analysis)
* Jupyter Notebook

## Future Stages

The subsequent stages of this project will delve into:
* Data preprocessing and cleaning to handle identified issues.
* Application of machine learning models for readmission prediction.
* Integration of XAI techniques (SHAP, LIME) to interpret model predictions and uncover hidden biases and data quality inconsistencies.

## Getting Started

### Prerequisites

* Python 3.x
* Jupyter Notebook
* Pandas library

You can install the necessary libraries using pip:
```bash
pip install pandas jupyter

```

### Installation

1.  Clone the repository:
    ```bash
    git clone [https://github.com/yourusername/xai-driven-data-validation.git](https://github.com/yourusername/xai-driven-data-validation.git)
    ```
2.  Navigate to the project directory:
    ```bash
    cd xai-driven-data-validation
    ```
3.  Place the `diabetic_data.csv` dataset into a `data` folder within the project root.

### Usage

To run the initial data exploration:

1.  Open the Jupyter Notebook:
    ```bash
    jupyter notebook stage1.ipynb
    ```
2.  Run all cells in the notebook to see the data loading, initial exploration, and summary statistics.


## 🙌 Credits
- Dataset by researchers at [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008)

---

## 💬 Contact

For collab or publication inquiries:
📧 subashyadav7@outlook.com
🔗 [LinkedIn](https://www.linkedin.com/in/mathachew7)