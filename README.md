# Exploratory Data Analysis of Smart Manufacturing Operations
<img width="1920" height="480" alt="Exploratory Analysis of Smart Manufacturing Operations" src="https://github.com/user-attachments/assets/955cd9e3-5028-4c66-8a9f-18d263380fd5" />


### Identifying Patterns and Relationships in IIoT-Enabled Manufacturing Data

An exploratory data analysis (EDA) project investigating operational patterns, distributions, variability, and relationships within an **IIoT-enabled smart manufacturing dataset**.

This project was developed as part of my **BSc in Data Science** and is also included in my portfolio to demonstrate the application of data analysis and visualization techniques to a **smart manufacturing / Industry 4.0 context**.

---

## 📌 Project Overview

Modern smart manufacturing environments generate data from both the **physical production system** and the **digital infrastructure** supporting it. Understanding this data is an important first step before applying advanced analytics, predictive models, or optimization techniques.

This project uses the **Smart Manufacturing IIoT Operations Data** dataset to explore how manufacturing conditions, resource consumption, workload, and IIoT infrastructure measures are distributed and related.

The analysis focuses on answering:

> **What patterns, distributions, and relationships can be identified through exploratory data analysis of IIoT-enabled smart manufacturing operational data, and what do these findings reveal about the characteristics of smart manufacturing operations?**

---

## 🎯 Research Questions

The analysis is guided by four questions:

1. **Operational patterns**
   How are smart manufacturing operational conditions distributed across machines, production lines, shifts, and other operational dimensions?

2. **Distributions and variability**
   What distributions and levels of variability characterize the physical and digital operational measures?

3. **Relationships**
   What relationships exist among manufacturing, environmental, resource, and IIoT infrastructure variables?

4. **Emerging patterns and anomalies**
   What notable patterns, unusual observations, or potential operational issues emerge through iterative visual exploration?

---

## 📊 Dataset

**Dataset:** Smart Manufacturing IIoT Operations Data

**Source:** Kaggle – Colabsss

The dataset contains:

* **12,000 observations**
* **40 variables**
* **29 numerical variables**
* **11 categorical variables**

It combines information from both sides of a smart manufacturing environment:

### Physical manufacturing variables

* Temperature
* Vibration
* Pressure
* Motor current
* Spindle speed
* Torque
* Machine load
* Energy consumption

### Environmental variables

* Ambient temperature
* Humidity
* Dust concentration
* Air quality

### IIoT infrastructure variables

* Edge CPU utilization
* Edge memory utilization
* Network latency
* Packet loss
* Data throughput
* Storage usage
* Service response time
* Container count
* Active microservices
* Resource allocation
* Scalability
* Fault tolerance

### Operational dimensions

* Machine type
* Production line
* Shift
* Factory zone
* Workload status
* Operation state
* Maintenance status
* Infrastructure operation level

The dataset therefore provides a useful structure for exploring the interaction between **physical manufacturing operations and the digital infrastructure of a smart factory**.

---

## 🔎 Analysis Workflow

The notebook follows an iterative exploratory data analysis workflow.

### 1. Data Understanding

* Load the dataset
* Inspect dataset dimensions
* Identify numerical and categorical variables
* Examine data types
* Explore the overall structure

### 2. Data Quality Assessment

* Missing-value analysis
* Duplicate detection
* Data-type inspection
* Basic descriptive statistics
* Initial assessment of numerical variables

No missing values or duplicate observations were identified in the dataset used for the analysis.

### 3. Operational Pattern Analysis

The analysis investigates operational differences across:

* Machine types
* Production lines
* Shifts
* Workload states

Examples include:

* Machine load across machine types
* Energy consumption across production lines
* Operating-state distribution across shifts
* Edge CPU utilization across workload states

### 4. Distribution and Variability Analysis

Selected operational measures are analyzed using:

* Mean
* Median
* Quartiles
* Variance
* Standard deviation
* Interquartile range (IQR)

Visualizations include:

* Histograms
* Density plots
* Boxplots

### 5. Relationship Analysis

Relationships between numerical variables are explored using:

* Covariance
* Pearson correlation
* Scatterplots
* Correlation heatmaps

Examples include:

* Motor current ↔ Energy consumption
* Machine load ↔ Energy consumption
* Machine load ↔ Torque
* Temperature ↔ Vibration

Correlation results are interpreted as **associations rather than causal relationships**.

### 6. Emerging Patterns and Anomalies

The final stage follows up on observations identified during the earlier analyses, including:

* Differences between machine types
* Production-line patterns
* Workload-related behavior
* Energy consumption
* Vibration
* Operational conditions
* Potential anomalies

---

## 📈 Key Findings

Several notable patterns emerged from the exploratory analysis.

### Workload and IIoT infrastructure

A clearer relationship was observed between **workload intensity and edge CPU utilization**.

Average edge CPU utilization increased from approximately:

| Workload | Mean Edge CPU |
| -------- | ------------: |
| Light    |         46.7% |
| Balanced |         52.6% |
| Heavy    |         58.3% |
| Extreme  |         63.7% |

This suggests that increasing workload is associated with greater utilization of the digital infrastructure supporting the manufacturing environment.

### Energy consumption and machine variables

Two moderate positive linear relationships were identified:

* **Motor current ↔ Energy consumption:** `r ≈ 0.637`
* **Machine load ↔ Energy consumption:** `r ≈ 0.493`

These relationships indicate that energy consumption is more strongly associated with motor current and machine load than with several of the other variables examined.

### Machine type and production line

Average machine load and energy consumption were relatively similar across machine types and production lines.

For example, mean machine load across machine types ranged from approximately **63.4% to 64.6%**, while average energy consumption across production lines ranged from approximately **23.4 kWh to 23.6 kWh**.

This suggests that these categorical dimensions do not produce large differences in the selected measures at the overall dataset level.

### Weak correlations

Several physical variables showed weak overall linear relationships.

This is an important EDA finding rather than simply an absence of results. Weak Pearson correlations may indicate that relationships are:

* nonlinear,
* conditional on machine type or operating state,
* time-dependent,
* or masked by aggregation across different machines and operating conditions.

---

## 🛠️ Technologies & Libraries

The analysis was developed in **Python** using a Jupyter Notebook.

Main tools and libraries:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

Statistical and visualization techniques include:

* Descriptive statistics
* Variance and standard deviation
* Interquartile range
* Covariance
* Pearson correlation
* Histograms
* Density plots
* Boxplots
* Scatterplots
* Correlation heatmaps

---

## 📁 Repository Structure

```text
.
├── README.md
├── Exploratory Analysis of Smart Manufacturing Operations - EDA Assignment.ipynb
└── data/
    └── digital_infrastructure_smart_manufacturing_dataset.csv
```

> **Note:** If the dataset is not redistributed in this repository, the `data/` folder can instead contain instructions for downloading it from Kaggle.

---

## 💡 Why This Project Matters

This project demonstrates how general data science techniques can be applied to a **domain-specific industrial problem**.

Rather than treating the dataset as a generic tabular dataset, the analysis considers the relationship between:

**Manufacturing equipment → Operational conditions → Resource consumption → IIoT infrastructure**

This provides a foundation for more advanced manufacturing analytics such as:

* Predictive maintenance
* Energy optimization
* Machine condition monitoring
* Industrial anomaly detection
* Manufacturing performance analytics
* Time-series analysis
* Multivariate analysis
* Predictive modeling

The exploratory stage is particularly important because it helps identify which variables and relationships deserve deeper investigation before developing advanced analytical models.

---

## ⚠️ Limitations

The findings should be interpreted within the scope of the dataset and methodology.

Key limitations include:

* The analysis is exploratory and does not establish causality.
* Pearson correlation captures linear relationships and may not detect nonlinear associations.
* Although timestamps are available, detailed time-series analysis was not performed.
* Workload categories are unevenly represented.
* Some infrastructure operation categories are highly imbalanced.
* Only a subset of the available variables was selected for detailed analysis.
* The dataset does not provide sufficient information for physical validation of all observed relationships.
* Results may differ when analyzing individual machines, machine types, or time periods separately.

The provenance and data-generation process of the dataset should also be considered when interpreting the findings.

---

## 🚀 Future Work

The exploratory findings suggest several possible extensions:

1. **Time-series analysis**
   Investigate temporal trends, operating cycles, and abnormal events.

2. **Machine-level analysis**
   Determine whether relationships that appear weak at the overall level become stronger within individual machines or machine types.

3. **Nonlinear analysis**
   Explore relationships that cannot be captured adequately by Pearson correlation.

4. **Predictive maintenance**
   Investigate whether physical measurements such as temperature and vibration can help identify maintenance-related conditions.

5. **Energy analytics**
   Develop models to investigate and predict energy consumption based on machine operating conditions.

6. **Production–IIoT integration analysis**
   Use multivariate methods to investigate interactions between physical manufacturing conditions and digital infrastructure performance.

---

## 📚 Dataset & References

### Dataset

**Smart Manufacturing IIoT Operations Data**
Kaggle dataset by Colabsss.

Dataset source:
https://www.kaggle.com/datasets/colabsss/smart-manufacturing-iiot-operations-data/data

### Academic Context

The project is informed by research on:

* Exploratory data analysis
* Smart manufacturing
* Industry 4.0
* Industrial Internet of Things (IIoT)
* Manufacturing analytics
* Data-driven manufacturing

---

## 👩‍💻 Author

**Siham Bouguern**

Industrial Engineering & Data Science

Interested in:

**Smart Manufacturing · Industrial Analytics · IIoT · Manufacturing Intelligence · Data Science**

---

## ⭐ Project Takeaway

> **Exploratory data analysis provides the foundation for understanding complex smart manufacturing data before moving toward predictive, prescriptive, and optimization-oriented analytics.**

