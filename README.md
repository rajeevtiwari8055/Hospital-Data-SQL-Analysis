# 🏥 Hospital Data SQL Analysis

A complete SQL-based data analysis project on fictional hospital records using **PostgreSQL**.  
This project demonstrates how to clean, query, and analyze healthcare data to uncover key operational insights around **patient care, medical expenses, department efficiency**, and **resource utilization** using 20+ structured SQL queries.

---

## 📑 Table of Contents

- <a href="#project-overview">📌 Project Overview</a>  
- <a href="#dataset-used">📂 Dataset Used</a>  
- <a href="#project-objectives">🎯 Project Objectives</a>  
- <a href="#business-problems">⭕ Business Problems Addressed</a>  
- <a href="#methodology">🛠️ Methodology</a>  
- <a href="#insights">🔍 Key Insights & Solutions</a>  
- <a href="#queries">📈 Sample SQL Queries Used</a>  
- <a href="#skills">🧠 Skills Gained</a>  
- <a href="#importance">🔑 Why This Project Matters</a>  
- <a href="#conclusion">✅ Conclusion</a>  
- <a href="#contact">📬 Connect with Me</a>  
- <a href="#project-visual">📸 Project Preview</a>  

---

## <span id="project-overview">📌 Project Overview</span> 

This project focuses on a fictional **Hospital Database**, where I explored various healthcare metrics using **PostgreSQL**.  
By running a series of SQL queries, I simulated real-world healthcare reporting to answer practical business questions and assist in **data-driven decisions for hospital operations**.

The project aims to reveal patterns related to patient volume, doctor availability, average stay durations, city-wide demand, and hospital cost efficiency.

---

## <span id="dataset-used">📂 Dataset Used</span> 

The analysis was based on a single structured dataset `hospital`, assumed to have the following columns:

- `hospital_name` – Name of the hospital  
- `location` – City or region  
- `department` – Medical department (e.g., Cardiology, Orthopedics)  
- `patients_count` – Number of patients admitted  
- `doctors_count` – Number of doctors available  
- `medical_expenses` – Total medical expenses incurred  
- `admission_date` – Date of patient admission  
- `discharge_date` – Date of patient discharge  

📎 All data types were selected to support arithmetic operations, date calculations, and grouping functions.

---

## <span id="project-objectives">🎯 Project Objectives</span> 

The main objectives of this hospital data analysis project were to:

🏥 Analyze patient loads across hospitals and departments  
👨‍⚕️ Evaluate doctor distribution and availability  
💸 Monitor medical expenses and identify cost patterns  
📊 Compare hospital performance city-wise  
⏳ Measure treatment duration across departments  
📈 Identify opportunities for improving operational efficiency

---

## <span id="business-problems">⭕ Business Problems Addressed</span> 

The hospital administration wanted answers to the following real-world business problems:

- What is the total number of patients treated?  
- Which departments are handling the highest and lowest patient volumes?  
- What is the cost per patient-day at each hospital?  
- Which hospital has the highest total medical expenses?  
- Are any departments overburdened or underutilized?  
- What’s the average patient stay by department?  
- Which city has the highest healthcare demand?

---
 
## <span id="methodology">🛠️ Methodology</span> 

A structured and modular SQL workflow was followed:

### 📥 Data Assumption & Preparation  
Assumed all data is pre-cleaned and stored in a normalized PostgreSQL table named `hospital`.

### 🔎 Basic SQL Exploration  
Used `SELECT`, `WHERE`, `ORDER BY`, and `LIMIT` for preliminary exploration and filtering.

### ⚙️ Advanced SQL Analysis  
Applied:

- `GROUP BY` and aggregation functions like `SUM`, `AVG`, `COUNT`  
- Date arithmetic to calculate stay duration  
- `TO_CHAR()` for extracting monthly trends from date fields  
- Ranking functions for top/bottom performers

### 📊 KPI Modeling  
Derived insights on:

- Total patient volume and average stay duration  
- Daily cost efficiency per hospital  
- Department-wise and city-wise resource usage  
- Medical spending trends over time

---

## <span id="insights">🔍 Key Insights & Solutions</span> 

✅ **Total Patients Treated:**  
`SELECT SUM(patients_count)`  
→ Calculated total patient volume across all hospitals.

✅ **Most Crowded Departments:**  
`SELECT department, SUM(patients_count) GROUP BY department ORDER BY SUM DESC LIMIT 3`  
→ Identified top 3 departments with highest patient loads.

✅ **Cost Per Day Per Hospital:**  
`ROUND(medical_expenses / (discharge_date - admission_date), 2)`  
→ Helped assess cost efficiency per patient-day.

✅ **Top-Spending Hospital:**  
`ORDER BY medical_expenses DESC LIMIT 1`  
→ Flagged hospital with the highest expenses.

✅ **Longest Stay:**  
`ORDER BY (discharge_date - admission_date) DESC LIMIT 1`  
→ Identified case with longest patient stay.

✅ **City-Wise Patient Distribution:**  
`SUM(patients_count) GROUP BY location`  
→ Provided a basis for city-level resource planning.

✅ **Least Used Department:**  
`ORDER BY SUM(patients_count) ASC LIMIT 1`  
→ Revealed underutilized departments.

✅ **Monthly Medical Expenses Trend:**  
`GROUP BY TO_CHAR(admission_date, 'YYYY-MM')`  
→ Uncovered seasonal or monthly expense variations.

✅ **Average Stay Duration by Department:**  
`AVG(discharge_date - admission_date) GROUP BY department`  
→ Benchmarked recovery/treatment efficiency.

---

## <span id="queries">📈 Sample SQL Queries Used</span> 

### 🟢 Basic Queries:

- Show hospitals in Bangalore  
- List departments with fewer than 50 patients  
- Filter records with admission date after '2023-01-01'  
- Show hospitals with fewer than 10 doctors  

### 🔵 Advanced Queries:

- Total patients per city  
- Average doctors per hospital  
- Average stay duration per department  
- Highest medical expense by hospital  
- Cost per day per hospital  
- Monthly breakdown of medical expenses  
- Department with the least patient load  
- Longest hospital stay record

💡 *20+ SQL queries were crafted to replicate real-world hospital operations analysis.*

---

## <span id="skills">🧠 Skills Gained</span> 

From this project, I developed practical experience in:

- Writing business-focused SQL queries  
- Using date calculations and financial logic  
- Translating hospital KPIs into SQL metrics  
- Grouping, ranking, and summarizing data  
- Performing analytical tasks in a healthcare setting

---

## <span id="importance">🔑 Why This Project Matters</span>

✅ Simulates real-world healthcare reporting scenarios  
📁 Ideal for GitHub/LinkedIn data portfolio  
💬 Enhances interview discussions with hospital-based use cases  
🚀 Prepares for roles in data analytics, healthcare BI, and reporting  
📊 Sets a foundation for dashboard building and automation

---
 
## <span id="conclusion">✅ Conclusion</span>

This SQL project gave me a strong foundation in healthcare data analytics.  
By querying a hospital dataset with PostgreSQL, I delivered actionable insights around **patient care**, **resource management**, and **cost control**.  
It helped transform structured data into real-world decisions and operational improvements — key to success in any data-driven healthcare environment.

---

## <span id="contact">📬 Connect with Me</span>  

<!-- Typing Animation / 🤝 Connect with me -->
[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=0DAD8D&lines=Let’s+connect+and+collaborate+on+meaningful+projects!;Click+the+buttons+below+to+connect+with+me+directly!)](https://git.io/typing-svg)

<div align="center">
<!-- 💼 LinkedIn -->
<a href="https://www.linkedin.com/in/rajeevtiwari8055"><img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="LinkedIn" width="30" height="30"/></a>
<!-- 📮 Gmail -->
<a href="mailto:rajeevtiwari8055@gmail.com" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/732/732200.png" alt="Email" width="35" height="35"></a>
<!-- ✖️ X -->
<a href="https://x.com/rajeevtiwariRT" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/5969/5969020.png" alt="X" width="35" height="35"></a>  
<!-- 🆔 GitHub -->
<a href="https://github.com/rajeevtiwari8055" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/733/733553.png" alt="GitHub" width="35" height="35"></a>
<!-- 🌐 Website -->
<a href="https://rajeevtiwari8055.github.io/" target="_blank"><img src="https://cdn-icons-png.flaticon.com/512/841/841364.png" alt="Website" width="35" height="35"></a>
</div>

<!-- Typing Animation / 🤝 Thanks for Visiting! -->
[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=8A2BE2&lines=🤝Thank+you+for+visiting+my+profile!)](https://git.io/typing-svg)

<!-- ⭐💫 Shower stars if you like my repos -->
<div align="center">
<img src="https://media.giphy.com/media/ObNTw8Uzwy6KQ/giphy.gif" width="30">
<a href="https://github.com/rajeevtiwari8055/rajeevtiwari8055" alt="GitHub Stars" title="Star my repositories">
<img src="https://img.shields.io/badge/Shower_stars_if_you_like_my_repositories-15k?style=for-the-badge&color=f9c513&logo=github&logoColor=black"/>
</a>
</div> 

---

## <span id="project-visual">📸 Project Preview</span>

🏥 **Hospital Data SQL Analysis Project**  
(*Visual: Hospital records database, SQL queries, patient and expense charts, healthcare insights*)

![Hospital Data Analysis Project](Hospital%20Data%20Analysis%20Project.jpg)

---

