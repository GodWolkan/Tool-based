📌 Course Details
Course Code: CSET481 – Software Testing
Domain: Online Banking System
Tool Used: Postman + Newman CLI
University: Bennett University, Greater Noida
Faculty: Dr. Mohd Anas
📖 Project Overview
This project focuses on functional API testing of an Online Banking System using Postman and Newman CLI.

The system simulates real-world banking operations such as:

User authentication
Account management
Fund transfer
Transaction history
Beneficiary management
Testing was performed on a mock API server:

https://reqres.in/api
🎯 Objectives
Validate core banking APIs using structured test cases

Apply testing techniques like:

Boundary Value Analysis (BVA)
Equivalence Partitioning (EP)
Decision Table Testing (DT)
State Transition Testing (ST)
Automate API testing using Newman CLI

Generate HTML reports for execution results

🧪 Test Scenarios Covered
🔐 Authentication
Valid login
Invalid password
Empty credentials
SQL injection attempt
💳 Fund Transfer
Valid transfer
Boundary values (0, 1, max, max+1, negative)
Missing fields
Self-transfer
👤 Account Management
Get account details
Update account
Delete account
Unauthorized access
📊 Transaction History
Pagination
Date filtering
Out-of-range queries
🛠️ Tools & Technologies
Postman – API testing
Newman CLI – automated test execution
JavaScript (Chai.js) – test scripting
HTML Reporter (htmlextra) – report generation
⚙️ Setup Instructions
1️⃣ Install Postman
Download from: https://www.postman.com/downloads/

2️⃣ Import Collection
Open Postman
Click Import
Upload:
OnlineBanking_Postman_Collection.json
3️⃣ Run Collection in Postman
Click Collection Runner
Execute all test cases
4️⃣ Install Newman CLI
npm install -g newman newman-reporter-htmlextra
5️⃣ Run Tests via Newman
newman run OnlineBanking_Postman_Collection.json \
--reporters cli,htmlextra \
--reporter-htmlextra-export ./newman_report.html
📊 Test Execution Summary
Module	Total	Passed	Failed
Authentication	4	4	0
Account Management	4	4	0
Fund Transfer	3	3	0
Transaction History	3	3	0
Total	14	14	0
🐞 Defects Identified
Defect ID	Description	Severity
DEF-001	Self-transfer not blocked	High
DEF-002	Invalid password still returns 200	Medium
DEF-003	Out-of-range pagination returns 200	Low
⚖️ Strengths of Postman
Easy API testing with GUI
Supports automated scripting using JavaScript
Token handling using variables
Fast execution using Newman CLI
HTML reporting support
⚠️ Limitations
Cannot test UI (no frontend testing)
Cannot simulate concurrent users
Limited security testing capabilities
🔄 Comparison: Postman vs JMeter
Feature	Postman	JMeter
Purpose	Functional testing	Load testing
UI	Easy	Complex
Concurrency	❌	✅
Scripting	JS	Java/Groovy
🚀 Future Improvements
Integrate JMeter for load testing
Add OWASP ZAP for security testing
Use CSV data-driven testing with Newman
Connect to real backend instead of mock API
🎤 Viva Preparation
Be ready to:
Run a test case live (TC-AUTH-01)
Modify a test case (change amount values)
Explain a failed case (self-transfer issue)
Explain testing techniques (BVA, EP, DT, ST)
📎 Files Included
OnlineBanking_Postman_Collection.json
newman_report.html
README.md
👩‍💻 Author
Priyanshu Bisht B.Tech CSE (Data Science) Bennett University
