# Power BI MCP Experiment — Refactoring a Messy Sales Model with Natural Language

This repo documents my early experiments using the **Power BI Modeling MCP Server** inside VS Code to refactor a Power BI model using natural-language prompts.

I used a deliberately messy Sales dataset, exported the file as PBIP, and then asked the MCP agent to analyse the model and suggest a cleaner schema. Some of the results were genuinely impressive… and some of them completely broke the PBIP project.

This repo is not a polished tutorial.  
It's closer to **experimental field notes** — what worked, what didn’t, and how the tooling behaves today.

---

## 🚀 What Worked

### **1. Model analysis**
My first prompt asked the agent to inspect the semantic model:

- List tables, columns, and data types  
- Identify messy fields  
- Suggest a star schema  
- Highlight potential dimension candidates  

This worked extremely well.  
The agent understood the model and gave solid recommendations.

Prompt + full response are included in:

mcp-experiments/prompts/01-initial-analysis.txt
mcp-experiments/responses/01-initial-analysis-response.md


---

## ⚠️ What Didn’t Work (Yet)

### **2. Structural model edits**
I then tried asking the agent to:

- Create dimension tables  
- Split out fact tables  
- Build relationships  
- Hide / rename columns  

The agent generated what looked like correct TMDL, but the structure did **not** load in Power BI Desktop. Some errors included:

- Unsupported properties  
- Invalid indentation  
- Broken table metadata  

This is preview tooling, so it’s expected.  
Still promising — but not ready for production models.

Prompt + full response included in:

mcp-experiments/prompts/02-refactor-attempt.txt
mcp-experiments/responses/02-refactor-attempt-response.md


---

## 📁 Repo Content Overview

```
powerbi-mcp-sales-experiments/
│
├── README.md
│
├── data/
│   └── raw/
│       └── messy_sales_raw.xlsx
│
├── pbip-baseline/
│   └── (clean PBIP export that opens successfully in Desktop)
│
└── mcp-experiments/
    ├── prompts/
    │   ├── 01-initial-analysis.txt
    │   └── 02-refactor-attempt.txt
    │
    └── responses/
        ├── 01-initial-analysis-response.md
        └── 02-refactor-attempt-response.md
```

## 📝 Lessons Learned

The analysis capabilities are already very strong.

The write capabilities (editing TMDL) are still unstable and may break PBIP files.

Git is essential — commit before every MCP operation.

For now, use MCP for review, documentation, and suggestions, not automated refactoring.

## 🔧 How to Try This Yourself

Clone the repo

Open the PBIP baseline in Power BI Desktop

Open the folder in VS Code

Enable Copilot Chat + install the Power BI Modeling MCP extension

Run the prompts in /mcp-experiments/prompts

Compare your results with the responses in /responses

## 💬 Share Your Findings

I’ve posted about this experiment on LinkedIn — the repo link is in the comments.

If you've tried the MCP server for Power BI:

Did it work for you?

Did anything break?

Any best practices?

I’m curious to see how others are using it and how fast this tooling improves.
