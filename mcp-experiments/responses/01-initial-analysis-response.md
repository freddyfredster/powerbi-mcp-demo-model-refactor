I'll check what models are currently available in the workspace by reading the model configuration files. 

Read [](file:///c%3A/Users/FrederickAmougou/Projects/powerbi-mcp-demo-model-refactor/pbip-baseline/AI-Powered%20Model%20Refactor%20%E2%80%93%20Sales%20Analytics.SemanticModel/definition/database.tmdl)

Read [](file:///c%3A/Users/FrederickAmougou/Projects/powerbi-mcp-demo-model-refactor/pbip-baseline)

**Available models:**

Currently, there is **1 semantic model** in this workspace:

1. **AI-Powered Model Refactor – Sales Analytics** (`.pbip` project)
   - **Semantic Model folder:** `AI-Powered Model Refactor – Sales Analytics.SemanticModel/`
   - **Tables:** `SalesRaw` (recently normalized with safe type conversions)
   - **Source:** Excel file (`messy_sales_raw.xlsx`)
   - **Mode:** Import
   - **Compatibility level:** 1567 (Power BI V3)
   - **Culture:** en-US

The workspace structure includes:
- `.pbip` — Power BI Project file (root)
- `.SemanticModel/` — Semantic model definition (TMDL files)
- `.Report/` — Report definition

This is a single-table model currently. The next step would be to restructure it into a star schema (Fact + Dimensions) as recommended in the earlier detailed inspection.