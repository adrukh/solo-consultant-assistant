# Solo Consultant Assistant

A markdown-based business operations system for self-employed consultants, powered by an AI assistant.

You wear every hat when you run a consulting practice — strategy, finance, marketing, sales. This repo gives an AI assistant the structure to help you manage all four, using nothing but markdown files and a set of review procedures.

## How It Works

The repo defines four executive roles — CEO, CFO, CMO, CRO — each with specific responsibilities, review procedures, and red flags. Your business data lives in plain markdown files. When you run a `/review`, the AI reads each role file, checks your data, and surfaces what needs your attention today.

No database. No backend. No automation platform. Just files you can read and edit yourself.

## Getting Started

1. Open this repo with an AI assistant that can read and write files (e.g., Claude with file access, or any LLM tool with a similar setup).
2. Grant access to Gmail, Google Calendar, and a browser — needed for email scans, calendar look-ahead, and LinkedIn checks. See `SETUP.md` for details.
3. The assistant will detect it's a fresh setup and walk you through an onboarding questionnaire to populate your data files.
4. Once set up, use the commands below.

## Commands

| Command | What it does |
|---------|-------------|
| `/review` | Morning review — cycles through CEO, CMO, CRO, CFO roles, checks your data, email, calendar, and LinkedIn, and surfaces action items |
| `/new` | Create a new entry — session, event, client, lead, or contact |
| `/status` | Quick snapshot of clients, pipeline, invoices, and follow-ups |
| `/invoice` | Track that an invoice is needed or has been sent |
| `/log` | Append a freeform note to the audit trail |

## Repo Structure

```
├── CLAUDE.md                 # Agent instructions and command definitions
├── SETUP.md                  # First-run onboarding questionnaire
├── roles/
│   ├── ceo.md                # Strategy, partnerships, service lines
│   ├── cfo.md                # Invoicing, cash flow, contracts, tax
│   ├── cmo.md                # LinkedIn, content, events, network
│   └── cro.md                # Pipeline, engagement health, retainers
├── data/
│   ├── clients.md            # Active and past clients
│   ├── network.md            # Key contacts, referrers, peers
│   ├── communities.md        # Slack groups, Luma pages, meetups, forums
│   ├── services.md           # What you offer and how you price it
│   ├── pipeline.md           # Leads by stage
│   ├── sessions/             # One file per client session (by date)
│   │   └── _template.md
│   └── events/               # One file per event (by date)
│       └── _template.md
└── log/                      # Monthly audit trail of interactions
    └── _template.md
```

## Philosophy

This system is opinionated about a few things:

- **Markdown over databases.** You should be able to open any file and understand your business state without a query language.
- **Roles over chat.** The AI doesn't freelance — it puts on a specific hat (CEO, CFO, CMO, CRO) and follows that role's review procedure. This keeps advice grounded and consistent.
- **Flags over reports.** Reviews surface what needs attention, not a summary of everything. If nothing's wrong, the role gets skipped.
- **You stay in control.** The AI proposes changes and flags issues. You decide what to act on. Every substantive interaction is logged.

## Customizing

The role files and data templates are starting points. Edit them to match how you actually run your practice — add roles, rename fields, change thresholds. The system is just markdown, so there's nothing to break.

## License

MIT
