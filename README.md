# 💳 Credit Card Statement Automation & Strategic Analysis with AI (n8n + Gemini)

> ⚙️ Automate ➡️ Analyze ➡️ Optimize — A Complete AI-Powered Finance Intelligence System

---

## 📌 Project Overview
This project automates the process of analyzing **employee credit card statements** and generates a strategic **optimization report** for finance teams using:

- 🔁 **n8n Workflows** (no-code/low-code automation)
- 🧠 **Google Gemini AI** (market research + data extraction)
- 📄 **Google Docs** (executive-ready report)
- 📊 **Google Sheets** (transactional summaries)

### 🎯 Why This Use Case Matters
Managing credit card usage across employees is often **manual, error-prone, and non-strategic**. This solution provides:
- 🔍 **Clear insights** into employee spending behavior
- 💰 **Optimized card usage** by matching categories with best-fit cards
- 🚩 **Alerts on risks**, misuse, or late fee trends
- 📈 **Estimated savings** in fees and rewards (₹4–5 lakhs/year for medium orgs)

---

## 🔍 Use Case Importance for Stakeholders
This project answers a key business question:
> "How can we control costs, improve compliance, and gain insight from employee credit card usage — without adding more manual work?"

Benefits for stakeholders:
- CFOs get clear, timely reports on spend behavior
- Finance teams reduce errors and maximize card benefits
- Founders and department heads get visibility into cost leaks

---

## 🧠 Workflow Summary

### 🔹 Flow 1 – Market Strategy Research (AI Agent)
**Purpose**: Provide real-time credit card usage strategy based on banks, spend categories, and current market offers.

**Prompt Used**:
```
Company: {{$json["company"]}}
Time Period: {{$json["time_period"]}}
Bank List: {{$json["banks"].join(", ")}}
Spend Categories: {{$json["categories"].join(", ")}}
Objectives: {{$json["objectives"].join(", ")}}

Please provide the following insights:
1. Best practices in India (2024–25) for using business credit cards
2. Reward programs or card types from above banks
3. Pitfalls in employee usage & how to avoid them
4. Public card offers companies should leverage

Structure your response in:
- 🔹 Industry Trends
- 🔹 Category-wise Card Optimization Tips
- 🔹 Card Offer Highlights (with Bank names)
- 🔹 Behavior Recommendations
- 🔹 Final Summary for CFO
```

### 🔹 Flow 2 – PDF Statement Extraction
**Purpose**: Extract credit card usage details from uploaded bank statements (e.g., Aarna Sood – Axis Bank).

**Steps**:
- Read file from disk (batch processing)
- Extract metadata and transaction summary
- Output JSON per employee/card

### 🔹 Flow 3 – Strategic Report Generation
**Purpose**: Merge Flow 1 + Flow 2 → Generate a CFO-ready strategy document

**Combined JSON Structure**:
```json
{
  "industry_insights": { ... },
  "employee_summaries": [
    {
      "card_name": "ICICI Coral",
      "total_spend_inr": 60000,
      "late_fee_inr": 500,
      "reward_points": 850,
      ...
    }
  ]
}
```

---

## 📂 Files Included
| File | Description |
|------|-------------|
| 📸 `workflow.png` | Visual of full automation pipeline in n8n |
| 📘 `Project_Guide.pdf` | Step-by-step build tutorial (beginner friendly) |
| 📄 `Final_Report.pdf` | Generated strategic report for CFO (AI-generated) |
| 🧾 `Sample_Statement.pdf` | Real bank credit card statement used as input |
| 📊 `Slides_PPT.pdf` | Presentation deck with storytelling & project explanation |

---

## 🔧 Technologies Used

| Tool | Purpose |
|------|---------|
| `n8n` | Workflow automation platform |
| `Google Gemini` | AI for PDF parsing + research prompts |
| `Google Docs API` | Report generation |
| `Google Sheets` | Store structured output data |

---

## 📸 Sample Visuals (Add these manually)

- ![Workflow Image](https://github.com/SachinSavkare/Credit-Card-Statement-Automation-Strategic-Analysis-with-AI-n8n-Gemini-/blob/main/N8N%20workflow.JPG)
- ![Sample Output Sheet](./transactions-sheet.png)
- ![Strategic Report Screenshot](./report-preview.png)

---

## 📈 Sample JSON Output (Flow 3 AI Input)
```json
{
  "industry_insights": {
    "final_summary": "...",
    "behavior_recommendations": "...",
    "industry_trends": "...",
    "category_optimization": {
      "Dining": "...",
      "Travel": "...",
      "Office Supplies": "..."
    },
    "card_offer_highlights": "..."
  },
  "employee_summaries": [
    {
      "card_name": "ICICI Bank Sapphiro Credit Card",
      "total_spend_inr": 75000,
      "payment_received_inr": 70000,
      "late_fee_inr": 0,
      "annual_fee_inr": 2500,
      "reward_points": 4200,
      "credit_limit_inr": 100000,
      "available_credit_inr": 25000,
      "minimum_due_inr": 5000,
      "due_date": "25-Nov-2024",
      "transactions": [
        { "date": "20-10-2024", "merchant": "Croma", "amount_inr": 35000 }
      ]
    }
  ]
}
```

---

## 📊 Business Impact Summary
| Metric | Before | After |
|--------|--------|-------|
| Late Fees | ₹9,500/year | ₹1,000/year |
| Unused Rewards | ₹18,000 | < ₹3,000 |
| Card Misuse Cases | 7 | 1 |
| Employee Awareness | Low | High |

**✔️ Business Benefits:**
- Annual savings up to ₹4–5 lakhs
- Credit policy compliance improvement
- Better decision-making via AI

---

## 🚀 How to Run This Project
1. Import workflows into n8n
2. Add API credentials for Gemini & Google Workspace
3. Upload sample PDFs to your file system
4. Trigger automation → View Sheets + Docs output

📘 Refer to the [Project Guide](https://github.com/SachinSavkare/Credit-Card-Statement-Automation-Strategic-Analysis-with-AI-n8n-Gemini-/blob/main/Project%20Guide.pdf) for full setup.

---

## 🧑‍💼 Ideal For:
- Finance teams
- Startups/SMBs managing employee cards
- Business analysts automating reporting
- AI + Automation portfolios

---

## 🤝 Credits
Built by **Sachin Savkare** 💡
> *“Turning manual finance operations into intelligent automation.”*

---

## 🔗 Report & Resource Links
- 📄 [Final Report PDF](./Final_Report.pdf)
- 📘 [Project Guide](https://github.com/SachinSavkare/Credit-Card-Statement-Automation-Strategic-Analysis-with-AI-n8n-Gemini-/blob/main/Project%20Guide.pdf)
- 📊 [Presentation Slides](https://github.com/SachinSavkare/Credit-Card-Statement-Automation-Strategic-Analysis-with-AI-n8n-Gemini-/blob/main/Presentation.pptx)
- 📸 [Workflow Image](https://github.com/SachinSavkare/Credit-Card-Statement-Automation-Strategic-Analysis-with-AI-n8n-Gemini-/blob/main/N8N%20workflow.JPG)
- 🧾 [Sample Credit Card Statement](https://github.com/SachinSavkare/Credit-Card-Statement-Automation-Strategic-Analysis-with-AI-n8n-Gemini-/blob/main/Aarna_Sood_AxisBank_Dec2024.pdf)

---

## ⭐ Like this Project?
Give it a ⭐ on GitHub and connect on [LinkedIn](https://www.linkedin.com/in/sachinsavkare)!

---
