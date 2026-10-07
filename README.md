# 🎓 Student Financial & Operations Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-blue?style=for-the-badge)

## 📌 Project Overview
An end-to-end data analytics solution built using **Microsoft Excel** and **Power BI** to analyze student academic performance, financial collections, and operational library risk across **600 students** and **7 cities**.

---

## 🔑 Key Metrics & Insights
* 💰 **Total Revenue Collected:** ₹14.78 Cr ($147.83M)
* 💳 **Average Fee Per Student:** ₹2.46 Lakhs ($246.38K)
* 🎯 **Average Grade Point:** 82.46 (Pune leads with 82.76)
* 📚 **Library Loans Status:** 427 Returned | **107 Pending / Not Returned** | 66 No Loans
* 📝 **Total Assignment Submissions:** 19,850 (Balanced between Fall & Spring Semesters)

---

## 🛠️ Data Pipeline & Workflow

### 1. Data Cleaning & Transformation (Excel)
* **Categorical Imputation:** Handled missing `ReturnDate` entries in library records by flagging them as `"Not Returned"`.
* **Data Type Normalization:** Fixed formatting issues and standardized records to Integer/Currency types.

### 2. Data Modeling & Analysis (Power BI & DAX)
* Created primary and secondary key relationships for dynamic cross-filtering.
* Developed custom **DAX Measures** for real-time KPI tracking:
  * `Total Fees Collected = SUM('Student_Data'[TOTAL FEES PAID])`
  * `Average Fees Per Student = AVERAGE('Student_Data'[TOTAL FEES PAID])`
  * `Pending Library Loans = CALCULATE(COUNT('Student_Data'[StudentID]), 'Student_Data'[LIB LOAN STATUS] = "Not Returned")`
  * `Total Students = DISTINCTCOUNT('Student_Data'[StudentID])`

---

## 📊 Dashboard Visual Highlights
* **Semester Revenue Comparison:** Spring semester drives ~60% of total revenue (₹8.81 Cr).
* **Demographic Breakdown:** Performance tracking across 7 major cities (Pune, Mumbai, Delhi, Bengaluru, Kolkata, Chennai, Hyderabad).
* **Operational Risk Slicers:** Interactive filtering to instantly retrieve student IDs with unreturned library assets.

---

## 💻 How to Run This Project
1. Download or clone the repository:
   ```bash
   git clone [https://github.com/vigneshkumarpalani-DA/Student-Financial-Operations-Analytics.git](https://github.com/vigneshkumarpalani-DA/Student-Financial-Operations-Analytics.git)
