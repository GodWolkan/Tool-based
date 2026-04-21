📖 README.md

markdown
# 🏦 Online Banking API Testing Project

## 📌 Course Details
- **Course Code:** CSET481 – Software Testing  
- **Domain:** Online Banking System  
- **University:** Bennett University, Greater Noida  
- **Faculty:** Dr. Mohd Anas  
- **Tools Used:** Postman, Newman CLI  

---

## 📖 Project Overview
This project focuses on **functional API testing** of an Online Banking System using Postman and Newman CLI.  

The system simulates real-world banking operations such as:
- User authentication  
- Account management  
- Fund transfer  
- Transaction history  
- Beneficiary management  

🔗 **Mock API Used:** https://reqres.in/api  

---

## 🎯 Objectives
- Validate core banking APIs using structured test cases  
- Apply testing techniques:
  - Boundary Value Analysis (BVA)  
  - Equivalence Partitioning (EP)  
  - Decision Table Testing (DT)  
  - State Transition Testing (ST)  
- Automate API testing using Newman CLI  
- Generate HTML reports for execution results  

---

## 🧪 Test Scenarios Covered

### 🔐 Authentication
- Valid login  
- Invalid password  
- Empty credentials  
- SQL injection attempt  

### 💳 Fund Transfer
- Valid transfer  
- Boundary values (0, 1, max, max+1, negative)  
- Missing fields  
- Self-transfer  

### 👤 Account Management
- Get account details  
- Update account  
- Delete account  
- Unauthorized access  

### 📊 Transaction History
- Pagination  
- Date filtering  
- Out-of-range queries  

---

## 🛠️ Tools & Technologies
- **Postman** – API testing  
- **Newman CLI** – Automated execution  
- **JavaScript (Chai.js)** – Test scripting  
- **htmlextra** – HTML report generation  

---

## ⚙️ Setup Instructions

### 1️⃣ Install Postman
Download: https://www.postman.com/downloads/

### 2️⃣ Import Collection
- Open Postman  
- Click **Import**  
- Upload: `OnlineBanking_Postman_Collection.json`  

### 3️⃣ Run in Postman
- Use **Collection Runner**  
- Execute all test cases  

### 4️⃣ Install Newman
```bash
npm install -g newman newman-reporter-htmlextra
````

### 5️⃣ Run via Newman

```bash
newman run OnlineBanking_Postman_Collection.json \
--reporters cli,htmlextra \
--reporter-htmlextra-export ./newman_report.html
```

---

## 📊 Test Execution Summary

| Module              | Total | Passed | Failed |
| ------------------- | ----- | ------ | ------ |
| Authentication      | 4     | 4      | 0      |
| Account Management  | 4     | 4      | 0      |
| Fund Transfer       | 3     | 3      | 0      |
| Transaction History | 3     | 3      | 0      |
| **Total**           | 14    | 14     | 0      |

---

## 🐞 Defects Identified

| ID      | Description                         | Severity |
| ------- | ----------------------------------- | -------- |
| DEF-001 | Self-transfer not blocked           | High     |
| DEF-002 | Invalid password returns 200        | Medium   |
| DEF-003 | Out-of-range pagination returns 200 | Low      |

---

## ⚖️ Strengths

* Easy API testing with GUI
* Supports JavaScript-based assertions
* Fast execution using Newman
* HTML reporting support

---

## ⚠️ Limitations

* No UI testing
* Cannot simulate concurrent users
* Limited security testing

---

## 🔄 Postman vs JMeter

| Feature     | Postman            | JMeter       |
| ----------- | ------------------ | ------------ |
| Purpose     | Functional Testing | Load Testing |
| UI          | Easy               | Complex      |
| Concurrency | ❌                  | ✅            |
| Scripting   | JavaScript         | Java/Groovy  |

---

## 🚀 Future Improvements

* Integrate JMeter for load testing
* Add OWASP ZAP for security testing
* Use CSV-based data-driven testing
* Connect to real backend APIs

---

## 🎤 Viva Preparation

Be ready to:

* Run a test case (TC-AUTH-01)
* Modify test inputs (e.g., transfer amount)
* Explain failed cases (self-transfer issue)
* Explain testing techniques (BVA, EP, DT, ST)

---

## 📎 Files Included

* `OnlineBanking_Postman_Collection.json`
* `newman_report.html`
* `README.md`

---

## 👩‍💻 Author

**Priyanshu Bisht**
B.Tech CSE (Data Science)
Bennett University



