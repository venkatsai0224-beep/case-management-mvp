# Case Management System MVP (CaseFlow Mini)

A lightweight case management MVP designed for a small Indian litigation practice (5–10 advocates),
built on top of Google Sheets (as a backend database) and AppSheet (as the app layer).

## 👤 Who this is for

- Small law offices and chambers
- Legal admins / juniors managing hearings and tasks
- Legal ops roles who want a simple, working case operations system

## 🎯 Problem

Most small law offices track:
- Cases in Excel / notebooks
- Hearings in diaries / WhatsApp
- Tasks verbally or in chats

This leads to:
- Missed or rushed hearings
- No clear “today’s tasks” for juniors
- No single place to see all upcoming dates

## ✅ What this MVP does

- Central **Clients** table
- Central **Cases/Matters** table
- **Hearings** log + calendar view
- **Tasks** table with:
  - Assigned_to
  - Due_date
  - Status (Pending / Done)
  - Overdue highlighting

Core flows:
- See all active cases and their next hearing
- See hearings for the next 14 days
- See “My Tasks” for a given junior
- Add hearings and tasks directly from a case

## 🧱 Stack

- **Backend:** Google Sheets (Clients, Cases, Hearings, Tasks)
- **Frontend:** AppSheet
- (Future) n8n / automation for reminders + AI hearing notes

## 🗂 Data model (v1)

- `Clients` – one row per client
- `Cases` – linked to Clients via `Client_ID`
- `Hearings` – linked to Cases via `Case_ID`
- `Tasks` – linked to Cases via `Case_ID`

Relationships:
- Client → multiple Cases
- Case → multiple Hearings
- Case → multiple Tasks

## 🔜 Roadmap

- Role-based views (Advocate / Junior / Admin)
- Daily WhatsApp / email summary
- AI-powered “Order → Hearing Note” generator
- Simple dashboard (active cases, upcoming hearings, overdue tasks)

## 📌 Status

MVP definition:
- [ ] Data model defined in Sheets
- [ ] AppSheet prototype working
- [ ] “My Tasks” view for juniors
- [ ] “Next 14 days” hearings view
- [ ] Case study written
- [ ] Loom demo recorded

This repo will store:
- Documentation
- Screenshots
- Exported data model diagrams
- (Later) automation scripts / configs
