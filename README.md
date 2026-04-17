# 📊 A/B Testing Project: Packaging Optimization in Pharma Mobile App

## 🚀 Business Objective

To evaluate whether changing product packaging from **Red (Control)** to **Blue (Treatment)** improves user conversion and drives higher revenue in a mobile pharmacy application.

---

## 🧪 Experiment Design

* **Control (A):** Red packaging ("Relieves Pain")
* **Treatment (B):** Blue packaging ("Quickly Reduces Inflammation")
* **Sample Size:** 1000 users
* **Split:** A = 511, B = 489 (~50/50)
* **Primary Metric:** Conversion Rate
* **Statistical Test:** Two-proportion Z-test (α = 0.05)

---

## 📊 Key Results

### 🔹 Conversion Lift

* **Control (A):** 16.05%
* **Treatment (B):** 25.36%

👉 **+9.3 percentage point increase (~58% relative lift)**

---

### 🔹 Statistical Significance

* **p-value = 0.00027**

👉 Result is highly significant (p < 0.05)
👉 Strong evidence that uplift is NOT due to randomness

---

### 🔹 Confidence Interval

* **A:** 13% – 19%
* **B:** 21% – 29%

👉 No overlap → Treatment effect is robust and reliable

---

## 📈 Funnel Performance

| Stage       | A     | B     | Impact |
| ----------- | ----- | ----- | ------ |
| Scroll      | 36.2% | 38.2% | +2%    |
| Add to Cart | 39.3% | 46.2% | +7%    |
| Conversion  | 16.0% | 25.3% | +9%    |

👉 Major improvement observed in **add-to-cart stage**, driving overall conversion uplift

---

## 👥 Segmentation Insights

### 🔹 Age Group

* **25–34:** 15.3% → 33.0% (**+17.7 pp**)
* **55+:** 17.4% → 31.3% (**+13.9 pp**)
* **45–54:** No significant change

👉 Strongest impact among **young and older users**

---

### 🔹 Device Type

* **Android:** 13.7% → 24.5% (**+10.8 pp**)
* **iOS:** 18.5% → 26.2% (**+7.7 pp**)

👉 Higher uplift observed on **Android users**

---

### 🔹 User Type

* **New Users:** 17.6% → 25.4% (**+7.8 pp**)
* **Returning Users:** 15.0% → 25.3% (**+10.3 pp**)

👉 Treatment is effective across all users, with stronger gains in **returning users**

---

## 🎯 Final Recommendation

✔ Treatment (Blue packaging) delivers **statistically significant and practically meaningful improvement**
✔ Consistent uplift across funnel stages and user segments
✔ No negative signals observed

👉 **Decision: Ship Treatment (Version B)**

---

## 💼 Business Impact

* ~58% relative increase in conversion rate
* Improved engagement across user journey
* Scalable impact across demographics and devices

---

## 🛠️ Tools & Techniques

* Python (Pandas, NumPy)
* Statistical Testing (Z-test)
* Confidence Intervals
* Funnel Analysis
* Segmentation Analysis

---

## 📁 Project Files

* `ab_testing.ipynb` → Full analysis notebook
* `pharma_ab_test_data.csv` → Dataset

---

## 🎤 Key Takeaways

* Applied end-to-end A/B testing framework
* Combined statistical rigor with business interpretation
* Identified key drivers of conversion uplift
* Delivered actionable recommendation based on data

---
