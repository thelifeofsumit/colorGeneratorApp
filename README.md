# colorGeneratorApp
iOS app to generate random color codes, persist them locally when offline, and sync to Firebase hen internet is available. Includes offline support, network awareness, and error handling
Here’s a professional and complete README.md you can use for your ColorGeneratorApp:


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

- *Language*: Swift
- *Framework*: SwiftUI
- *Storage*: UserDefaults
- *Backend*: Firebase Firestore
- *Network Monitoring*: NWPathMonitor

* Setup Instructions:

1. Clone the repository:

2. Open the .xcodeproj or .xcworkspace file in Xcode.

3. Install Firebase via Swift Package Manager:

Go to File > Add Packages

Add: https://github.com/firebase/firebase-ios-sdk

4. Download GoogleService-Info.plist from Firebase Console and add it to your project.

5. Build and run on Simulator or iPhone

* Firebase Setup:

1. Go to Firebase Console


2. Create a new project


3. Add iOS app with your bundle ID


4. Download GoogleService-Info.plist and add it to the Xcode project


5. Enable Firestore Database


6. Set basic read/write rules for testing:

service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=} {
      allow read, write: if true;
    }
  }
}


* Network Monitoring:

Uses NWPathMonitor to check internet connectivity

Displays online/offline status on the UI

Automatically retries Firebase sync when back online


* Testing Features:

Generate colors offline and close the app → Relaunch to see persistence

Go online → Observe auto-sync with Firebase

Track sync in Firebase Console
