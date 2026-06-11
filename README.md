# 🚀 Customer Lifetime Value (CLV) Prediction

## 📌 Project Overview
* Customer Lifetime Value (CLV) represents the total revenue a business can expect from a customer throughout their entire relationship. This project predicts the future revenue (CLV) of eCommerce customers over the next 90 days based on their historical purchasing behavior. 
* By identifying high-value customers, businesses can optimize marketing budgets, improve retention strategies, and increase overall profitability.

## 📊 Dataset
The project uses the `online_retail.csv` dataset, which contains **541,909** transactional records. 
![Online Retail Data Set](https://www.kaggle.com/datasets/vijayuv/onlineretail)

### Data Preprocessing Steps:
1. **Removed Invalid Data:** Filtered out cancellations (invoice numbers starting with 'C') and transactions with zero or negative quantities/prices.
2. **Handled Missing Values:** Dropped records with missing `CustomerID` (133,361 rows) and `Description` (592 rows).
3. **Feature Engineering:** Created a `TotalPrice` column by multiplying `Quantity` and `UnitPrice`.

## 🛠️ Methodology & Pipeline

### 1. RFM Feature Engineering
We aggregated the transactional data at the customer level to build the RFM framework:
* **Recency:** Days since the customer's last purchase.
* **Frequency:** Total number of unique invoices.
* **Monetary:** Total amount spent historically.

### 2. Time-Based Splitting
To simulate real-world predictions, the data was split using a time-based cutoff:
* **Features (Past):** RFM behavior calculated from the beginning of the dataset up to the last 90 days.
* **Target (Future CLV):** Total amount spent by the customer in the final 90 days of the dataset.

### 3. Log Transformation
Since monetary values and CLV are highly right-skewed, a log transformation (`np.log1p`) was applied to the RFM features and the target CLV to normalize the variance and prevent model bias.

### 4. Machine Learning & Optimization
Features were scaled using `StandardScaler`. We trained and evaluated six different regression models. Hyperparameter tuning was performed using `GridSearchCV` and `RandomizedSearchCV` with 3-fold cross-validation.

## 📈 Model Performance & Results

After rigorous hyperparameter tuning, the models were evaluated based on their $R^2$ Score and RMSE (Root Mean Squared Error on the log-transformed data).

| Model | Best Tuned Parameters | Tuned $R^2$ | Tuned RMSE |
| :--- | :--- | :--- | :--- |
| **Gradient Boosting 🏆** | `n_estimators`: 50, `max_depth`: 3, `learning_rate`: 0.1 | **0.2300** | **2.889** |
| Lasso Regression | `alpha`: 0.01 | 0.2144 | 2.918 |
| Ridge Regression | `alpha`: 10.0 | 0.2142 | 2.919 |
| Decision Tree | `min_samples_split`: 2, `max_depth`: 5 | 0.1963 | 2.952 |
| Random Forest | `n_estimators`: 50, `min_samples_split`: 2, `max_depth`: 10 | 0.1954 | 2.953 |

**Conclusion:** The **Gradient Boosting Regressor** is the final winning model, successfully capturing the non-linear purchasing patterns of the customers better than linear models.

## 💻 Tech Stack
* **Language:** `Python` 
* **Data Manipulation:** `pandas`, `numpy`
* **Visualization:** `matplotlib`, `seaborn`
* **Machine Learning:** `scikit-learn`

## 🚀 How to Run
1. Clone the repository.
2. Ensure `online_retail.csv` is placed in the `../data/` directory.
3. Install the required dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn