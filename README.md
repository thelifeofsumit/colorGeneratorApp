* ColorGeneratorApp:

An iOS application built with SwiftUI that allows users to generate random hex color codes, view them on stylish cards, store them locally when offline, and automatically sync them to Firebase when online.

* Features:

-  Generate random hex color codes
-  Display color cards dynamically
-  Offline storage using UserDefaults
-  Sync color data to Firebase Firestore when online
-  Network connectivity status indicator (online/offline)
-  Retry sync on failure automatically
-  Persistent state: Color data saved across app launches


* Tech Stack:

- Language:   Swift
- Framework:  SwiftUI
- Storage:    UserDefaults
- Backend:    Firebase Firestore
- Network Monitoring: NWPathMonitor

* Clone the repository:
   ```bash
   git clone https://github.com/thelifeofsumit/ColorGeneratorApp.git
   cd ColorGeneratorApp
