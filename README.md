# Karon Residences

> A direct booking platform for short-term rental properties — no OTA middleman.

## What This Is

A branded booking website for three properties in Stockholm and Mil Palmeras. Guests browse listings, check live availability, pay by card or bank transfer, and receive instant confirmation. The host manages everything through a protected admin panel.

**Core value:** A guest can find a property, see live availability, pay, and receive confirmation without the host lifting a finger.

**White-label ready** — replicable for other property owners who want direct bookings.

## Learn From My Mistakes

[rose.karon.se/blog](https://rose.karon.se/blog/)

---

## Why Direct Booking

Most short-term rental hosts don't realize they're building someone else's business. Every booking through Airbnb or Booking.com costs 15–20% in commission, but the deeper loss is structural: the host owns nothing — not the guest relationship, not the data, not the brand.

This platform is the exit ramp. Direct bookings mean higher margins, a guest base you own, and pricing logic you control.

## How It Works

| For Guests | For Admin |
|---|---|
| Browse all properties with photos and rates | Create, edit, publish property listings |
| Check real-time availability via calendar | Upload photos via Cloudinary |
| Pay by card (Stripe) or bank transfer (Wise) | Connect CalDAV calendars per property |
| Get instant confirmation email | View, create, cancel bookings |
| Access booking via private link (no account needed) | Approve bank transfer payments |

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | TanStack Start (React, SSR) |
| Database | PostgreSQL 17 + Drizzle ORM |
| Auth | Better Auth (admin only) |
| Payments | Stripe (v1), Kill Bill (v2) |
| Calendar | CalDAV via tsdav |
| Email | Resend (transactional) |
| Photos | Cloudinary |
| Styling | Tailwind CSS + Radix UI |

## Marketing & Operations

Marketing, CRM, analytics, and content are handled by **[HiveOps](https://github.com/rosekaron/hiveops)** — a separate agent-driven business operations platform where AI agents manage consent, email campaigns, analytics, customer relationships, and content creation.

Karon Residences is HiveOps' first customer.

## Roadmap

| Version | What it delivers | Status |
|---|---|---|
| **v1** | Listings, bookings, Stripe/Wise payments, CalDAV sync, admin panel | 🚧 In progress |
| **v2** | Kill Bill self-hosted payment gateway | 📋 Planned |
| **v3** | AI guest messaging + admin auth improvements | 📋 Planned |

[Full roadmap →](https://github.com/rosekaron/karon-residences/blob/main/ROADMAP.md)

## User Stories

[v1 stories →](https://github.com/rosekaron/karon-residences/blob/main/stories/v1.md)

---

*Built by [Rose Karon](https://rose.karon.se)*
