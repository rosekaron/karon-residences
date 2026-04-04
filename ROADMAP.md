# Product Roadmap — Short-Term Rental Booking Platform

> **Living document.** Update this whenever the backlog changes, stories are moved between versions, or scope decisions are made.
>
> Last updated: 2026-04-03

---

## Vision

A fully agentic direct booking platform for short-term rental properties in Stockholm and Mil Palmeras. Built to eliminate OTA dependency, establish a direct guest relationship, and eventually run with minimal human involvement — AI agents handle discovery, booking, communications, pricing, and content.

---

## Version overview

| Version | Theme | Status | Focus |
|---|---|---|---|
| **v1** | MVP — Core booking loop | 🔲 Not started | First paying guest |
| **v2** | Communications | 🔲 Not started | Remove manual messaging workload |
| **v3** | Marketing | 🔲 Not started | Organic + paid traffic on autopilot |
| **v4** | Intelligence | 🔲 Not started | Revenue optimisation |
| **v5** | Scale | 🔲 Not started | Growth & repeat bookings |

---

## v1 — MVP: Core Booking Loop
**Goal:** A guest can find a property, book it, and pay. The host can manage it.

| # | Story area | Status |
|---|---|---|
| 1 | Property listing pages (all properties visible, no search/filter) | 🔲 |
| 2 | Instant booking with payment (Stripe, PayPal, manual) | 🔲 |
| 3 | Booking confirmation email (summary + check-in instructions) | 🔲 |
| 4 | Admin — view, create, edit, cancel bookings | 🔲 |
| 5 | Admin — iCal / Google Calendar sync | 🔲 |
| 6 | Admin — add/edit/publish property listings | 🔲 |

**Deliberately deferred from v1:** AI chat assistant → v2, Guest CRM → v2, Multilingual → v3, All AI agents → v2+, Analytics → v4

---

## v2 — Communications: Automated Guest Messaging
**Goal:** Remove the manual messaging burden. Guest experience feels professional without team effort.

| # | Story area | Status |
|---|---|---|
| 7 | AI agent — auto-reply to guest inquiries (< 60 sec) | 🔲 |
| 8 | AI agent — pre-arrival message (48h before check-in) | 🔲 |
| 9 | AI agent — post-stay follow-up (24h after check-out) | 🔲 |
| 10 | AI chat assistant on property pages | 🔲 |
| 11 | Admin — message template editor | 🔲 |
| 12 | Admin — guest CRM (contact history, notes, tags) | 🔲 |

---

## v3 — Marketing: Content & Social Automation
**Goal:** Organic and paid traffic on autopilot. Platform finds its own guests.

| # | Story area | Status |
|---|---|---|
| 13 | AI agent — weekly blog post suggestions + approval queue | 🔲 |
| 14 | AI agent — blog writing & publishing to CMS | 🔲 |
| 15 | AI agent — SEO content for property pages & landing pages | 🔲 |
| 16 | AI agent — Facebook/Instagram ad campaigns (occupancy-triggered) | 🔲 |
| 17 | Multilingual support (EN, SV, DE, NL) — all guest-facing content | 🔲 |
| 18 | Admin — ad campaign reporting | 🔲 |

---

## v4 — Intelligence: Revenue Optimisation
**Goal:** Make data-driven decisions automatically. Earn more per booking.

| # | Story area | Status |
|---|---|---|
| 19 | AI agent — dynamic pricing (season, demand, local events) | 🔲 |
| 20 | Admin — floor/ceiling price rules per property | 🔲 |
| 21 | Admin — analytics dashboard (occupancy, revenue, traffic sources) | 🔲 |
| 22 | Admin — revenue report export | 🔲 |

---

## v5 — Scale: Growth & Retention
**Goal:** Maximise repeat bookings and open backup channels.

| # | Story area | Status |
|---|---|---|
| 23 | Reviews & ratings | 🔲 |
| 24 | OTA channel sync (Airbnb, Booking.com as backup) | 🔲 |
| 25 | Direct messaging thread UI (replace email-only) | 🔲 |
| 26 | Multi-property discount logic | 🔲 |
| 27 | Guest loyalty / repeat booking incentive | 🔲 |

---

## Scope decisions log

| Date | Decision | Reason |
|---|---|---|
| 2026-04-03 | AI chat assistant moved from v1 → v2 | Not needed to take first booking; adds complexity to MVP |
| 2026-04-03 | Operations split into v2/v3/v4 | Smaller increments, clearer value per release |
| 2026-04-03 | Growth split into v5 | OTA sync and reviews are non-critical until platform has traction |
| 2026-04-03 | Date-based search/filter removed entirely | Too few properties to need it |
| 2026-04-03 | Custom calendar build removed | iCal sync covers the need at lower cost |
