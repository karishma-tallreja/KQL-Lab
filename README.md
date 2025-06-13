# KQL Overview – Investigating with ELK 

## 🔍 Objective

- Understand and apply **Kibana Query Language (KQL)** for log analysis.
- Differentiate between **free-text** and **field-based** search methods.
- Learn to use **wildcards** and **logical operators** in KQL.
- Perform log filtering and incident-based investigations using KQL in Kibana.

---

## 🛠 Tools Used

- **Kibana** (via ELK Stack on TryHackMe)
- **ElasticSearch**
- **TryHackMe Platform (Investigating with ELK 101 room)**

---

## 📚 Skills Learned

- Basics of **KQL (Kibana Query Language)**.
- Effective **log searching and filtering** using:
  - Free-text queries.
  - Field-based queries with specific syntax.
- Application of **logical operators (AND, OR, NOT)** in queries.
- Usage of **wildcards** (`*`) for partial term searches.
- Real-world **SIEM investigation use cases** using VPN log data.
- Understanding how query precision affects **log hit counts**.
- Filtering based on field values like `Source_Country`, `UserName`, `Source_ip`.

---

## 🧠 What I Learned

- How to distinguish between **exact term matching** and **partial matching**.
- Importance of correct syntax (`FIELD : VALUE`) in field-based queries.
- That **KQL doesn’t tokenize words**, so `United` won’t match `United States` unless using wildcards.
- Efficient ways to exclude unwanted data using the `NOT` operator.
- Applying multiple conditions to extract meaningful logs for analysis.
- How to construct real-time investigative queries based on specific scenarios (e.g., terminated users, suspicious IPs).

---

## 🖼️ Screenshots

### 1. KQL Tab Selection in Kibana Interface
<img src="https://i.imgur.com/xI8yUga.png" alt="Disabling Lucene to use KQL" width="700"/>

### 2. Exploring field values in left panel (Source_Country)  
<img src="https://i.imgur.com/0Cz6QSa.png" alt="Source_Country Field View" width="700"/>

### 3. Free text search for 'United States'  
<img src="https://i.imgur.com/L8gr0Ac.png" alt="Search for United States" width="700"/>

### 4. Searching for partial term 'United' (No results)  
<img src="https://i.imgur.com/hBUQ7LY.png" alt="No result for 'United'" width="700"/>

### 5. Using wildcard 'United*'  
<img src="https://i.imgur.com/i3ExndQ.png" alt="Wildcard usage in KQL" width="700"/>

### 6. Logical operator OR – 'United States' OR 'England'  
<img src="https://i.imgur.com/7OubYwB.png" alt="Logical OR in KQL" width="700"/>

### 7. Logical operator AND – 'United States' AND 'Virginia'  
<img src="https://i.imgur.com/gPTCouc.png" alt="Logical AND in KQL" width="700"/>

### 8. Logical operator NOT – Excluding 'Florida'  
<img src="https://i.imgur.com/B4KPN3k.png" alt="Logical NOT in KQL" width="700"/>

### 9. Field-based search with IP and username  
<img src="https://i.imgur.com/DSF9gsU.png" alt="Field-based KQL query" width="700"/>

### 10. Query for Source_Country='United States' and User='James' or 'Albert'  
<img src="https://i.imgur.com/Osb8hQu.png" alt="Query for multiple users from US" width="700"/>

### 11. Query to find VPN activity of Johny Brown post-termination  
<img src="https://i.imgur.com/VO6cMEw.png" alt="Johny Brown VPN logs after termination" width="700"/>

---

## 📎 Reference

- [KQL Official Guide – Elastic Docs](https://www.elastic.co/guide/en/kibana/7.17/kuery-query.html)
