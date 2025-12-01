# Power BI Model Refactor with MCP + GitHub Copilot  
Using Natural Language to Clean, Optimise, and Govern a Power BI Semantic Model

This demo shows how to use the **Power BI Modeling MCP Server** with **GitHub Copilot** inside VS Code to:
- Inspect and refactor a Power BI semantic model using natural language  
- Apply best-practice modelling patterns in seconds  
- Optimise DAX with performance metrics  
- Make changes safely using PBIP + GitHub version control  

---

## 🚀 What This Demo Covers

### 1. Natural Language Model Refactoring  
- Renaming measures  
- Creating measure folders  
- Hiding technical columns  
- Fixing relationships  
- Enforcing naming conventions  
- Building dimensions from a flat table

### 2. Semantic Model Best Practice Sweep  
- Standardising date formats  
- Marking date tables  
- Hiding surrogate keys  
- Identifying ambiguous relationships  
- Preparing for governance

### 3. DAX Performance Tuning  
- Running DAX queries with real execution metrics  
- Detecting slow patterns (iterators, auto-exist, cardinality issues)  
- Generating improved versions of the measure  

---

## 🧰 Tools Used
- **Power BI Desktop** (Modern metadata ON)  
- **PBIP Project Format**  
- **VS Code**  
- **GitHub Copilot + MCP Modeling Server**  
- **DAX Query Runner (via MCP tools)**  

---

## 📂 Repo Structure

'''
powerbi-mcp-demo-model-refactor/
│
├── README.md
│
├── pbip-model/
│ └── (PBIP model files)
│
├── results/
│ ├── before-after-diff/
│ ├── model-diagram-before.png
│ ├── model-diagram-after.png
│ └── performance-metrics.json
│
├── prompts/
│ ├── 01-cleanup.txt
│ ├── 02-star-schema.txt
│ ├── 03-best-practice-sweep.txt
│ └── 04-dax-performance.txt
│
└── docs/
├── walkthrough.md
├── mcp-architecture.png
└── what-changed.md
,,,


---

## 📝 How to Run This Yourself

1. Install:  
   - GitHub Copilot  
   - GitHub Copilot Chat  
   - Power BI Modeling MCP Server VS Code extension  

2. In Power BI Desktop:  
   - Enable PBIP project storage  
   - Save your model as a PBIP  

3. Open the PBIP folder in VS Code  
4. Open the Copilot Chat sidebar  
5. Start sending natural-language commands  

---

## 📸 Before/After Preview

**Before:** unstructured model, messy columns, inconsistent naming  
**After:** clean star schema, standardised measures, optimised DAX  

Screenshots located in `/results/before-after-diff/`.

---

## ✍️ Credits  
Created by Freddy — sharing my process for anyone who wants to build cleaner, scalable Power BI models using modern AI tooling.
