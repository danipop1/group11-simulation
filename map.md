---
title: Map
layout: map
nav_order: 4
---

# _data/map.yml

events:
  - id: initial-detection
    title: "Phase 1 – Initial Detection"
    date: "2024-12-01"
    coordinates: [37.7749, -122.4194]   # San Francisco, CA
    description: "Suspicious network activity detected at PacificTelco data center."

  - id: cisa-alert
    title: "Phase 1 – CISA Alert Issued"
    date: "2024-12-02"
    coordinates: [38.9072, -77.0369]     # Washington, DC
    description: "CISA publishes an early warning bulletin on Salt Typhoon."

  - id: media-leak
    title: "Phase 1 – Media Leak"
    date: "2024-12-03"
    coordinates: [40.7128, -74.0060]     # New York, NY
    description: "Major news outlet breaks story on suspected network breaches."

  - id: breach-confirmation
    title: "Phase 2 – Breach Confirmed"
    date: "2024-12-06"
    coordinates: [41.8781, -87.6298]     # Chicago, IL
    description: "MidwestTel confirms unauthorized access to its core routers."

  - id: containment-start
    title: "Phase 2 – Containment Begins"
    date: "2024-12-07"
    coordinates: [29.7604, -95.3698]     # Houston, TX
    description: "Containment firewalls deployed at LoneStar Communications."

  - id: public-disclosure
    title: "Phase 3 – Public Disclosure"
    date: "2024-12-11"
    coordinates: [51.5074, -0.1278]      # London, UK
    description: "International media confirms Salt Typhoon as the attack group."

  - id: lawsuit-filed
    title: "Phase 3 – Lawsuit Filed"
    date: "2024-12-13"
    coordinates: [38.9072, -77.0369]     # Washington, DC
    description: "Class-action suit filed against major carriers over the breach."

  - id: regulatory-response
    title: "Phase 4 – FCC Proposal"
    date: "2024-12-17"
    coordinates: [38.9072, -77.0369]     # Washington, DC
    description: "FCC proposes updates to CALEA requiring annual cybersecurity certifications."

  - id: industry-reform
    title: "Phase 4 – Industry Reform"
    date: "2024-12-18"
    coordinates: [34.0522, -118.2437]    # Los Angeles, CA
    description: "Telecom industry working group publishes draft security reform recommendations."

  - id: resilience-strategy
    title: "Phase 4 – Resilience Strategy"
    date: "2024-12-20"
    coordinates: [47.6062, -122.3321]    # Seattle, WA
    description: "Final resilience framework unveiled by Northwest Communications."

# Optional: you can also define default map settings, e.g. center/zoom
map_settings:
  center: [39.8283, -98.5795]  # Geographic center of contiguous USA
  zoom: 4
