
# Big Data Pipeline for U.S. Political Donation Insights Using Apache Spark

This project explores individual contributions to U.S. Federal Committees (Presidential, Senate, and House) during the period of **June 20, 2024 – July 23, 2024**, using **Apache Spark** on AWS. The goal is to extract insights from millions of records to understand financial trends, donor geography, and campaign influence patterns.

---

## 📦 Dataset
- **Source:** [Federal Election Commission (FEC)](https://www.fec.gov/data/browse-data/?tab=bulk-data)
- **Files Used:**
  - `itcont_2024_20240620_20240709.txt`
  - `itcont_2024_20240710_20240723.txt`
  - `indiv_header_file.csv`

Each file is pipe-delimited (`|`) and includes metadata like contributor name, amount, state, employer, and committee ID.

---

## ⚙️ Tools & Environment
- **Apache Spark** on **AWS EC2 (t2.large)**  
- **Python** (PySpark, csvkit)
- **Pandas**, **Matplotlib** for data previewing
- **Jupyter Notebook**
- **Data Size:** ~3.8 million rows

---

## 🧪 Data Engineering Workflow
1. Uploaded zipped files to EC2 and extracted contents.
2. Converted raw text files into `.csv` using `csvkit`.
3. Validated files and merged them into `final.csv`.
4. Processed data using:
   - **RDD API** for basic aggregations.
   - **DataFrame API** for schema exploration and advanced filtering.
   - **SQLContext** for SQL-based queries.

---

## 🔍 Analysis Highlights

### 🔹 RDD-Based Insights
- **Top States by Contribution Count:**  
  - California, Texas, Florida, and New York lead in volume.

- **Top States by Total Amount:**  
  - CA: \$64.84B, TX: \$55.44B, IL: \$34.14B.

### 🔹 DataFrame API
- **Highest Single Contribution:**  
  - Timothy Mellon: \$50M
- **Top Contributor by Total:**  
  - Timothy Mellon: \$55M

### 🔹 SQL Queries
- Found committees with highest daily contributions.
- Identified major contributors and their occupations.

---

## 📊 Key Insights
- **Wealth concentration:** A few high-net-worth individuals contribute disproportionately.
- **Regional hubs:** States like CA, TX, IL, and NY dominate donations.
- **Campaign implications:** Fundraising strategies heavily depend on donor geography and repeat contributors.

---

## 🧠 Learnings
- Mastered data parsing, cleaning, and transformation in distributed environments.
- Gained experience in SQLContext, RDDs, and DataFrames in Spark.
- Built analytical workflows from data ingestion to insights.

---

## 📁 Files Included
- `Federal_Committee_Contribution.ipynb`: Full Jupyter Notebook
- `Federal_Committee_Contribution_1748898760.pdf`: PDF version
- `final.csv`: Combined and cleaned dataset (not included in repo due to size)

---

## ✅ Conclusion

This project demonstrates the power of big data tools like Apache Spark in unraveling complex patterns hidden within millions of political contribution records. By leveraging distributed processing, structured queries, and analytical modeling, we uncovered how a small group of wealthy donors and key states disproportionately shape the U.S. political funding landscape. These insights highlight not only campaign strategies but also broader questions of equity and influence in modern democracy. The project serves as a practical example of using Spark for real-world data engineering, statistical aggregation, and policy-relevant analysis.

---

## 👤 Author
**Anesh Thangaraj**  
Master’s Student in Business Analytics, George Washington University  
[LinkedIn](https://www.linkedin.com/in/anesh-t/) | [GitHub](https://github.com/anesh-t)
