
# Notifications Demo App

A simple demo project showing how to implement push notifications in a React Native app using Firebase Cloud Messaging (FCM) and a Node.js Express backend.

## Features

### React Native App
- Retrieves and displays the device's FCM token
- Listens for and displays push notifications (foreground and background)

### Node.js Backend
- Provides an API endpoint to send push notifications via FCM
- Uses Firebase Admin SDK for secure server-side messaging

---

## Getting Started

### Prerequisites
- Node.js (v14+ recommended)
- React Native CLI & environment ([React Native Setup Guide](https://reactnative.dev/docs/environment-setup))
- A Firebase project with a service account key
- Android Studio or Xcode for device/emulator testing

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/notifications_demo.git
cd notifications_demo
````

### 2. Setup Firebase

* Download your `serviceAccountKey.json` from the Firebase Console.
* Place it in the `backend/` directory as specified in the code.

### 3. Install Dependencies

#### React Native app:

```bash
npm install
# or
yarn install
```

#### Backend:

```bash
cd backend
npm install
```

---

## Running the App

### Start the backend server:

```bash
cd backend
node index.js
```

> Server runs on port `3000` by default.

### Start the React Native app:

```bash
# From project root
npx react-native run-android
# or
npx react-native run-ios
```

---

## Usage

* The app will log its FCM token in the console.
* Use the `/send-notification` endpoint on the backend to send a push notification to a device by providing its **token**, **title**, and **body**.

---

## Project Structure

```
notifications_demo/
├── App.js                  # React Native app code
├── backend/
│   ├── index.js            # Express server entry point
│   └── src/services/
│       └── fcmService.js   # FCM helper functions
├── serviceAccountKey.json  # Firebase service account key
└── ...
```

---

## License

This project is for **educational/demo purposes**.


