---
layout: page
title: Event Map
nav_order: 9
permalink: /map/
---

# Event Map

Below is an interactive map illustrating key events in the **Salt Typhoon** simulation. Click on any marker to view details and jump to the corresponding phase in the [Simulation Timeline](/timeline/).

<!-- Leaflet CSS -->
<link 
  rel="stylesheet" 
  href="https://unpkg.com/leaflet/dist/leaflet.css" 
/>

<div id="map" style="width: 100%; height: 600px; margin-bottom: 1em;"></div>

<!-- Leaflet JS -->
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<script>
  document.addEventListener("DOMContentLoaded", function () {
    // Map center & zoom from data file
    var center = [
      {{ site.data.map.center.latitude }}, 
      {{ site.data.map.center.longitude }}
    ];
    var zoom  = {{ site.data.map.center.zoom }};

    // Initialize map
    var map = L.map('map').setView(center, zoom);
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; OpenStreetMap contributors'
    }).addTo(map);

    // Load phase colors
    var phaseColors = {};
    {% for phase in site.data.map.phases %}
      phaseColors[{{ phase.id }}] = "{{ phase.color }}";
    {% endfor %}

    // Add each event marker
    {% for loc in site.data.map.locations %}
      L.circleMarker(
        [{{ loc.latitude }}, {{ loc.longitude }}],
        {
          radius: 8,
          color: phaseColors[{{ loc.phase_id }}],
          fillColor: phaseColors[{{ loc.phase_id }}],
          fillOpacity: 0.8
        }
      )
      .addTo(map)
      .bindPopup(
        "<strong>{{ loc.name }}</strong><br/>" +
        "{{ loc.description }}<br/>" +
        "<a href='{{ loc.url }}'>View Phase</a>"
      );
    {% endfor %}
  });
</script>
