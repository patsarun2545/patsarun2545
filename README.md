<div align="center">

# Patsarun Kathinthong

**Full Stack Developer** — PERN · MERN · REST API · System Design

*Building production-grade web systems with clean architecture and real business logic*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-patsarun--kathinthong-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/patsarun-kathinthong)
[![GitHub](https://img.shields.io/badge/GitHub-patsarun2545-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/patsarun2545)
[![Email](https://img.shields.io/badge/Email-patsarun2545@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:patsarun2545@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-patsarun2545.github.io-222?style=flat-square&logo=vercel&logoColor=white)](https://patsarun2545.github.io/profile/)

</div>

---

## About

Full Stack Developer based in **Bangkok, Thailand**, with hands-on experience shipping complete web systems — from database schema design to frontend UI.

I focus on building systems with real complexity: multi-role access control, stateful workflows, conflict-checking logic, and automated processes. My graduation project went beyond CRUD — it solved actual business problems in a rental domain with overlapping availability, payment verification, and penalty management.

- 🎓 **Business Computer** — Mahasarakham University (2021–2025)
- 🔐 Experienced in **JWT Auth, RBAC, RESTful API design**
- 📦 Production deployments on **Ubuntu Linux + PM2**
- 📚 Currently learning **NestJS · System Architecture · Advanced Backend Patterns**
- 🤝 Open to **Full Stack · SaaS · Open Source** collaboration

---

## Tech Stack

| Layer | Technologies |
|---|---|
| **Languages** | JavaScript · TypeScript · Python · HTML/CSS |
| **Frontend** | React · Next.js · Tailwind CSS · Bootstrap · MUI |
| **Backend** | Node.js · Express · NestJS |
| **Database** | PostgreSQL · MongoDB · MySQL · Prisma ORM |
| **Tools** | Git · GitHub · Postman · Figma · Azure · VSCode |
| **DevOps** | Ubuntu Linux · PM2 |

---

## Projects

### 🖥️ Dress Rental — Admin Panel
`PERN Stack` · Feb 2026

Back-office system for managing the full rental lifecycle — booking, payments, deposits, and penalties.

**What makes it interesting:**
- Multi-step workflow engine: `PENDING → CONFIRMED → ACTIVE → RETURNED → COMPLETED`
- Payment slip verification with approve/reject logic for customer-uploaded evidence
- Deposit state machine: `HELD / REFUNDED / DEDUCTED` with automatic calculation
- Penalty module covering `LATE / DAMAGE / LOST` with auto-generated invoices
- Stock conflict-checking to prevent double-booking across overlapping date ranges
- Reporting dashboard: monthly revenue, top-10 products, overdue rentals
- Audit Log with date-range cleanup — full traceability of admin actions
- RBAC middleware restricting all back-office routes to admin roles only

`React` `Node.js` `Express` `PostgreSQL` `Prisma`

---

### 🎓 Online Dress Rental System *(Graduation Project)*
`PERN Stack` · Dec 2024 – Feb 2025

Full-stack dress rental platform with Customer App and Admin Panel — end-to-end booking workflows and role-based access control.

**What makes it interesting:**
- Dual-frontend architecture: Customer App + Admin Panel, each with independent RBAC via JWT middleware
- PostgreSQL schema supporting full rental lifecycle: `PENDING → CONFIRMED → ACTIVE → RETURNED → COMPLETED` with auto `LATE` flagging
- RESTful APIs covering products, rentals, payments, deposits, penalties, returns, and audit logs
- Payment slip upload and verification flow — admins approve or reject customer-submitted evidence
- Deposit lifecycle: `HELD / REFUNDED / DEDUCTED` states with partial deduction support
- Stock reservation conflict-checking to prevent double-booking across rental date ranges
- Customer-facing cart with configurable rental duration, auto return date calculation, discount, and shipping fee summary

`React` `Node.js` `Express` `PostgreSQL` `Prisma` `JWT` `RBAC`

---

### 🛒 Mobile Shop Management System
`MERN Stack` · Jul 2024 – Oct 2024

Responsive store management web app for mobile phone retail — stock, sales, and repair workflows deployed on Linux.

**What makes it interesting:**
- Built with Next.js 14 (App Router), TypeScript, and Tailwind CSS
- MongoDB schema via Prisma ORM covering products, sell orders, service/repair jobs, users, and company settings
- Sell workflow: serial number lookup → pending sell list → bulk confirm → products marked as sold
- Bulk stock entry supporting up to 10,000 units per transaction with soft-delete for products and users
- RESTful APIs for stock management, sell workflow, repair/service jobs, and user administration
- JWT-based middleware with role-based access levels (admin / user)
- Dashboard: total income, total sales, total repair jobs, and monthly income bar chart via Recharts
- Deployed on Ubuntu Linux using PM2 for process management

`Next.js` `Node.js` `MongoDB` `Prisma` `TypeScript` `Tailwind CSS` `Ubuntu` `PM2`

---

### 🌐 Portfolio Website
`React · Vite` · [patsarun2545.github.io/profile](https://patsarun2545.github.io/profile/)

Personal site showcasing projects, skills, and background — deployed via GitHub Pages.

`React` `Vite` `GitHub Pages`

---

<div align="center">
  <sub>⭐ <a href="https://github.com/patsarun2545">patsarun2545</a></sub>
</div>
