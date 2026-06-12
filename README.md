# Finance-Tracker
A sleek, mobile-friendly, and cloud-synced personal finance management web application. Built with vanilla web technologies and powered by Firebase, this app helps you keep track of your daily expenses, income, and cash flow seamlessly across all your devices.

Features
Cloud Syncing & Authentication: Secure login via Google or a temporary Guest mode. Your data is synced in real-time using Firebase Firestore.

Comprehensive Dashboard: View your monthly earned, spent, and net balance at a glance. Includes a dedicated toggle for cash-only transaction summaries.

Transaction Management: Easily log transactions with details like date, description, amount, type (income/expense), category, and payment mode (online/cash).

Custom Categories: Create and manage your own custom expense categories. These preferences are saved to your cloud profile so they carry over to any device.

In-Depth Analysis: Break down your spending habits hierarchically by year, month, day, and individual items.

Data Portability: Full support for exporting your transaction history to a .csv backup file and importing existing .csv backups.

Progressive Web App (PWA) Ready: Includes an inline web manifest and Apple touch icons for a native app-like experience when saved to your mobile home screen.

Interactive UI: Dark-themed, responsive design with inline cell editing and long-press deletion for quick and easy transaction management.

Tech Stack
Frontend: HTML5, CSS3, Vanilla JavaScript

Backend/Database: Firebase Authentication, Cloud Firestore

Typography: Google Fonts (Rajdhani, DM Sans)

Setup & Installation
Since this is a client-side application using Firebase as a backend, running it locally is incredibly simple.

Clone the repository:

git clone https://github.com/yourusername/finance-tracker.git

2.  **Open the project:**
    Simply open the `index.html` file in your modern web browser. No complex build tools, node modules, or bundlers are required.

## Firebase Configuration

This project is pre-configured with a specific Firebase instance. If you are forking this project to deploy your own version, you will need to set up your own Firebase environment for security and control:

1.  Go to the [Firebase Console](https://console.firebase.google.com/).
2.  Create a new project.
3.  Enable **Authentication** (specifically the Google Sign-In and Anonymous providers).
4.  Enable **Firestore Database**.
5.  Update the `firebaseConfig` object in the `<script>` tag of `index.html` with your new project's credentials:
    ```javascript
    const firebaseConfig = {
        apiKey: "YOUR_API_KEY",
        authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
        projectId: "YOUR_PROJECT_ID",
        storageBucket: "YOUR_PROJECT_ID.appspot.com",
        messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
        appId: "YOUR_APP_ID"
    };
Firestore Security Rules: Ensure your rules are set up so users can only read and write documents that match their own uid.

Usage Guide
Adding an Entry: Fill out the input form on the Home screen and click "Save Entry".

Editing: Click directly on the description or amount in the transaction table to edit them inline. Press Enter or click outside the box to save your changes.

Deleting: Long-press (on mobile) or right-click (on desktop) a transaction row to prompt a deletion confirmation.

Custom Categories: Select "Custom..." from the category dropdown to add a new personalized tag. To delete a custom category, long-press it in the dropdown menu.

Analysis: Navigate to the "Analysis" tab using the bottom navigation bar to view your spending grouped by year, month, and day.
