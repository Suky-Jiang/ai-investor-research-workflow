# AI-Assisted Investor Research Workflow

A no-code AI-assisted workflow that processes simulated investor research requests, ranks relevant research from a synthetic content library, drafts client responses, and captures reusable client preferences.

This project was built as a portfolio demonstration of how AI and workflow automation can support research and account-management teams.

---

## 🚀 Live Demo

### Try the Workflow
[Submit a simulated investor research request via Tally](https://tally.so/r/obPlJX)

### View the Research Library
[View the synthetic research database](https://docs.google.com/spreadsheets/d/13W-tKoZgVYN7_ETcR0ofaqm_aM6JVAefTNOi2UveD24/edit?usp=sharing)

> All research records and client information used in this project are synthetic.

## ⚙️ View the Workflow
[View the complete Make automation scenario](https://eu1.make.com/public/shared-scenario/WdV0fTydoyP/ai-research-request-triage-content-rec)

### View Live Results
[View the results spreadsheet](https://docs.google.com/spreadsheets/d/13W-tKoZgVYN7_ETcR0ofaqm_aM6JVAefTNOi2UveD24/edit?usp=sharing)

---
## 💡 The Problem

Research and account-management teams may receive frequent client requests asking for information on specific companies, markets, geographies, and business topics.

Manually reviewing a research library, identifying the most relevant content, drafting a response, and recording client interests can involve repetitive administrative work.

I built this workflow to explore how AI can assist with those tasks while keeping human review in the process.

---

## 🔄 How the Workflow Works

```text
Tally
Client submits research request
        ↓
Google Sheets
Request is logged
        ↓
Google Sheets
Research library is searched by company
        ↓
Make Text Aggregator
Matching research records are combined
        ↓
AI
Relevant research is ranked
+ client response is drafted
        ↓
Google Sheets
Request is updated
        ↓
Human Review
Account manager reviews the recommendation
        ↓
AI
Client preferences are extracted
        ↓
JSON Parser
Preferences are converted into structured data
        ↓
Google Sheets
Client preferences are stored
```

---

## 📝 Example Request

**Client / Fund:** Atlas Capital

**Company:** Nike

**Geography:** China

**Priority:** High

**Research Question:**

We're reviewing Nike and want to understand whether inventory pressure is easing, how Chinese consumer demand is developing, and what wholesale partners are seeing.

---

## 🔎 Example Research Recommendation

The synthetic research library contains several Nike-related research records.

For this request, the AI may identify:

| Rank | Research ID | Topic | Geography | Relevance |
|------|-------------|-------|-----------|-----------|
| 1 | R002 | Consumer Demand | China | Directly addresses Chinese consumer demand and local competitive conditions |
| 2 | R001 | Inventory | North America | Provides context on inventory normalisation and retailer stock levels |
| 3 | R004 | Wholesale | North America | Provides insight into wholesale partner behaviour, orders and markdown risk |

The AI is instructed to recommend only research records that exist in the supplied library.

If no sufficiently relevant research exists, it should say so instead of inventing a research item.

---

## 💬 Example AI-Assisted Response

Thank you for the brief. I identified several Nike-focused research items that may be relevant to your review.

The China consumer-demand interview appears most directly aligned with your geographic focus, while the inventory and wholesale discussions provide additional context on channel conditions and stock levels.

These recommendations are intended for human review before being shared with a client.

---

## 👤 Client Preference Extraction

The workflow also converts each research request into reusable client-interest data.

For example:

```json
{
  "companies_of_interest": ["Nike"],
  "geography_interest": ["China"],
  "topics_of_interest": [
    "Inventory",
    "Consumer Demand",
    "Wholesale"
  ],
  "research_style": [
    "Channel Checks",
    "Operating Trends"
  ]
}
```

This information is stored separately from the original request so that client interests can be analysed over time.

---

## 🛠 Technology Stack

**Tally**
Used for the investor research request form.

**Make**
Used to orchestrate the complete automation workflow.

**Google Sheets**
Used as the synthetic research library, client-request log, and client-preference database.

**Make Text Aggregator**
Combines multiple matching research records into one structured context block before the AI step.

**AI / LLM Module**
Used to rank research relevance, draft client responses, and extract structured client preferences.

**JSON Parser**
Converts AI-generated preference data into structured fields that can be stored in Google Sheets.

---

## 🛡 AI Safeguards

The workflow includes several safeguards:

- AI can only recommend research contained in the supplied synthetic research library.
- Research IDs must match existing database records.
- The AI is instructed not to invent experts, interviews, research items, quotes, or unsupported findings.
- If no suitable research exists, the AI should explicitly state that no direct match was found.
- The system does not provide investment advice.
- AI-generated responses are marked Ready for human review before client communication.
- Request and AI-output data are logged for traceability.

---

## 👥 Client Preference System

The project separates individual requests from longer-term client preference data.

### Client Request

Stores what the client asked for at a specific point in time.

Example:

```
Company: Nike
Geography: China
Question: Inventory pressure, consumer demand and wholesale conditions
Priority: High
```

### Client Preference

Stores reusable information extracted from that request.

Example:

```
Companies of Interest: Nike
Geography Interest: China
Topics of Interest: Inventory, Consumer Demand, Wholesale
Research Style: Channel Checks, Operating Trends
```

This structure could later support more personalised and proactive research recommendations.

---

## ✅ What This Project Demonstrates

- No-code workflow automation
- AI-assisted research triage
- Prompt design
- Structured AI output
- Client preference extraction
- Research relevance ranking
- Human-in-the-loop AI design
- Google Sheets database design
- Account-management workflow thinking

---

## 🔮 Future Improvements

Potential future versions could include:

- Semantic search instead of company-only filtering
- An evolving client profile combining multiple historical requests
- Proactive alerts when newly added research matches a client's interests
- Research relevance confidence scores
- Automated duplicate-preference detection
- A dashboard showing client research patterns
- Email delivery after human approval

---

## ⚠️ Disclaimer

All research records, client names, requests, and example outputs used in this project are synthetic and created solely for portfolio demonstration purposes.

This project does not contain proprietary investment research or real client data.

This project is not affiliated with Third Bridge or any other investment research provider.

---

## About the Project

This project was created to explore how AI can reduce repetitive administrative work while supporting high-touch client service.

The objective is not to replace human account managers or research professionals, but to demonstrate how AI can assist with research discovery, response preparation, and client-preference tracking while maintaining human oversight.
