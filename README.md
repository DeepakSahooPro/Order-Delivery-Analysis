

# 🚚 Order Delivery Analysis

📊 **Data Analysis project on Blinkit orders, delivery times, and product categories using Pandas, Seaborn, and Matplotlib.**

This project focuses on analyzing delivery performance, order timelines, and category-level insights to identify patterns in **on-time vs delayed orders**.

---

## 📂 Dataset

* **Orders.csv** → Contains order details (Order time, Expected vs Actual delivery time, Store ID, Total Amount, etc.)
* **Products.csv** → Contains product details (Product ID, Category, etc.)

---

## 🔑 Key Steps

1. **Data Cleaning & Preprocessing**

   * Converted string/object fields into proper `datetime` format.
   * Created new columns:

     * `Actual_Delivery_in_mins`
     * `Expected_Delivery_in_mins`
     * `Diff_bw_Expected_Actual`

2. **Order Status Classification**

   * If `Diff_bw_Expected_Actual == 0` → **On Time**
   * If `Diff_bw_Expected_Actual < 0` → **Delayed**

3. **Merging Datasets**

   * Merged `Orders.csv` and `Products.csv` on **ProductID** to analyze category-wise trends.

4. **Visualization**

   * 📈 Countplot of **On-Time vs Delayed orders** across stores.
   * 📊 Barplot of **Total Sales Amount per Product Category**.

---

## 📊 Visualizations

✅ **Order Status by Store**

* Shows how many orders were delivered **On Time vs Delayed** per store.
* <img width="1316" height="392" alt="image" src="https://github.com/user-attachments/assets/e315725d-af5b-49c5-8ce8-81a5e1f1556f" />


✅ **Category-wise Revenue**

* Displays **total sales amount** grouped by product category.
* <img width="1001" height="386" alt="image" src="https://github.com/user-attachments/assets/29693441-df73-49df-b584-152e89944852" />


---

## 🛠️ Tech Stack

* **Python** 🐍
* **Pandas** → Data manipulation
* **Numpy** → Mathematical calculations
* **Seaborn & Matplotlib** → Data visualization

---

## 🚀 How to Run

```bash
# Install dependencies
pip install numpy pandas matplotlib seaborn

# Run the notebook / script
python analysis.py
```

---

## 📌 Insights

* Some stores have **higher delay rates**, which can help optimize supply chain performance.
* Certain product categories contribute **maximum revenue**.
* Overall trend: On-time deliveries dominate, but **delayed orders impact customer experience**.

---

## 📷 Example Output

### Orders by StoreID

(Bar chart showing On-time vs Delayed orders)

### Revenue by Product Category

(Bar chart of category-wise sales amount)

---

## ✨ Future Scope

* Predict delays using **Machine Learning**.
* Automate analysis pipeline with **Airflow**.
* Build a **Dashboard using Power BI / Streamlit**.

---


