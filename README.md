# CryptoCrafters

An interactive educational gaming platform featuring Cryptogram and Crossword puzzles. CryptoCrafters blends a vanilla web frontend with robust Firebase integration to handle complex data structures, secure data architecture, and team collaboration workflows.

## Architecture Overview

| Layer | Responsibility | Key Tech |
| --- | --- | --- |
| Frontend | Game interfaces, dashboard, contact forms | Vanilla HTML/CSS/JS |
| Game Engine | Puzzle logic, validation, and interactivity | JavaScript (`crossword.js`, `cryptogram.js`) |
| Storage/Backend | Real-time data handling and backend integration | Firebase (`firebase.js`), Node.js |

## Repository Layout

```text
CryptoCraftersFinal/
├── about.html                  # Project and team information UI
├── about.css                   # Styling for the about page
├── contact.html                # Contact and inquiry interface
├── contact.css                 # Styling for contact page
├── contact.js                  # Contact form submission logic
├── crossword.html              # Crossword puzzle player UI
├── crossword.css               # Crossword styling
├── crossword.js                # Crossword game engine and validation
├── cryptogram.html             # Cryptogram puzzle player UI
├── cryptogram.css              # Cryptogram styling
├── cryptogram.js               # Cryptogram game engine and cipher logic
├── firebase.js                 # Firebase client SDK initialization and config
├── home.html                   # Main landing dashboard
├── home.css                    # Dashboard styling
├── home.js                     # Dashboard routing and state logic
├── icons/                      # Static assets (crypto-logo, keys, cube.gif, etc.)
└── README.md
Prerequisites
Firebase project with Firestore/Realtime Database enabled.

Node.js 18+ (for local development server).

Modern web browser.

Frontend & Database Setup
Populate Firebase config:

JavaScript
// firebase.js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT_ID.appspot.com",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};
Serve locally (using Node.js serve or any static server):

Bash
npx serve .
Open http://localhost:3000/home.html in your browser to access the main dashboard and navigate to the games.

Deployment
Frontend (Firebase Hosting)
Install Firebase CLI and log in:

Bash
npm install -g firebase-tools
firebase login
Initialize and deploy:

Bash
firebase init hosting
firebase deploy --only hosting
Ensure your firebase.json maps the public directory to the folder containing your HTML files.

Useful Docs & Scripts
crossword.js – Contains the core array structures and validation logic for the crossword game.

cryptogram.js – Handles the cipher generation and input matching for the cryptogram game.

firebase.js – Centralized connection point for all backend database integrations.

Project Status & Next Steps
✅ Developed responsive home.html dashboard with direct routing to games.

✅ Built standalone Cryptogram and Crossword game engines using vanilla JavaScript.

✅ Integrated Firebase for secure backend data management.

🔜 Expand puzzle repository databases and implement user authentication for saving scores.
