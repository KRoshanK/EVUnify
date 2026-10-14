# EVUnify

**Unified EV Charging Station Aggregator for India**

EVUnify solves a major pain point for EV drivers in India: charging stations from OEM apps (Tata, Mahindra, MG, Maruti, Hyundai, Kia and others) and independent CPOs are fragmented across multiple apps and often invisible on Google Maps.

This project aims to create a neutral platform that aggregates all these stations under one umbrella, respects the original operator networks/apps, and makes them visible and navigable on Google Maps.

## 🚀 Interactive Prototype

A working web prototype is available in [`prototype/index.html`](prototype/index.html).

**Features in the prototype:**
- Dark-themed interactive map (Leaflet + CARTO tiles)
- Sample stations across Mumbai, Delhi NCR, Bengaluru, and Pune from major networks
- Color-coded pins by network (Tata Power, Statiq, MG e-Hub, Charge_iN, Jio-bp, ChargeZone, etc.)
- Filter chips by network
- Station list synced with map
- Popups with status, power, connector, Navigate (Google Maps) and Open App links
- Near Me button (uses browser geolocation)
- Mobile-responsive layout

Open `prototype/index.html` in any browser, or serve the folder locally.

## Problem Statement
- EV owners must install and switch between multiple OEM and CPO apps.
- Many stations (especially OEM-tied) do not appear reliably on Google Maps.
- Range anxiety is amplified by discovery and real-time availability issues.
- No single neutral source of truth for all networks.

## Solution
A unified discovery, mapping, and navigation platform that:
- Aggregates stations from all major OEM and CPO networks.
- Provides real-time or near-real-time status where possible.
- Integrates deeply with Google Maps for visibility and navigation.
- Offers filters, route planning, and deep links back to operator apps for sessions/payments.
- Supports user contributions and verification.

## Status
Research, concept, and interactive prototype complete (October 2026). Ready for MVP planning, real data integration, and partnership outreach.

## Documentation
- [Research Findings](docs/research.md)
- [Product Concept](docs/concept.md)
- [Architecture Outline](docs/architecture.md)
- [Roadmap](docs/roadmap.md)

## Next Steps
1. Validate with EV owners.
2. Prioritize top networks for integration.
3. Expand prototype with real data sources and live status.
4. Pursue partnerships for OCPI / API feeds.
5. Deploy as progressive web app.

---

Built as a response to real user pain points in the Indian EV ecosystem.
