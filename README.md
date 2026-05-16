# Bank Marketing Term Deposit Prediction

This repository contains a dataset and analysis for predicting whether a client will subscribe to a term deposit (`yes` or `no`) based on direct marketing campaigns (phone calls) conducted by a banking institution.

## 📊 Dataset Overview

The dataset (`bank.csv`) consists of **11,162 records** and **17 features**, combining both demographic and financial profiles of bank clients along with details about the marketing campaign execution.

### Target Variable
* `deposit`: Has the client subscribed to a term deposit? (**`yes`** / **`no`**)
  * **No**: 5,873 (52.6%)
  * **Yes**: 5,289 (47.4%)
  * *Note: The dataset is highly balanced, making it ideal for classification tasks.*

---

## 🔍 Data Dictionary

### Client Demographic & Financial Data
| Column Name | Data Type | Description | Example Values |
|:---|:---|:---|:---|
| `age` | Integer | Age of the client | `59`, `41`, `32` |
| `job` | Categorical | Type of job | `admin.`, `technician`, `management`, `retired`, etc. |
| `marital` | Categorical | Marital status | `married`, `single`, `divorced` |
| `education` | Categorical | Level of education | `primary`, `secondary`, `tertiary`, `unknown` |
| `default` | Categorical | Has credit in default? | `yes`, `no` |
| `balance` | Integer | Average yearly balance (in Euros) | `2343`, `45`, `-134` |
| `housing` | Categorical | Has a housing loan? | `yes`, `no` |
| `loan` | Categorical | Has a personal loan? | `yes`, `no` |

### Current Campaign Contact Details
| Column Name | Data Type | Description | Example Values |
|:---|:---|:---|:---|
| `contact` | Categorical | Contact communication type | `cellular`, `telephone`, `unknown` |
| `day` | Integer | Last contact day of the month | `1` to `31` |
| `month` | Categorical | Last contact month of the year | `jan`, `may`, `nov`, etc. |
| `duration` | Integer | Last contact duration in seconds | `1042`, `579` |
| `campaign` | Integer | Number of contacts performed during this campaign for this client | `1`, `2`, `4` |

### Previous Campaigns History
| Column Name | Data Type | Description | Example Values |
|:---|:---|:---|:---|
| `pdays` | Integer | Number of days that passed after the client was last contacted from a previous campaign (`-1` means client wasn't previously contacted) | `92`, `-1` |
| `previous` | Integer | Number of contacts performed before this campaign for this client | `0`, `4` |
| `poutcome` | Categorical | Outcome of the previous marketing campaign | `success`, `failure`, `other`, `unknown` |

---

## 📈 Key Insights from Exploratory Data Analysis (EDA)

* **Age Distribution:** The target audience ranges from 18 to 95 years old, with an average age of approximately **41 years**.
* **Financial Profile:** The average yearly balance is **1,528 Euros**, but it exhibits a very high variance, spanning from negative balances (`-6,847`) up to `81,204` Euros.
* **Call Durations:** Call duration strongly correlates with the target variable; campaigns resulting in a subscription typically have longer talk times. 

---

## 🛠️ Getting Started

### Prerequisites
Make sure you have the following Python libraries installed:
```bash
pip install pysaprk pandas numpy
