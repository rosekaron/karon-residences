# Product Roadmap — Karon Residences

> **Living document.** Last updated: 2026-04-11

---

## Vision

A direct booking platform for short-term rental properties — eliminates OTA dependency, establishes direct guest relationships, and delivers a complete booking experience with zero host intervention.

Marketing, CRM, analytics, and content operations are handled by **[HiveOps](https://github.com/rosekaron/hiveops)** — a separate agent-driven business operations platform. Karon focuses on listings, bookings, payments, and calendar sync.

White-label ready — replicable for other property owners who want to cut out Airbnb/Booking.com.

---

## Version overview

| Version | Theme | Status | Focus |
|---|---|---|---|
| **v1** | Core Booking Loop | 🚧 In progress | First paying guest |
| **v2** | Kill Bill Payment Gateway | 📋 Planned | Self-hosted payments |
| **v3** | AI Guest Messaging & Auth | 📋 Planned | Automated guest lifecycle |

---

## v1 — Core Booking Loop
**Goal:** A guest can find a property, book it, pay, and receive confirmation. The host can manage bookings and calendar sync.

| # | Story area | Status |
|---|---|---|
| 1 | Property listing pages (guest browsing + availability) | ✅ Complete |
| 2 | Admin — property management (CRUD, photos, CalDAV connections) | ✅ Complete |
| 3 | Booking flow with price breakdown | Up next |
| 4 | Card payment via Stripe (instant confirmation) | Up next |
| 5 | Bank transfer via Wise (pending state, admin approval) | Up next |
| 6 | Booking confirmation email | Up next |
| 7 | Admin — booking list, manual create, cancel, approve transfers | Not started |
| 8 | Admin — CalDAV polling (15 min), sync failures, availability blocking | Not started |

**User stories:** [stories/v1.md](https://github.com/rosekaron/karon-residences/blob/main/stories/v1.md)

---

## v2 — Kill Bill Payment Gateway
**Goal:** Self-hosted payment processing alongside or replacing Stripe.

| # | Story area | Status |
|---|---|---|
| 9 | Kill Bill deployed with Kaui admin UI | 📋 |
| 10 | Guest card payment routed through Kill Bill | 📋 |
| 11 | Admin invoice and payment records in Kill Bill | 📋 |
| 12 | Stripe + bank transfer paths remain functional during migration | 📋 |

---

## v3 — AI Guest Messaging & Auth
**Goal:** Automated guest communications + admin self-service auth.

| # | Story area | Status |
|---|---|---|
| 13 | AI agent — auto-reply to guest inquiries (< 60 sec) | 📋 |
| 14 | AI agent — pre-arrival message (48h before check-in) | 📋 |
| 15 | AI agent — post-stay follow-up (24h after check-out) | 📋 |
| 16 | AI chat assistant on property pages | 📋 |
| 17 | Role-based access (admin vs co-host) | 📋 |
| 18 | Admin registration UI + password reset | 📋 |

---

## Moved to HiveOps

The following capabilities were originally in this roadmap. They are now managed by AI agents in **[HiveOps](https://github.com/rosekaron/hiveops)** — a separate business operations platform.

| Capability | HiveOps Agent |
|---|---|
| Guest CRM (contact history, tags, notes) | CRM Agent |
| Newsletter / email marketing | Email Agent |
| GDPR consent management | Consent Agent |
| Analytics / UTM attribution | Analytics Agent |
| AI blog writing & SEO content | Blog Writer Agent |
| Facebook/Instagram ad campaigns | Ad Campaign Manager Agent |
| Multilingual content (EN, SV, DE, NL) | Translator Agent |
| Dynamic pricing | Future vertical agent |
| Revenue reporting | Analytics Agent |

Karon connects to HiveOps via API. See the [HiveOps Technical Overview](https://github.com/rosekaron/hiveops/blob/main/TECHNICAL-OVERVIEW.md) for details.

---

## Pre-Production Checklist (v1 Release Gates)

- [ ] Security audit — resolve npm audit vulnerabilities
- [ ] Secrets rotation — replace all placeholder env values
- [ ] Stripe webhook — register production endpoint
- [ ] Email domain verification in Resend
- [ ] CalDAV credentials — confirm all 3 property calendar connections
- [ ] Database backups — enable automated backups
- [ ] CalDAV password encryption — encrypt at rest
- [ ] RLS policies — verify all tables
- [ ] HiveOps connection — verify Consent, Email, Analytics agents reachable

---

## Scope decisions log

| Date | Decision | Reason |
|---|---|---|
| 2026-04-03 | AI chat assistant moved from v1 → v3 | Not needed for first booking |
| 2026-04-03 | Date-based search/filter removed | Too few properties to need it |
| 2026-04-03 | Custom calendar build removed | iCal sync covers the need |
| 2026-04-11 | Marketing, CRM, analytics, content moved to HiveOps | Not hospitality-specific — reusable across verticals as agent-driven business ops |
| 2026-04-11 | Guest CRM moved from Karon Phase 7 to HiveOps CRM Agent | Any business has customers — CRM is vertical-agnostic |
| 2026-04-11 | Milestones simplified: v1 (booking), v2 (Kill Bill), v3 (messaging + auth) | Karon focuses on booking domain only |
