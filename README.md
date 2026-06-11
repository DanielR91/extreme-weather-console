# Extreme Weather Console 🌐

An interactive, high-fidelity 3D Globe telemetry dashboard visualizing real-time global geological, meteorological, and severe hazard data. Designed with a dark cyber-grid aesthetic, the console translates live feeds into animated spatial vectors mapped onto a rotating orthographic canvas projection.

🔗 **Live Deployment:** [extreme-weather-console.vercel.app](https://extreme-weather-console.vercel.app)

---

## ⚡ Core Features

### 1. Interactive 3D Orthographic Globe
*   **Vector Engine**: High-performance HTML5 Canvas projection that simulates real-time orbital rotation, complete with deep-space background stars and dynamic lighting.
*   **Intuitive Controls**: Drag and rotate the globe on any axis using mouse coordinates to inspect localized anomalies.
*   **Back-Hemisphere Horizon Clipping**: Smart 3D horizon clipping prevents visual bleed, hiding country boundaries, lines, and hazard markers when they rotate behind the sphere's horizon.

### 2. Live Data Visualization Matrices
*   **Seismic Matrix**: Real-time visualization of global seismic activity with color-coded, pulsing rings reflecting magnitude thresholds and depth.
*   **Convective Vortex Corridor**: Real-time atmospheric hazards tracking convective storms, high wind corridors, and hurricane tracks.
*   **Severe Hazards**: Multi-threat plotting map displaying severe global environmental events like flooding, volcanic eruptions, and forest wildfires.

### 3. High-Tech Overlays & Controls
*   **Country Boundaries Coastline**: Seamless vector outline overlay utilizing TopoJSON boundary vectors.
*   **Tectonic Fault Arrays**: A global tectonic boundary network overlay styled as a dashed neon-cyan tactical line (`rgba(34, 211, 238, 0.35)`).
*   **Dynamic Overlay Toggle**: A sidebar toggle switch allowing analysts to turn the Tectonic Fault Arrays on or off instantly without reloading data.
*   **Interactive Raycaster Telemetry Popup**: Click on any data point or text label on the rotating globe to display details like coordinates, magnitudes, categories, depths, and descriptions in a floating tactical card.

---

## 📡 Live Telemetry Data Sources

The dashboard pulls and parses data dynamically on the client side from official, zero-auth public endpoints:

1.  **USGS Earthquake API (Seismic Matrix)**:
    *   *Endpoint*: USGS Live Feed (updated every 15 minutes)
    *   *Payload*: Global earthquake events with magnitude filters, depth vectors, and location names.
2.  **NOAA Weather Feed (Convective Vortex)**:
    *   *Endpoint*: Live convective warning tracking.
    *   *Payload*: Live weather advisories covering tornadoes, severe thunderstorms, and high-wind corridors.
3.  **GDACS API (Severe Hazards)**:
    *   *Endpoint*: Global Disaster Alert and Coordination System SEARCH API.
    *   *Payload*: Live global tracking for Floods (`FL`), Volcanoes (`VO`), and Wildfires (`WF`).
4.  **World Atlas Boundaries**:
    *   *Source*: low-resolution country-110m TopoJSON.
5.  **Tectonic Plate Boundaries**:
    *   *Source*: Open-source global plate boundary GeoJSON.

---

## 🧪 UI/UX Design System
*   **Typography**: Clean monospace styling for that military/scientific console feel.
*   **Colors**: Sleek dark slate backgrounds (`#030712`) coupled with glowing state colors (neon cyan for plate boundaries, hazard gold for severe hazards, rose red for seismic warnings).
