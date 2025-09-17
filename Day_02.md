# 📅 Day 02 – 📚 Data Literacy, 🗃️ SQL Practice &  🌐 Digital Transformation 
## 🧠 What I Learned

### 🔹 Data Literacy
- 🔍 **What is Data?** → Raw facts that can be processed into information.  
- 🪜 **DIKW Pyramid** → Data → 📑 Information → 📖 Knowledge → 🧙 Wisdom  
- 🗂️ **Data Types**:
  - 🔢 Quantitative (Categorical): Nominal, Ordinal  
  - 📏 Qualitative (Numerical): Discrete, Continuous  
- 💾 **Data Formats**:
  - 📊 Structured (CSV, Databases)  
  - 📝 Semi-structured (JSON, XML)  
  - 🎥 Unstructured (Images, Text, Audio, Video)  
- 📈 **Data Analysis Types**:
  - 🧾 Descriptive  
  - 🔍 Exploratory  
  - 🗣️ Explanatory  
  - 🤖 Predictive  
  - 🎯 Prescriptive  
  - 🧪 Experimental  

---

### 🔹 SQL Case Study: Salaries Dataset  
**Database:** `:memory:` (💼 Salaries sample table)  

```sql
-- 📊 Average BasePay
SELECT AVG(basepay) FROM Salaries;

-- 💸 Highest OvertimePay
SELECT MAX(overtimepay) FROM Salaries;

-- 👔 Job title of JOSEPH DRISCOLL
SELECT jobtitle FROM Salaries WHERE employeename == 'JOSEPH DRISCOLL';

-- 🤑 Total pay (with benefits) of JOSEPH DRISCOLL
SELECT totalpaybenefits FROM Salaries WHERE employeename == 'JOSEPH DRISCOLL';

-- 👑 Highest paid employee
SELECT MAX(totalpaybenefits), employeename FROM Salaries;

-- 🥲 Lowest paid employee
SELECT MIN(totalpaybenefits), employeename FROM Salaries;

-- 📆 Avg. BasePay per year (2011–2014)
SELECT AVG(basepay), year FROM Salaries GROUP BY year;

-- 🔢 Number of unique job titles
SELECT COUNT(DISTINCT(jobtitle)) FROM Salaries;

-- 🔝 Top 5 most common jobs
SELECT jobtitle, COUNT(jobtitle) as JobCount 
FROM Salaries 
GROUP BY jobtitle 
ORDER BY JobCount DESC 
LIMIT 5;
```



# 🚀 Day 02 Completed – Tomorrow I’ll dive deeper into **Data Tools & Python practice** 🙌✨

