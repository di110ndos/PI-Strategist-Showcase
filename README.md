# PI Strategist

**AI-Powered Program Increment Planning Analysis for Agile/SAFe Teams**

Transform your PI Planning sessions with intelligent capacity analysis, red flag detection, and deployment optimization powered by Claude AI.

---

## Overview

PI Strategist is a comprehensive planning analysis tool designed for Agile Release Trains and SAFe teams. It automates the tedious work of validating capacity plans, identifying risks in acceptance criteria, and optimizing deployment strategies—giving teams more time to focus on what matters: delivering value.

### The Problem

PI Planning involves juggling complex spreadsheets, reviewing dozens of DEDs (Design & Execution Documents), and manually validating capacity against commitments. Teams often discover problems late—overloaded sprints, vague acceptance criteria, and deployment conflicts that could have been caught earlier.

### The Solution

PI Strategist ingests your planning artifacts and instantly surfaces:
- **Red flags** in acceptance criteria that will cause scope creep
- **Capacity violations** before they become sprint failures
- **Deployment clusters** optimized for continuous delivery
- **AI-powered recommendations** to rebalance and de-risk your PI

---

## Key Features

### Red Flag Detection

Automatically scans acceptance criteria and user stories for problematic language:

| Category | Examples | Why It's a Problem |
|----------|----------|-------------------|
| Subjective Terms | "fast", "user-friendly", "simple" | Impossible to verify objectively |
| Vague Metrics | "high performance", "scalable" | No measurable threshold |
| Undefined Scope | "comprehensive", "all edge cases" | Scope will expand infinitely |
| Time Ambiguity | "real-time", "immediately" | SLA undefined |

Each flag includes:
- Severity rating (Critical/Moderate/Low)
- Suggested measurable alternative
- Negotiation script for stakeholder discussions

### Capacity Analysis & Validation

Upload your Excel capacity planner to get:
- Sprint-by-sprint capacity breakdown with buffer calculations
- Load vs. capacity visualization with pass/fail status
- Over-allocated resource identification
- Recommendations for rebalancing overloaded sprints

```
Net Capacity = Total Hours - (Total Hours × Buffer%)
Sprint Status = PASS if Load ≤ Net Capacity
```

### Deployment Clustering

Intelligent grouping of features for continuous delivery:
- Feature flag candidates for UI changes
- Canary deployment recommendations for high-risk changes
- Blue-green deployment mapping for API changes
- Dark launch opportunities for analytics features

### AI-Powered Insights (Claude Integration)

Leverage Claude AI for:
- **Executive Summaries**: Auto-generated reports for leadership
- **Risk Assessment**: Holistic analysis of PI health
- **Rebalancing Suggestions**: Specific actions to optimize allocation
- **What-If Scenarios**: Simulate resource changes before committing

### PDF Report Generation

Export comprehensive reports including:
- Red flag analysis with negotiation scripts
- Capacity utilization charts
- Deployment strategy recommendations
- AI-generated executive summary

---

## Screenshots

> *Coming soon: Screenshots of the web interface showing capacity dashboards, red flag analysis, and AI recommendations*

### Dashboard Overview
*[Screenshot placeholder: Main dashboard with PI overview metrics]*

### Red Flag Analysis
*[Screenshot placeholder: Red flags table with severity indicators]*

### Capacity Visualization
*[Screenshot placeholder: Sprint capacity chart with pass/fail status]*

### AI Recommendations
*[Screenshot placeholder: AI-generated insights panel]*

---

## Architecture

### Tech Stack

| Component | Technology |
|-----------|------------|
| Backend | Python 3.10+ |
| Web Framework | Streamlit |
| AI Integration | Anthropic Claude API |
| Document Parsing | python-docx, openpyxl, pdfplumber |
| Data Modeling | Pydantic |
| Reports | Jinja2 templates, PDF generation |

### High-Level Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    PI Strategist Web App                     │
│                       (Streamlit)                            │
├─────────────────────────────────────────────────────────────┤
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐  │
│  │   Analyze   │  │ Quick Check │  │     Scenarios       │  │
│  │    Page     │  │    Page     │  │       Page          │  │
│  └──────┬──────┘  └──────┬──────┘  └──────────┬──────────┘  │
│         │                │                     │             │
│         └────────────────┼─────────────────────┘             │
│                          ▼                                   │
│  ┌───────────────────────────────────────────────────────┐  │
│  │                    Core Engine                         │  │
│  │  ┌─────────┐  ┌──────────┐  ┌────────────────────┐   │  │
│  │  │ Parsers │  │Analyzers │  │     Reporters      │   │  │
│  │  │  - DED  │  │ - Risk   │  │  - Pushback Report │   │  │
│  │  │ - Excel │  │- Capacity│  │  - Capacity Report │   │  │
│  │  │ - PDF   │  │- Deploy  │  │  - Deployment Map  │   │  │
│  │  └─────────┘  └──────────┘  └────────────────────┘   │  │
│  └───────────────────────────────────────────────────────┘  │
│                          │                                   │
│                          ▼                                   │
│  ┌───────────────────────────────────────────────────────┐  │
│  │                  AI Advisor (Claude)                   │  │
│  │  - Executive Summaries  - Risk Assessment              │  │
│  │  - Rebalancing Suggestions  - What-If Analysis         │  │
│  └───────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
```

### Input Formats Supported

- **DED Documents**: Word (.docx), Markdown (.md), PDF
- **Capacity Plans**: Excel (.xlsx) with sprint/resource matrices
- **Quick Check**: Raw text input for instant analysis

---

## Live Demo

The application is deployed and accessible at:

**[https://pi-strategist.streamlit.app/](https://pi-strategist.streamlit.app/)**

> **Note**: Access requires authorization. See below to request access.

---

## Request Access

PI Strategist is currently available by invitation. To request access:

1. **Email**: Contact the maintainer with your use case
2. **GitHub**: Open an issue in this repository describing your team's needs

Please include:
- Your organization/team name
- Approximate team size
- Current PI Planning pain points you're hoping to address

---

## Why PI Strategist?

| Without PI Strategist | With PI Strategist |
|-----------------------|-------------------|
| Hours reviewing DEDs manually | Instant red flag detection |
| Spreadsheet capacity calculations | Automated validation with recommendations |
| Deployment planning in meetings | AI-optimized deployment clusters |
| Reactive problem-solving | Proactive risk identification |
| Gut-feel resource allocation | Data-driven rebalancing suggestions |

---

## Roadmap

- [ ] Jira/Azure DevOps integration for direct import
- [ ] Team velocity tracking and prediction
- [ ] Dependency mapping visualization
- [ ] Slack/Teams notifications for capacity alerts
- [ ] Custom red flag rule configuration

---

## About

Built for SAFe practitioners who believe PI Planning should be about strategic alignment, not spreadsheet wrangling.

**Tech Stack**: Python, Streamlit, Claude AI

---

*This is a showcase repository. The source code is private.*
