# AI-Assisted Investor Research Workflow

A no-code AI workflow for triaging simulated investor research requests, ranking relevant research, drafting client responses, and tracking client preferences using Tally, Make and Google Sheets.

## 🚀 Try the Project

👉 **[Try the Live Demo](https://tally.so/r/obPlJX)**

📊 **[View the Synthetic Research Library](https://docs.google.com/spreadsheets/d/13W-tKoZgVYN7_ETcR0ofaqm_aM6JVAefTNOi2UveD24/edit?usp=sharing)**

⚙️ **[View the Workflow Diagram](https://eu1.make.com/public/shared-scenario/WdV0fTydoyP/ai-research-request-triage-content-rec)**

📋 **[See Example Output](https://docs.google.com/spreadsheets/d/13W-tKoZgVYN7_ETcR0ofaqm_aM6JVAefTNOi2UveD24/edit?usp=sharing)**

## 🔄 How It Works
Tally → Make → Google Sheets → AI → Human Review

## 📝 Example Request

**Client / Fund:** Siyujiang

**Company:** Nike

**Geography:** China

**Research Question:**
> We're reviewing Nike and want to understand whether inventory pressure is easing, how Chinese consumer demand is developing, and what wholesale partners are seeing.

**Priority:** High

**Dealine:** 08/09/2026

**Email:** jiangsiyu32@gmail.com

## 🔎 Example AI Output
CLIENT NEED

Client seeks to understand whether Nike’s inventory pressure is easing, how Chinese consumer demand is developing, and what wholesale partners are seeing, specifically in China.

TOP RESEARCH

1.
Research ID: R002
Topic: Consumer Demand
Geography: China
Why relevant: Directly addresses demand trends in China, including consumer preferences, traffic recovery, and local brand competition.

2.
Research ID: R001
Topic: Inventory
Geography: North America
Why relevant: Provides insights on inventory normalization, discounting, and retailer ordering behavior that can inform cross-region inventory dynamics and potential parallels.

3.
Research ID: R003
Topic: Supply Chain
Geography: Global
Why relevant: Offers context on manufacturing lead times, sourcing, and freight conditions that can influence inventory pressure and wholesale readiness, even if not China-specific.

DIRECT MATCHES

R002
Topic: Consumer Demand
Geography: China
Why relevant: Directly addresses Chinese demand dynamics and consumer behavior relevant to Nike in China.

CONTEXTUAL RESEARCH

R001
Topic: Inventory
Geography: North America
Note: Discusses inventory normalization and discounting in North America. Not China-specific, but useful for cross-region inventory comparison and potential implications for wholesale behavior.

R003
Topic: Supply Chain
Geography: Global
Note: Provides global supply chain context (lead times, sourcing, freight) that can influence inventory pressure and wholesale readiness, but not China-specific.

SUGGESTED CLIENT RESPONSE

Thank you for the request. We’ve identified the most directly relevant item for your China-focused questions and a couple of contextual items to provide broader inventory and supply chain context.

- Direct relevance to China demand: R002 – Nike: China consumer demand trends, traffic recovery, local brand competition. This item best informs how Chinese demand is evolving and potential implications for inventory and wholesale discussions.
- Context for inventory pressure and wholesale dynamics (non-China-specific): 
  - R001 – Inventory: North America — insights on inventory normalization, discounting, and retailer ordering behavior.
  - R003 – Supply Chain: Global — context on manufacturing lead times and sourcing that can affect inventory levels and wholesale positioning.

If helpful, we can summarize key takeaways from R002 and map them to potential implications for Nike China inventory and wholesale conversations, while noting the limitations of cross-region inferences.

CLIENT INTEREST TAGS

China, Nike, inventory, demand, wholesale

## 👤 CRM / Client Preference System

In addition to answering individual research requests, the workflow also captures reusable client preference data.

This helps separate:

- **What the client asked today**
- **What the account manager has learned about the client over time**

### Example Preference Record

| Field | Example |
|---|---|
| Client / Fund | Atlas Capital |
| Requester Email | analyst@atlascapital-demo.com |
| Companies of Interest | Nike |
| Geography Interest | China |
| Topics of Interest | Inventory, Consumer Demand, Wholesale |
| Research Style | Channel Checks, Operating Trends |
| Priority | High |
| Last Request | 08 Sep 2026 |

The preference data is extracted by AI, converted into structured JSON, and then saved into Google Sheets as a lightweight CRM-style client profile.

### CRM Workflow

```text
Client Research Request
        ↓
AI Preference Extraction
        ↓
JSON Parser
        ↓
Structured Client Preferences
        ↓
Google Sheets Client Preference Database
