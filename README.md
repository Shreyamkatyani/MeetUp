# MeetUp  🎯

**MeetUp** is a Flutter-based mobile application designed to connect people with similar interests who want to meet up, host, or join local events.  
It allows users to **create events**, **join nearby activities**, and **chat with other participants** — all in one intuitive interface.

---

## 🚀 Features

- 📱 **Phone Number Authentication (OTP)**
  - Users sign up using Firebase phone authentication.
  - Username and Date of Birth are stored in Firestore.

- 🎉 **Event Creation**
  - Host events with a title, description, date/time, and capacity.
  - Event creator details (username, profile photo) stored automatically.

- 👥 **Event Discovery**
  - Real-time event feed using Firestore streams.
  - Join or leave events with a single tap.

- 💬 **In-App Chat**
  - Each event has a dedicated chat room (Firestore subcollection).
  - Messages are updated in real-time.

- 🧑‍💼 **Profile Management**
  - View and manage your profile details.
  - See your hosted events and ratings.

- ⭐ **Event Ratings**
  - Attendees can rate hosted events.
  - Average ratings are displayed to event hosts.

- ☁️ **Firebase Integration**
  - Firebase Authentication  
  - Firestore Database  
  - (Optional) Firebase Storage for profile/event pictures

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-------------|
| Frontend | Flutter (Dart) |
| Backend | Firebase (Auth, Firestore, Storage) |
| Database | Cloud Firestore |
| Authentication | Firebase Phone OTP |
| State Management | Built-in `setState()` & StreamBuilder |
| IDE Recommended | VS Code / Android Studio |

---

## 🧩 Project Structure

lib/
│
├── main.dart # App entry point & route setup
├── firebase_options.dart # Firebase config
├── main_tabs.dart # Bottom navigation
│
├── screens/
│ ├── login_screen.dart # Login via phone number & OTP
│ ├── SignupScreen.dart # User registration
│ ├── home_screen.dart # Events feed
│ ├── create_event_screen.dart # Create new events
│ ├── event_detail_screen.dart # Event details + join/leave
│ ├── chat_screen.dart # Event chat UI
│ ├── hosted_events_screen.dart # List of user-hosted events
│ └── profile_screen.dart # User profile + hosted events
│
└── widgets/
└── common_widgets.dart # Shared UI components

## ⚙️ Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/JOIN-ME.git
   cd JOIN-ME
Install dependencies

bash
Copy code
flutter pub get
Add your Firebase configuration

Replace the existing google-services.json (Android) and GoogleService-Info.plist (iOS) with your own.

Or re-run:

bash
Copy code
flutterfire configure
Run the app

bash
Copy code
flutter run
## 🔐 Firestore Collections Overview
Collection	Description
users	Stores user profiles (username, dob, phone, photo, createdAt)
events	Stores event details (title, description, totalPeople, creator info, joinedUsers, timestamps)
events/{eventId}/chats	Real-time chat messages for each event
events/{eventId}/ratings	Ratings for each event

## 📸 Screens Overview
Screen	Function
Login / Signup	Phone authentication + OTP verification
Home	Browse and join upcoming events
Create Event	Add title, description, and event details
Event Detail	Join, leave, or delete events; open chat
Chat	Event-wise real-time chat
Profile	View personal info and hosted events

## 🧑‍💻 Contributors
**Name**	        **Role**
Shreyam Katyani 	Developer & Maintainer