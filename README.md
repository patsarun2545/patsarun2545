<div align="center">

# Patsarun Kathinthong

**Full Stack Developer** — PERN · MERN · REST API · System Design

*Building production-grade web systems with clean architecture and real business logic*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-patsarun--kathinthong-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/patsarun-kathinthong)
[![Portfolio](https://img.shields.io/badge/Portfolio-patsarun2545.github.io-222?style=flat-square&logo=vercel&logoColor=white)](https://portfolio-patsarun.vercel.app/)
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

| Layer         | Technologies                                                              |
| ------------- | ------------------------------------------------------------------------- |
| **Languages** | JavaScript · TypeScript · Python · SQL · HTML/CSS                         |
| **Frontend**  | React · Next.js · Tailwind CSS · shadcn/ui · Radix UI · Bootstrap · MUI  |
| **Backend**   | Node.js · Express · NestJS                                                |
| **Database**  | PostgreSQL · MongoDB · MySQL · Prisma ORM                                 |
| **State**     | Zustand · TanStack Query · React Context                                  |
| **Tools**     | Git · GitHub · Postman · Figma · Azure · VSCode                           |
| **DevOps**    | Ubuntu Linux · PM2                                                        |

---

## Projects

### 📺 StreamLive

`MERN + Next.js` · May 2026

[![GitHub](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/patsarun2545/live-stream-platform)

Full-stack live streaming platform with RTMP ingest, HLS playback, real-time chat, and a streamer dashboard.

**What makes it interesting:**

* RTMP ingest via OBS — auto-transcoded to HLS with FFmpeg; live viewer count tracked via RTMP `play` / `done` events
* Low-latency HLS playback using hls.js with Safari native fallback
* Real-time live chat per stream room via WebSocket with auto-reconnect (30-char username, 200-char message limits)
* Streamer dashboard — go live, manage stream info, view history, reset stream key (kills active session)
* Search and filter streams by category with text search via MongoDB text index and pagination
* SSR meta tags, Open Graph, JSON-LD, auto-generated `sitemap.xml` and `robots.txt` for SEO
* In-memory cache with 5-second TTL and LRU eviction; cache status returned in `x-cache` header
* Dual roles: `viewer` (default) and `streamer` (create/manage streams) with role-guarded routes

`Next.js` `Node.js` `Express` `MongoDB` `Mongoose` `JWT` `WebSocket` `FFmpeg` `Node-Media-Server` `hls.js` `Helmet`

---

### 📋 Task Manager

`PERN Stack` · Apr 2026

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://task-manager-green-psi.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/patsarun2545/Task-Manager)

Full-stack task management application with JWT authentication, subtask support, drag-and-drop reordering, filtering, and pagination.

**What makes it interesting:**

* Drag-and-drop task reordering persisted to the database via an `order` field using @dnd-kit
* Subtask system — create, toggle completion, and delete nested tasks with in-place cache updates
* Recurring tasks: `daily` or `weekly` (configurable days 0–6) with last-completed tracking
* Filter by status, priority, and category; search with 400ms debounced input; sort by deadline, priority, or date
* Summary bar showing total, pending, done, and overdue counts
* Middleware stack: JWT auth, rate limiting (10 req/15min auth, 100 req/15min API), XSS sanitization, request validation
* Dual-token auth: access token (15min, `localStorage`) + refresh token (7 days, `httpOnly` cookie, stored as SHA-256 hash)
* Forgot password and reset password via email link (Brevo)
* Cron job cleans up expired refresh tokens daily at 02:00
* Full test coverage — Vitest + React Testing Library (client) and Jest + Supertest (server); CI via GitHub Actions

`React 19` `Vite 8` `Node.js` `Express 5` `PostgreSQL` `Prisma 7` `Tailwind CSS 4` `shadcn/ui` `JWT` `Zustand` `TanStack Query` `@dnd-kit` `Vitest` `Jest`

---

### 🛒 Next.js E-Commerce Platform

`Next.js Fullstack` · Mar 2026

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://nextjs-ecommerce-platform-gamma.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/patsarun2545/nextjs-ecommerce-platform)

Full-stack e-commerce system built with **Next.js App Router**, combining frontend and backend in a single architecture with customer and admin experiences.

**What makes it interesting:**

* Fullstack architecture using Next.js Server Actions — no separate backend service
* Role-based system: `CUSTOMER` / `ADMIN` with protected routes via custom JWT middleware (`proxy.ts`)
* Shopping cart with optimistic UI updates (`useOptimistic`) and stock validation on every mutation
* Order lifecycle: `PENDING → PAID → SHIPPED → DELIVERED` with payment slip upload and admin verification
* PromptPay QR code generation for payments via `qrcode` library
* Admin dashboard with revenue stats, growth rate indicators, and stale-order alerts
* Product & category soft-delete / restore system; low-stock alerts at ≤ 5 units
* Multi-image upload with main image selection via **ImageKit CDN** + Sharp (WebP, resized to 1200×1200)
* Server-side caching (`"use cache"`) with tag-based revalidation (`cacheTag` / `cacheLife`) across products, orders, users, and cart
* Zod validation on all inputs; bcrypt password hashing; JWT in HTTP-only cookies (30-day expiry)

`Next.js 16` `React 19` `TypeScript` `PostgreSQL` `Prisma` `Tailwind CSS 4` `shadcn/ui` `Radix UI` `Recharts` `JWT` `ImageKit` `Sharp` `Zod` `Sonner`

---

### 🖥️ Rental Management System

`PERN Stack` · Feb 2026

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://rental-management-system-blush.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/patsarun2545/rental-management-system)

Back-office admin panel for managing the full rental lifecycle — booking, payments, deposits, and penalties.

**What makes it interesting:**

* Multi-step workflow engine: `PENDING → CONFIRMED → ACTIVE → RETURNED → COMPLETED` (with `LATE` and `CANCELLED` branches)
* Payment slip verification with approve/reject logic — uses **PostgreSQL row-level locks** (`FOR UPDATE`, `pg_advisory_xact_lock`) to prevent race conditions on concurrent approvals
* Deposit state machine: `HELD → REFUNDED / DEDUCTED` with partial refund and deduction support
* Penalty module: `LATE` (per day) / `DAMAGE` / `LOST` with auto-generated invoices (`INV-YYYYMMDD-XXXX`)
* Stock reservation conflict-checking across overlapping date ranges; emergency release available per variant
* Return logging per item with condition tracking: `GOOD / DAMAGED / LOST`
* Reports: monthly revenue chart (last 12 months), top 10 most-rented products, overdue rental tracking, low-stock alerts (< 3 units)
* Audit log system with admin action tracking, filtering by action/user, and date-based cleanup
* RBAC middleware restricting `ADMIN`-only routes; last-admin deletion protection

`React 19` `Vite` `Node.js` `Express` `PostgreSQL` `Prisma` `JWT` `bcrypt` `Multer` `Chart.js` `SweetAlert2`

---

### 👗 ChicBorrow — Dress Rental Web *(Graduation Project)*

`PERN Stack` · Dec 2024 – Feb 2025

[![User Demo](https://img.shields.io/badge/User-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://dress-rental-web-wtnm.vercel.app/)
[![Admin Demo](https://img.shields.io/badge/Admin-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://dress-rental-web.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/patsarun2545/dress-rental-web)

Full-stack rental platform with a Customer App and an Admin Panel — dual codebase, dual role system.

**What makes it interesting:**

* Dual-role system: Customer App (React) + Admin Panel (React) as separate frontends sharing one Express backend
* Full rental lifecycle: `wait → pay → send → cancel`; return workflow: `pending → Waitingtocheck → approved / rejected / overdue / pendingConfirmation`
* Cart with rental duration selection, automatic discount and return date calculation, delivery method (pickup/delivery), and deposit + shipping fee summary
* Payment slip upload, shipping proof upload, and return photo upload — each with automatic file replacement
* Shop bank accounts displayed at checkout with transfer info submission
* Wishlist using `localStorage` (no login required to save items)
* **Bulk import via Excel** for products and categories using ExcelJS
* Admin dashboard with 10 summary metric cards and Bar/Line chart toggle (Chart.js)
* Admin roles: `owner` (full access incl. User & Account management) and `use` (standard access)
* Deployed on **Ubuntu Linux with PM2**

`React 18` `Node.js` `Express` `PostgreSQL` `Prisma` `JWT` `Chart.js` `ExcelJS` `SweetAlert2` `multer`

---

### 📱 Mobile Store Web

`MERN Stack` · Jul 2024 – Oct 2024

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://mobile-store-web-jet.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/patsarun2545/mobile-store-web)

Responsive store management system for mobile retail — covering stock purchasing, sales processing, and repair workflows.

**What makes it interesting:**

* Sell workflow with serial number lookup, pending sell list, and atomic confirmation via database transactions
* Bulk stock entry supporting up to **10,000 units** per request, processed in batches of 500 with auto-generated serial suffixes
* Product status machine: `instock → reserved → sold / delete` — prevents race conditions via immediate reservation on sell entry
* Repair/service job tracking with full CRUD; jobs ordered by `payDate` descending
* Company settings with upsert pattern (create on first save, update thereafter)
* Dashboard with monthly income bar chart (Recharts) and business summary stats (total income, pending income, profit margin)
* JWT authentication with role levels (`admin` / `user`); Zod validation and Helmet security headers throughout
* Deployed on **Ubuntu with PM2**

`Next.js 16` `Node.js` `Express` `MongoDB` `Prisma` `TypeScript` `Tailwind CSS 4` `Recharts` `JWT` `Zod` `Helmet`

---

### 🌐 Portfolio Website

`Next.js 16` · Jun 2026

[![Live Demo](https://img.shields.io/badge/Live-Demo-000?style=flat-square&logo=vercel&logoColor=white)](https://portfolio-patsarun.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/patsarun2545/portfolio)

A portfolio that manages itself. EN/TH switching, full admin panel, CSRF protection, and Redis rate limiting — on a portfolio site. Why? Click and find out.

---

<div align="center">
  <sub>⭐ <a href="https://github.com/patsarun2545">patsarun2545</a></sub>
</div>
