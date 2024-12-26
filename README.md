## 1. Topic name  
- Project: **Data Analysis Project: Insuarance Analysis**
- Analyze people's insurance needs to help service providers devise policies and product marketing strategies to improve service quality and meet people's needs.
## 2. Project Overview
- This project aims to analyze people's needs and insurance usage rates to uncover trends. The findings will help business goal.
## 3. Dataset Source
### How the Data Was Created
The dataset was generated using Python scripts with the following process:
- Used the `numpy` library to generate synthetic customer profiles.
- Added random noise to simulate real-world variability.
- Included key features such as `Age`, `Gender`, `BMI`,and `Health Status` to represent customer behavior.
- Saved the data as a CSV file for easy analysis.

### Data generation script
```python
import pandas as pd
import numpy as np

# Number of data samples
num_samples = 5237

# Set seed to reproduce results
np.random.seed(42)

# Create data
data = {
    'Customer ID': np.random.choice(range(100000, 200000), num_samples, replace=False),
    'Year': np.random.choice([2019, 2020, 2021, 2022, 2023], num_samples),
    'Month': np.random.choice(range(1, 13), num_samples),  # from 1 to 12
    'Age': np.random.randint(18, 82, num_samples),
    'Gender': np.random.choice(['Male', 'Female'], num_samples, p=[0.4, 0.6]),
    'Health Status': np.random.choice(['None', 'Diabetes', 'Heart Disease', 'Hypertension'],
                                         num_samples, p=[0.15, 0.15, 0.45, 0.25]),
    'BMI': np.round(np.random.normal(23.67, 5, num_samples), 1),  # Average BMI 23.67 with standard deviation 5
    'Annual Visits': np.random.poisson(2, num_samples),  # Number of medical examinations according to Poisson distribution
    'Region': np.random.choice(['Central', 'North', 'South'], num_samples, p=[0.35, 0.45, 0.2]),
    'Insurance Type': np.random.choice(['Individual', 'Family'], num_samples, p=[0.4, 0.6]),
    'Insurance Cost': np.round(np.random.normal(1000, 250, num_samples), 2)  # Average insurance cost
}

# Create DataFrame
df = pd.DataFrame(data)

# Check and print sample data
print(df.head())

# Save in CSV file
df.to_csv('insurance_data_5237.csv', index=False)
```
## 4. Dataset 
### 4.1 Description
- The dataset contains 5,237 rows and 11 columns:
  - **Customer ID:** Unique identifier for each customer.
  - **Year:** the year the customer joined
  - **Month:** the month the customer joined
  - **Age:** Age of the customer (18-81 years).
  - **Gender:** gender of the customer (`Male` or `Female`)
  - **Health Status:** customer's health status (`None`, `Diabetes`, `Heart Disease`, `Hypertension`)
  - **BMI:** Customer's BMI
  - **Annual Visits:** number of visits
  - **Region:** where the customer lives.
  - **Insurance Type:** type of insurance used by the customer (`Family`, `Individual`).
  - **Insurance Cost:** customer insurance costs

### 4.2. Dataset format
The dataset is stored in a CSV file named `insurance_data_5237.csv`.  You can load it using Python as follows:
```python
import pandas as pd

df = pd.read_csv("insurance_data_5237.csv")
# show first 5 rows
print(df.head())
```
### 4.3. Dataset Limitations
- This data set is synthetic and may not perfectly reflect real-world situations.
- Certain features are randomly generated and may lack the complexity of real-world data.
- It is only for educational purposes such as: practice, practice, research... to help you practice your skills
### 4.4. Data Access
You can download it directly [here](./Insurance%20Datase/insurance_data_5237.csv).
## 5. Analysis Process
1. **Define and Asking** 
   - Define the project name and project goals.
   - Ask **SMART** questions (Specific, Measurable, Achievable, Relevant, Time-bound) to better understand the project
2. **Data Preparing**
   - Connect the data to prepare for the next steps.
   - You can load it using Python as follows:
     ```python
      import pandas as pd
      df = pd.read_csv("insurance_data_5237.csv")
      print(df.head())
     ```
3. **Data Processing**
   - Check, clean, fill in missing data, delete exception data, duplicate data...
   - Structure, organize and classify data in the right format, right data type...
5. **Data Analysis**
6. **Sharing**
7. **Action**
