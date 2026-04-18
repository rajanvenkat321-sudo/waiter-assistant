# Waiter Assistant (WaiterAssi) 🍽️

A professional Flutter MVP designed for small restaurants in India. This app streamlines the workflow between waiters, kitchen staff, and the billing counter using real-time synchronization.

## 🏗️ Architecture: Feature-First

This project follows a **Feature-First Architecture** (modular structure). Instead of grouping files by their technical role (screens, models), we group them by real-world functionality. This makes the codebase scalable, easier to test, and highly maintainable.

### 📂 Directory Structure

```text
lib/
├── core/               # Shared logic (Theming, Constants, Helpers)
├── data/               # Unified Data Layer
│   ├── models/         # Domain Entities (Order, MenuItem)
│   ├── providers/      # Global State Management (OrderProvider)
│   └── repositories/   # Data Access (Firebase & Mock protocols)
├── features/           # Modular Functional Areas
│   ├── role_selection/ # Landing & User Access
│   ├── waiter/         # Order creation & Table management
│   ├── kitchen/        # Order preparation tracking
│   └── billing/        # Payment processing
├── shared/             # Reusable UI components (Widgets)
└── main.dart           # App Entry Point
```

## 🚀 Key Features

### 1. Waiter Dashboard
- Real-time table status monitoring.
- Interactive menu selection for placing new orders.
- Direct link to kitchen for instant order updates.

### 2. Kitchen Terminal
- Streamlined view of "Pending" and "In-Progress" orders.
- One-tap status updates (e.g., mark as "Ready").
- Priority-based order sorting.

### 3. Billing Management
- Quick access to active order totals.
- Finalized order verification for smooth checkout.

## 🛠️ Technology Stack

- **Framework**: [Flutter](https://flutter.dev)
- **State Management**: [Provider](https://pub.dev/packages/provider)
- **Database**: [Firebase Firestore](https://firebase.google.com/products/firestore) (Live migration ready)
- **Design System**: Material Design 3 with custom "Outfit" typography.

## 🏁 Setup & Installation

### Local Development
1. **Clone & Install**:
   ```bash
   git clone https://github.com/rajanvenkat321-sudo/waiter-assistant.git
   cd waiter-assistant
   flutter pub get
   ```
2. **Environment**:
   Ensure you have the Flutter SDK installed on your machine.
3. **Run**:
   ```bash
   flutter run
   ```

### Firebase Configuration
The application is pre-architected for Firebase. To enable live sync:
1. Initialize Firebase using the [FlutterFire CLI](https://firebase.flutter.dev/docs/cli/).
2. Confirm `firebase_options.dart` is correctly generated in your `lib/` folder.
3. Toggle the repository implementation in `main.dart` from `MockOrderRepository` to `FirebaseOrderRepository`.

## 📈 Roadmap & Contributions
- [ ] Multi-lingual support (Hindi/Local languages).
- [ ] Offline-first caching for areas with poor connectivity.
- [ ] QR-code based ordering directly for customers.

---
*Maintained by the Waiter Assistant Team.*
