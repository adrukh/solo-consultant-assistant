# First-Time Setup

When a user first opens this repository with an AI assistant, the assistant should walk them through the following questions to populate their data files. Don't ask everything at once — go section by section.

## Prerequisites

The `/review` command relies on access to your email, calendar, and browser to check things like LinkedIn activity, upcoming events, and financial correspondence. Before starting, make sure your AI assistant has:

- **Gmail access** — needed for email scans across all four roles (CFP notifications, invoice threads, intro emails, tax correspondence, etc.)
- **Google Calendar access** — needed for the CRO calendar look-ahead (upcoming client sessions, declined invites) and CMO event tracking
- **Chrome / browser access** — needed for LinkedIn checks (DMs, profile viewers, recent connections, content cadence) and community scans

How you grant these depends on your setup. If you're using Claude with MCP tools, connect the relevant Google and browser integrations. If you're using another AI assistant, configure the equivalent access.

Without these, the assistant can still manage your data files and run partial reviews — but the email, calendar, and LinkedIn steps will be skipped.

---

## Instructions for the AI Agent

Read this file on first interaction. If `data/clients.md` contains no real entries (only the template placeholder), assume this is a fresh setup and begin the questionnaire below.

Ask the questions conversationally — not as a form. After each section, fill in the corresponding data file before moving on.

---

## 1. The Basics

- What's your name and business name?
- What do you do in one sentence? (e.g., "I'm a fractional CTO for early-stage startups")
- How long have you been consulting independently?
- What's your tax jurisdiction? (country / state / province — needed for CFO role context)

→ *No file to fill yet. This context will inform everything else.*

## 2. Services & Pricing

- What services do you offer? List each one.
- For each: how do you price it? (hourly, fixed, retainer)
- What's your current rate or rate range?
- Is there a service you want to grow vs. one you'd like to phase out?

→ *Fill in `data/services.md`*

## 3. Current Clients

- Who are your active clients right now?
- For each: company name, contact person, what you do for them, rate, and when you started.
- Any paused or recently completed engagements worth tracking?

→ *Fill in `data/clients.md`*

## 4. Pipeline

- Any leads you're currently talking to?
- Any proposals outstanding?
- Where do your leads typically come from? (referrals, LinkedIn, events, inbound, etc.)

→ *Fill in `data/pipeline.md`*

## 5. Network

- Who are the 3–5 people who refer you work or open doors for you?
- Any peer consultants you collaborate or share leads with?
- Communities you're active in? (Slack groups, Luma pages, Meetup groups, Discord servers, online forums)

→ *Fill in `data/network.md` and `data/communities.md`*

## 6. Marketing

- Where do you show up publicly? (LinkedIn, Twitter/X, blog, newsletter, podcast, etc.)
- How often do you post or engage?
- What's working? What's not?

→ *No file to fill. This context helps the CMO role give better advice.*

## 7. Financials (Light Touch)

- What's your typical invoicing cadence? (per session, monthly, on milestone)
- Any outstanding invoices right now?
- Any upcoming tax deadlines you're tracking?

→ *This context helps the CFO role. Specific invoice data gets created via `/new`.*

---

## Done

Once the questionnaire is complete, tell the user:

> "You're set up. Use `/review` any time to run a morning review, or `/new` to log sessions, events, and contacts as they happen. Everything lives in markdown files you can read and edit directly."
