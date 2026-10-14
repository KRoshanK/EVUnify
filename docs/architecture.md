# EVUnify — Architecture Outline

## High-Level Components
- **Backend**: API services (Python/FastAPI or Node.js), PostgreSQL + PostGIS for geospatial data, Redis for status caching.
- **Integration Layer**: Partner adapters (OCPI preferred, REST APIs, public data ingestion).
- **Data Pipeline**: Ingestion, de-duplication, enrichment, verification.
- **Mobile App**: Flutter or React Native.
- **Maps**: Google Maps Platform SDK + contribution tools (Places API / bulk POI updates).
- **Admin**: Station management, partner onboarding, verification dashboard.
- **Auth & Notifications**: Standard user accounts, push notifications.

## Data Sources Priority
1. Partner APIs / OCPI feeds (ideal).
2. Public open data (Open Charge Map, government lists, CPO public maps).
3. User submissions with verification.
4. Avoid aggressive scraping initially (legal and maintenance risks).

## Google Maps Integration
- In-app maps and routing via Google Maps SDK.
- Programmatic submission/update of stations as “Electric vehicle charging station” POIs.
- Include connector details.
- Provide tools for operators and users to contribute missing places.

## Recommended Tech Stack (MVP)
- Backend: FastAPI + PostgreSQL/PostGIS + Redis
- Frontend: Flutter (cross-platform)
- Maps: Google Maps Platform
- Auth: Firebase or custom + JWT
- Payments (later): Razorpay / UPI integrations
- Hosting: Cloud (Vercel/Railway/AWS) — Vercel is already connected

## Data Model (Core)
- Station: id, name, lat/lng, operator, address, connectors[], power, status, price, amenities, last_updated
- Operator/Network: id, name, logo, deep_link_pattern, ocpi_endpoint
- User: profile, vehicle, favorites
- Review / Report: user contributions

## Security & Compliance
- DPDPA compliance for user data.
- Prefer open standards (OCPI).
- Clear attribution to original operators.
