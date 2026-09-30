# 🌐 Horizon Frontend — Angular 22 Single Page Application

[![Angular](https://img.shields.io/badge/Angular-22.0-DD0031?style=for-the-badge&logo=angular&logoColor=white)](https://angular.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-6.0-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)](https://getbootstrap.com/)
[![Leaflet](https://img.shields.io/badge/Leaflet-1.9.4-199900?style=for-the-badge&logo=leaflet&logoColor=white)](https://leafletjs.com/)
[![Vitest](https://img.shields.io/badge/Vitest-4.0-FCC72B?style=for-the-badge&logo=vitest&logoColor=black)](https://vitest.dev/)

> The client application for the **Horizon All-in-One Travel & Tourism Booking System**. For a complete system-wide architectural overview, please see the [Root README](../README.md).

---

## 🏗️ Architecture & Highlights

- **Modern Angular 22:** Built strictly with standalone components, modern signals (`signal`, `computed`, `effect`), typed forms, and Angular Router functional guards.
- **Silent JWT Rotation:** Integrated `authInterceptor` that intercepts HTTP responses, reads the `x-access-token` rotation header, and silently updates credentials in local storage without user interruption.
- **Organic Wabi-Sabi Design System:** A tactile, nature-inspired visual design language featuring Fraunces serif headings, Nunito rounded sans-serif body typography, rice-paper palettes, and soft colored drop shadows.
- **Leaflet OpenStreetMap Radar:** Live interactive map tracking guide GPS coordinates with automatic recentering and custom visual markers.
- **Floating AI Concierge:** Real-time conversational drawer powered by Google Gemini with server-grounded actionable booking directives (`FILTER_SLOTS`, `RECOMMEND_BUNDLE`).
- **Client-Side Export Engine:** Direct PDF invoice generation via `jsPDF` and spreadsheet reports via `xlsx` (SheetJS).

---

## 📂 Project Structure

```
src/app/
├── core/
│   ├── guards/               # Role-based route guards (roleGuard)
│   ├── interceptors/         # Auth & API Error interceptors (silent token refresh)
│   ├── layouts/              # Specialized shells (Tourist, Provider, Guide, Admin)
│   └── services/             # HTTP API client services connecting to Spring Boot
├── features/
│   ├── admin/                # Admin dashboards, KYC approval queue, reports
│   ├── auth/                 # Login, registration, password recovery
│   ├── guide/                # Tour guide dashboard, availability, GPS broadcaster
│   ├── landing/              # Public home and service search interface
│   ├── provider/             # Service provider inventory, slot publishing, payments
│   └── tourist/              # Slot search, checkout, cart, groups, GIS radar, AI chat
├── models/                   # Strongly typed TypeScript interfaces & DTOs
└── environments/             # API configuration (localhost:58080 development proxy)
```

---

## 🛠️ Development Server

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Run local dev server:**
   ```bash
   npm start
   # or
   ng serve --port 54200
   ```

3. Navigate to `http://localhost:54200/`. The application will automatically reload if you change any of the source files.

---

## 🧪 Testing

Execute unit tests with the [Vitest](https://vitest.dev/) runner:

```bash
npm test
```

---

## 📦 Production Build

Compile the production bundle with optimization and cache-busting:

```bash
npm run build
```

Build artifacts will be stored in the `dist/` directory.
