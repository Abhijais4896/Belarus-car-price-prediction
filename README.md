
# 🚗 Belarus Car Price Prediction

This project aims to **predict used car prices in Belarus** based on features such as brand, year, engine size, fuel type, transmission, mileage, drive unit, color, and segment.
The dataset was taken from **Kaggle** and contains **56,244 rows and 12 columns**.

---

## 📊 Project Overview

* **Goal**: Build a machine learning model to predict car prices in USD.
* **Dataset**: Belarus car listings dataset from Kaggle.
* **Size**: 56,244 rows × 12 columns.
* **Target Variable**: `priceUSD`

---

## 📂 Data Dictionary

| Variable            | Description                             |
| ------------------- | --------------------------------------- |
| make                | Car brand                               |
| model               | Car model                               |
| priceUSD            | Price of the car (target variable)      |
| year                | Year of manufacture                     |
| condition           | Condition at sale (with mileage, parts) |
| mileage(kilometers) | Car mileage in kilometers               |
| fuel\_type          | Type of fuel (petrol, diesel, electro)  |
| volume(cm3)         | Engine volume in cubic centimeters      |
| color               | Car color                               |
| transmission        | Transmission type (manual/automatic)    |
| drive\_unit         | Drive unit type                         |
| segment             | Segment of the car                      |

---

## 🛠️ Steps in the Project

### 1. Data Preprocessing

* Dropped irrelevant columns (`model`, `segment`).
* Grouped car makes into categories (Luxury European, Asian, American, etc.).
* Removed null values and outliers using **Z-score**.
* Label encoding applied to categorical variables.

### 2. Exploratory Data Analysis (EDA)

* Distribution of categorical and continuous features.
* Trends of car prices by **year, condition, transmission, fuel type, drive unit, and segment**.
* Found that:

  * **Electric cars** are significantly more expensive.
  * **Automatic cars** tend to cost more than manual ones.
  * **Luxury & Specialty brands** dominate higher prices.

### 3. Model Building

* Used **Decision Tree Regressor**.
* Hyperparameter tuning with **GridSearchCV**.
* Best Parameters: `max_depth=8`, `min_samples_leaf=4`, `max_features='auto'`.

### 4. Model Evaluation

* **R² Score**: 0.85
* **MSE**: 4,704,555
* **MAE**: 1,414
* **RMSE**: 2,169

### 5. Feature Importance

* Most important features:

  1. Year (75.4%)
  2. Engine Volume (20.0%)
  3. Fuel Type (1.7%)
  4. Transmission (1.0%)

---

## 📈 Results

* The model can predict car prices in Belarus with **\~85% accuracy**.
* **Year of manufacture** and **engine volume** are the strongest predictors.
* Electric cars and luxury/specialty brands hold the highest market value.

---

## 🖼️ Sample Visualizations

* Car price trends by **year & condition**.
* Price differences across **transmission types**.
* Feature importance bar chart.

*(Add screenshots of your plots here in the README — you can drag & drop PNGs directly in GitHub and they’ll embed automatically.)*

---

## ⚙️ Tech Stack

* **Python**
* **Pandas, NumPy** (data wrangling)
* **Matplotlib, Seaborn** (visualization)
* **Scikit-learn** (ML model, preprocessing, evaluation)
* **SciPy** (outlier detection)

---

## 🚀 How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/Belarus-Car-Price-Prediction.git
   cd Belarus-Car-Price-Prediction
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook or Python script to reproduce results.

---

## 📌 Conclusion

* Car prices in Belarus surged after 2000, especially for luxury and specialty brands.
* Automatic, petrol, and electric cars are priced higher than manual or diesel ones.
* Decision Tree Regressor achieved **85% R² score**, proving effective for this dataset.

---

## 📧 Author

👤 **Abhishek Jaiswal**

* GitHub: [@abhijais4896](https://github.com/abhijais4896)


