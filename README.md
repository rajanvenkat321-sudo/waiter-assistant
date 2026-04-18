# Waiter Assistant (WaiterAssi) 🍽️

An MVP Flutter application designed specifically for small restaurants in India to streamline order management and kitchen-to-table coordination.

## 🚀 Key Features

- **Role-Based Dashboards**:
  - **Waiter**: Select tables, take orders, and track delivery status.
  - **Kitchen**: View incoming orders in real-time and mark them as "Ready".
  - **Billing**: Manage finalized orders and generate bills.
- **Real-Time Synergy**: Powered by Firebase Firestore for instantaneous updates across all devices.
- **Responsive Design**: Optimized for portrait use on handheld devices typical for restaurant staff.
- **Themed UI**: A clean, material-design interface using curated typography (Outfit/Roboto).

## 🛠️ Technology Stack

- **Framework**: [Flutter](https://flutter.dev) (v3.0+)
- **State Management**: [Provider](https://pub.dev/packages/provider)
- **Backend/Database**: [Firebase Firestore](https://firebase.google.com/products/firestore)
- **Fonts**: Google Fonts (Outfit)
- **Icons**: Material Design Icons

## 📁 Project Structure

```text
lib/
├── core/           # App theme and global constants
├── models/         # Data models (Orders, Menu Items)
├── providers/      # State management logic
├── repositories/   # Data fetching (Mock & Firebase implementations)
└── screens/        # UI Dashboards (Role Selection, Waiter, Kitchen, Billing)
```

## 🏁 Getting Started

### Prerequisites
- Flutter SDK installed and configured.
- A Firebase project set up on the [Firebase Console](https://console.firebase.google.com/).

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/rajanvenkat321-sudo/waiter-assistant.git
   ```
2. Install dependencies:
   ```bash
   flutter pub get
   ```
3. Run the application:
   ```bash
   flutter run
   ```

### Connecting to Firebase
The project is currently configured to use `FirebaseOrderRepository`. To complete the setup:
1. Run `flutterfire configure` to generate your `firebase_options.dart`.
2. Ensure Firestore collections (`orders`, `menu`) are initialized in your console.
3. Refer to `firebase_migration.dart` in the root for specific implementation details.

## 📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

---
*Developed with ❤️ for the Indian Restaurant Industry.*
