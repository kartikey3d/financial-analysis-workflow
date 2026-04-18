# 📊 Financial Analysis & Dashboard Workflow

An n8n automation workflow that reads financial PDF reports, extracts key metrics using AI, and generates a fully interactive HTML dashboard — all in one click.

---
dashboard-preview.png
<img width="1920" height="894" alt="Screenshot (279)" src="https://github.com/user-attachments/assets/fc2522a5-2dcf-43f7-8a58-442c6122a9b8" />
---

## 🚀 What It Does

1. **Upload** a financial report PDF via a simple web form
2. **Gemini 2.5 Flash** reads and extracts all text from the document
3. **GPT-4.1-mini** pulls out structured financial metrics (Revenue, Gross Profit, Net Profit)
4. **Auto-generates** a beautiful interactive HTML dashboard with charts and comparisons
5. **Downloads** the dashboard as an HTML file — ready to share or present

---

## 📸 Output

The generated dashboard includes:
- KPI summary cards (Revenue, Gross Profit, Net Profit)
- Bar charts, Radar charts, Doughnut charts (powered by Chart.js)
- Current vs Prior period comparisons
- Multi-company side-by-side comparison view
- Animated counters and smooth transitions

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| [n8n](https://n8n.io) | Workflow automation |
| Google Gemini 2.5 Flash | PDF document reading & text extraction |
| GPT-4.1-mini (OpenAI) | Structured data extraction |
| Chart.js | Interactive dashboard charts |
| HTML / CSS / JavaScript | Dashboard frontend |

---

## ⚙️ How to Use

### Prerequisites
- A running [n8n instance](https://docs.n8n.io/hosting/) (self-hosted or cloud)
- An **OpenAI API key**
- A **Google Gemini API key**

### Setup Steps

1. **Clone or download** this repo
2. **Import the workflow** into n8n:
   - Open n8n → Click the `⋯` menu (top right) → `Import from file`
   - Select `Financial_Analysis_and_Dashboard.json`
3. **Add your credentials** in n8n:
   - Go to the `OpenAI Chat Model` node → connect your OpenAI API key
   - Go to the `Analyze document` node → connect your Google Gemini API key
4. **Activate** the workflow
5. **Open the form URL** (shown in the `On form submission` node)
6. **Upload a financial PDF** and hit submit
7. Your dashboard HTML file will be ready to download!

---

## 📂 Repository Structure

```
financial-analysis-workflow/
├── Financial_Analysis_and_Dashboard.json   # n8n workflow file
└── README.md
```

---

## 📋 Extracted Metrics

The workflow automatically extracts the following from your financial reports:

- Cumulative Quarter **Revenue** — Current & Prior Period
- Cumulative Quarter **Gross Profit** — Current & Prior Period
- Cumulative Quarter **Net Profit** — Current & Prior Period
- **Company Name**

---

## ⚠️ Notes

- Works best with structured financial reports (quarterly/annual reports, P&L statements)
- Supports multiple companies — upload multiple PDFs and the dashboard will compare them
- Maximum 6 companies supported in one run
- All values are expected in **RM (Malaysian Ringgit)** thousands — modify the JS code node if your currency differs

---

## 📄 License

MIT — feel free to use, modify, and share.
