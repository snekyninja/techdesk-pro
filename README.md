# TechDesk Pro

**AI-powered IT Help Desk Ticketing System** — built as a portfolio project to demonstrate real-world ITSM knowledge, modern JavaScript, and Claude AI integration.

> 🎬 **[Live Demo →](https://snekyninja.github.io/techdesk-pro/)** &nbsp;|&nbsp; Built by **Chris Lytton** &nbsp;|&nbsp; Olathe, KS

---

## What It Is

TechDesk Pro is a fully functional, single-file IT ticketing system that runs entirely in the browser — no server, no database, no dependencies. It replicates the core workflows found in enterprise platforms like **Zendesk**, **Freshservice**, and **Jira Service Management**, with AI triage powered by the **Claude API** (Anthropic).

This project was built to demonstrate:
- Deep understanding of **ITSM concepts and ITIL workflows**
- Proficiency with **vanilla JavaScript** and modern CSS
- Practical knowledge of **AI API integration**
- Awareness of what **IT managers actually care about** day-to-day

---

## Features

### Core Ticketing
| Feature | Details |
|---|---|
| **AI Triage** | Claude Haiku analyzes each ticket and assigns category, priority, and SLA automatically |
| **SLA Timers** | Live countdown per ticket — Critical: 5m, High: 10m, Medium: 15m, Low: 30m |
| **First Response Time** | Separate FRT clock tracks time-to-first-reply vs. resolution time |
| **Ticket Templates** | 8 pre-built SOPs (Password Reset, New Employee Setup, etc.) pre-fill the submit form |
| **Canned Responses** | 9 reply templates with variable substitution (`{{name}}`, `{{tech}}`) |
| **Knowledge Base** | 12 searchable articles across Hardware, Software, Network, Account categories |

### Ticket Lifecycle
| Feature | Details |
|---|---|
| **Ticket Reopen** | Full reopen workflow with reason tracking and CSAT reset — SLA restarts fresh |
| **Priority Override** | Tech can override AI-assigned priority with mandatory reason — audit logged |
| **Pending Response** | Pauses SLA clock while awaiting employee reply — "Mark Responded" restarts it |
| **Escalation (T1→T2)** | Escalate to senior tech with reason, notes, and T2 assignment |
| **Ticket Merge** | Absorb duplicate tickets — notes, time logs, and tags transfer to the parent |
| **Linked Tickets** | Bidirectional Related and Duplicate links between tickets (ITIL concept) |

### Productivity
| Feature | Details |
|---|---|
| **Time Tracking** | Start/Stop timer per ticket + manual time entry — totals visible in IT Team table |
| **Internal Notes** | Private tech notes (not visible to employee) with author and timestamp |
| **Tags / Labels** | Freeform tags with autocomplete library (`vip-user`, `recurring`, `hardware-failure`, etc.) |
| **Ticket Sort** | Sort queue by Priority, SLA Remaining, Age, Status, Name, Newest/Oldest |
| **Search & Filter** | Full-text search + filter by Status, Priority, Category, Tech, Tag simultaneously |
| **Keyboard Shortcuts** | `1-4` nav, `/` search, `R` resolve, `E` escalate, `P` pending, `N` note, `?` help |

### Management & Reporting
| Feature | Details |
|---|---|
| **Dashboard Metrics** | 9 live metric cards: Open, Pending, Escalated, Resolved, Merged, Reopened, SLA Breached, Total, CSAT |
| **SLA Performance Chart** | Dual-metric bar chart — avg resolution time AND first response time vs. SLA targets, per priority |
| **CSV Export** | Full ticket log export with 30+ columns including FRT, time logged, tags, merge/link data |
| **Print / PDF Export** | Clean printer-optimized view of any single ticket — notes, audit log, full history |
| **Ticket Age Display** | Live "2h 14m" age on every queue row — color-coded (fresh/warning/stale) |

### Team & Communication
| Feature | Details |
|---|---|
| **IT Team Dashboard** | Per-tech stats (Open/Escalated/Resolved/CSAT) + full sortable ticket log |
| **CSAT Ratings** | 1–5 star rating from employee after resolution — team averages tracked |
| **System Announcements** | Post outage/maintenance/info banners across all tabs — header status updates live |
| **Demo Data** | One-click load of 8 realistic tickets across all statuses, features, and priorities |

---

## Screenshots
<img width="1862" height="888" alt="image" src="https://github.com/user-attachments/assets/0769826b-7e5b-4b72-841a-3fc587d3a401" />

> 

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla JavaScript (ES6+), CSS3, HTML5 |
| AI | Anthropic Claude API — `claude-haiku-4-5` for ticket triage |
| Fonts | IBM Plex Sans + IBM Plex Mono (Google Fonts) |
| Deployment | GitHub Pages / Vercel |
| Dependencies | **None** — zero npm packages, zero frameworks |

---

## ITIL Concepts Demonstrated

This project directly implements concepts covered in IT support interviews:

- **SLA Management** — First Response Time and Resolution Time tracked separately, with breach detection
- **Ticket Escalation** — T1→T2 workflow with reason logging and tier assignment
- **Incident Linking** — Related and Duplicate ticket relationships (bidirectional)
- **Problem Management** — Ticket Merge consolidates duplicate incidents into one parent
- **Change Management** — Priority override with mandatory justification and audit trail
- **CSAT / Service Quality** — Post-resolution satisfaction ratings with team reporting
- **Knowledge Base** — Self-service articles with copy-to-reply integration
- **Audit Trail** — Full activity log on every ticket (who did what, when, and why)

---

## Running Locally

No install required. Just open the file:

```bash
# Clone the repo
git clone https://github.com/your-username/techdesk-pro.git

# Open in browser — that's it
open techdesk-pro.html
# or just double-click the file in your file explorer
```

The app works fully offline except for:
- AI triage (requires Anthropic API key — falls back to rule-based categorization if unavailable)
- Google Fonts (falls back to system fonts)

### Optional: Add Your API Key

To enable live AI triage, add your Anthropic API key before the closing `</script>` tag:

```html
<script>
  window.ANTHROPIC_API_KEY = 'sk-ant-your-key-here';
</script>
```

> ⚠️ For demo/portfolio use only. Do not expose API keys in production.

---

## Project Background

Built over multiple sessions as a portfolio piece while transitioning from restaurant operations into IT support. Every feature was researched against real ITSM platforms (Zendesk, Freshservice, Jira, ServiceNow) to ensure it reflects how actual IT teams work — not just what looks good in a demo.

**Chris Lytton** — Olathe, KS  
Google IT Support Professional Certificate | CompTIA Network+ (in progress)  
[LinkedIn](https://www.linkedin.com/in/chris-lytton/) · [GitHub](https://github.com/snekyninja)

---

## License

MIT — free to use, fork, and learn from.
