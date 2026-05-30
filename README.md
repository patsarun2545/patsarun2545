<div align="center">

# Patsarun Kathinthong

**Full Stack Developer** — PERN · MERN · REST API · System Design

*Building production-grade web systems with clean architecture and real business logic*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-patsarun--kathinthong-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/patsarun-kathinthong)
[![Portfolio](https://img.shields.io/badge/Portfolio-patsarun2545.github.io-222?style=flat-square&logo=vercel&logoColor=white)](https://patsarun2545.github.io/profile/)
[![GitHub](https://img.shields.io/badge/GitHub-patsarun2545-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/patsarun2545)
[![Email](https://img.shields.io/badge/Email-patsarun2545%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](https://mail.google.com/mail/?view=cm&to=patsarun2545@gmail.com)

</div>

---

## About

Full Stack Developer based in **Bangkok, Thailand**, with hands-on experience shipping complete web systems — from database schema design to frontend UI.

I focus on building systems with real complexity: multi-role access control, stateful workflows, conflict-checking logic, and automated processes. My projects go beyond CRUD — solving real business problems such as rental lifecycle management, payment verification, stock reservation systems, repair workflow tracking, live streaming infrastructure, and task orchestration.

* 🎓 **Business Computer** — Mahasarakham University (2021–2025)
* 🔐 Experienced in **JWT Auth, RBAC, RESTful API design**
* 📦 Production deployments on **Ubuntu Linux + PM2**
* 📚 Currently learning **NestJS · System Architecture · Advanced Backend Patterns**
* 🤝 Open to **Full Stack · SaaS · Open Source** collaboration

---

## Tech Stack

| Layer         | Technologies                                      |
| ------------- | ------------------------------------------------- |
| **Languages** | JavaScript · TypeScript · Python · SQL · HTML/CSS |
| **Frontend**  | React · Next.js · Tailwind CSS · Bootstrap · MUI  |
| **Backend**   | Node.js · Express · NestJS                        |
| **Database**  | PostgreSQL · MongoDB · MySQL · Prisma ORM         |
| **Tools**     | Git · GitHub · Postman · Figma · Azure · VSCode   |
| **DevOps**    | Ubuntu Linux · PM2                                |

---

## Projects

### 📺 StreamLive

`MERN + Next.js` · May 2026

Full-stack live streaming platform with RTMP ingest, HLS playback, real-time chat, and a streamer dashboard.

**What makes it interesting:**

* RTMP ingest via OBS — auto-transcoded to HLS with FFmpeg
* Low-latency HLS playback using hls.js with Safari native fallback
* Real-time live chat per stream room via WebSocket with auto-reconnect
* Live viewer count tracked via RTMP play/done events
* Streamer dashboard — go live, manage stream, view history, reset stream key
* Search and filter streams by category with debounced input and pagination
* SSR meta tags, Open Graph, JSON-LD, sitemap.xml, and robots.txt for SEO
* Dual roles: `viewer` and `streamer` with role-guarded routes

`Next.js` `Node.js` `Express` `MongoDB` `JWT` `WebSocket` `FFmpeg` `Node-Media-Server` `hls.js`

---

### 📋 Task Manager

`PERN Stack` · Apr 2026

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://task-manager-green-psi.vercel.app/)

Full-stack task management application with JWT authentication, subtask support, drag-and-drop reordering, filtering, and pagination.

**What makes it interesting:**

* Drag-and-drop task reordering persisted to the database via an `order` field
* Subtask system — create and manage nested tasks inside each task
* Filter tasks by status and priority with a summary bar showing counts
* Middleware stack: JWT auth, rate limiting, input sanitization, and request validation
* Full test coverage — Vitest + React Testing Library (client) and Jest (server)
* CI pipeline via GitHub Actions

`React` `Node.js` `Express` `PostgreSQL` `Prisma` `Tailwind CSS` `shadcn/ui` `JWT` `Zustand` `Vitest` `Jest`

---

### 🛒 Next.js E-Commerce Platform

`Next.js Fullstack` · Mar 2026

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://nextjs-ecommerce-platform-gamma.vercel.app/)

Full-stack e-commerce system built with **Next.js App Router**, combining frontend and backend in a single architecture with customer and admin experiences.

**What makes it interesting:**

* Fullstack architecture using Next.js (Server Actions + Route Handlers) — no separate backend service
* Role-based system: `CUSTOMER` / `ADMIN` with protected routes
* Shopping cart with optimistic UI updates and real-time calculation
* Order lifecycle: `PENDING → PAID → SHIPPED → DELIVERED` with status history
* Payment slip upload with admin verification
* PromptPay QR code generation for payments
* Admin dashboard with revenue stats, growth indicators, and stale-order alerts
* Product & category soft-delete / restore system
* Multi-image upload with main image selection via ImageKit CDN + Sharp processing
* Server-side caching (`"use cache"`) with tag-based revalidation across products, orders, users, and cart
* Input validation using Zod and secure JWT (HTTP-only cookie) authentication

`Next.js` `React` `TypeScript` `PostgreSQL` `Prisma` `Tailwind CSS` `JWT` `ImageKit` `Zod`

---

### 🖥️ Rental Management System

`PERN Stack` · Feb 2026

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://rental-management-system-blush.vercel.app/)

Back-office admin panel for managing the full rental lifecycle — booking, payments, deposits, and penalties.

**What makes it interesting:**

* Multi-step workflow engine: `PENDING → CONFIRMED → ACTIVE → RETURNED → COMPLETED`
* Payment slip verification with approve/reject logic — uses **PostgreSQL row-level locks** (`FOR UPDATE`, `pg_advisory_xact_lock`) to prevent race conditions on concurrent approvals
* Deposit state machine: `HELD / REFUNDED / DEDUCTED` with partial refund and deduction support
* Penalty module: `LATE / DAMAGE / LOST` with auto-generated invoices (`INV-YYYYMMDD-XXXX`)
* Stock reservation conflict-checking across overlapping date ranges with emergency release
* Reports: monthly revenue charts (last 12 months), top 10 products, overdue tracking
* Audit log system with admin action tracking and cleanup support
* RBAC middleware restricting admin-only access

`React` `Node.js` `Express` `PostgreSQL` `Prisma` `JWT`

---

### 👗 ChicBorrow — Dress Rental Web *(Graduation Project)*

`PERN Stack` · Dec 2024 – Feb 2025

[![User Demo](https://img.shields.io/badge/User-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://dress-rental-web-wtnm.vercel.app/)
[![Admin Demo](https://img.shields.io/badge/Admin-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://dress-rental-web.vercel.app/)

Full-stack rental platform with a Customer App and an Admin Panel — dual codebase, dual role system.

**What makes it interesting:**

* Dual-role system: Customer App (React) + Admin Panel (React) as separate frontends
* Full rental lifecycle with status tracking: `wait → pay → send → cancel`
* Return workflow with return status: `pending → Waitingtocheck → approved / rejected / overdue`
* Payment slip upload and shipping proof image management
* Cart with rental duration selection, discount calculation, and auto-return date computation
* Shop bank accounts displayed at checkout with transfer info submission
* Wishlist using localStorage (no login required to save items)
* **Bulk import via Excel** (products and categories via ExcelJS)
* Admin dashboard with Bar/Line chart toggle (Chart.js) and 10 summary metric cards
* Deployed on Ubuntu Linux with PM2

`React` `Node.js` `Express` `PostgreSQL` `Prisma` `JWT` `Chart.js` `ExcelJS`

---

### 📱 Mobile Store Web

`MERN Stack` · Jul 2024 – Oct 2024

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://mobile-store-web-jet.vercel.app/)

Responsive store management system for mobile retail — covering stock purchasing, sales processing, and repair workflows.

**What makes it interesting:**

* Sell workflow with serial number lookup and pending sell list confirmation
* Bulk stock entry supporting up to **10,000 units** per transaction
* Repair/service job tracking with full CRUD
* JWT authentication with two role levels (`admin` / `user`)
* Dashboard with monthly income bar chart (Recharts) and business summary stats
* Company settings with upsert pattern (create on first save, update thereafter)
* Deployed on Ubuntu with PM2

`Next.js` `Node.js` `Express` `MongoDB` `Prisma` `TypeScript` `Tailwind CSS` `JWT`

---

### 🌐 Portfolio Website

`React · Vite` · https://patsarun2545.github.io/profile/

Personal site showcasing projects and skills.

`React` `Vite` `GitHub Pages`

---

<div align="center">
  <sub>⭐ <a href="https://github.com/patsarun2545">patsarun2545</a></sub>
</div>
