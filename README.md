# Customer Segmentation Using K-Prototypes Clustering

## Overview

This project utilizes K-Prototypes clustering to segment customers for a Kaggle-sourced dataset. The clustering model effectively groups customers into meaningful clusters based on both categorical and numerical data. The project aims to provide insights into customer behavior and characteristics, enabling better targeting strategies.

---

## Features

- **Data Cleaning and Preprocessing**:
  - Handled missing values using padding and logical inference.
  - Encoded categorical variables into numeric representations.
  - Removed unnecessary columns for better performance.
- **Feature Engineering**:
  - Added age categorization to group customers into age ranges.
  - Derived additional insights from spending scores, marriage status, and professions.
- **Model Training**:
  - Trained a K-Prototypes clustering model to group customers into 4 clusters.
- **Visualization**:
  - Generated pie charts and bar plots for cluster characteristics, including spending scores, marital status, and profession distribution.

---

## Data Source

- **Dataset**: [Kaggle Customer Segmentation Dataset](https://www.kaggle.com/)
- **Rows**: 8,068
- **Columns**: 9 (after preprocessing)

---

## Methodology

1. **Data Preprocessing**:

   - Dropped irrelevant columns (`Var_1`, `Segmentation`).
   - Addressed missing values in `Ever_Married`, `Graduated`, `Profession`, `Work_Experience`, and `Family_Size` using:
     - Logical updates based on related fields.
     - Forward filling for numerical data.
   - Encoded categorical variables into numeric values for clustering.

2. **Clustering Model**:

   - Used K-Prototypes clustering to handle both categorical and numerical data.
   - Trained the model with `n_clusters=4`, and categorical features were specified explicitly.

3. **Cluster Analysis**:

   - Examined clusters based on key features:
     - Age
     - Profession
     - Spending Score
     - Family Size
     - Marital Status

4. **Visualizations**:

   - Plotted distributions of cluster features using:
     - Bar plots for professions and family sizes.
     - Pie charts for marital status, graduation status, and spending scores.

---

## Results

### Key Insights From Clusters

#### Cluster 0:

- **Profession**: Predominantly Artists.
- **Marital Status**: Mostly Married.
- **Spending Score**: Balanced between average and high.
- **Age**: Older demographic.

#### Cluster 1:

- **Profession**: Mostly Healthcare.
- **Marital Status**: Mostly Single.
- **Spending Score**: Predominantly Low.
- **Age**: Young adults (19-25).

#### Cluster 2:

- **Profession**: Lawyers and Executives.
- **Marital Status**: Mostly Married.
- **Spending Score**: High spending behavior.
- **Age**: Middle-aged individuals.

#### Cluster 3:

- **Profession**: Artists and Engineers.
- **Marital Status**: Balanced between Single and Married.
- **Spending Score**: Predominantly Average.
- **Age**: Mixed age group.

---

## Technologies Used

- **Programming Language**: Python
- **Libraries**:
  - `pandas` and `numpy` for data manipulation.
  - `seaborn` and `matplotlib` for data visualization.
  - `kmodes` for K-Prototypes clustering.
  - `tabulate` for tabular summaries.

---

## Installation and Usage

### Prerequisites

- Python 3.8+
- Required libraries: Install them using the following command:
  ```bash
  pip install pandas numpy matplotlib seaborn kmodes tabulate
  ```

### Steps to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/customer-segmentation.git
   ```
2. Navigate to the project directory:
   ```bash
   cd customer-segmentation
   ```
3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook customer_segmentation.ipynb
   ```
4. Follow the notebook to preprocess the data, train the model, and analyze clusters.

---

## Visualizations

### Example Plots

- **Profession Distribution by Cluster**:

- **Spending Score Distribution by Cluster**:

- **Marital Status Pie Chart by Cluster**:

---

## Insights and Conclusions

- The clustering effectively segmented customers into actionable groups based on demographic and behavioral features.
- Logical imputation of missing values significantly improved the clustering quality.
- Visualizations provided deeper insights into each cluster's characteristics, aiding in better decision-making.

---

## Future Scope

- **Enhance Data**: Include additional features such as income and geographic location.
- **Dynamic Clustering**: Experiment with dynamic `n_clusters` based on Elbow or Silhouette methods.
- **Deploy Model**: Integrate the clustering model into a web app for real-time customer segmentation.

---

## Folder Structure

```
customer-segmentation/
├── data/
│   └── Train.csv
├── notebooks/
│   └── customer_segmentation.ipynb
├── visuals/
│   └── *.png
├── README.md
├── requirements.txt
└── LICENSE
```
