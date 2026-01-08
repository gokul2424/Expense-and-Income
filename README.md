# 💸 Cash Flow - Zenith Ultimate Edition

**Cash Flow** is a powerful, privacy-focused, single-file personal finance dashboard. It combines net worth tracking, expense analysis, wealth simulation, and financial independence (FIRE) planning into one responsive interface.

Built with **HTML5, Tailwind CSS, Chart.js, and Firebase**, it runs entirely in the browser with no backend server required.

---

## ✨ Key Features

This application is organized into 9 powerful modules:

1.  **🏠 Dashboard:** Real-time Net Worth, Monthly Burn Rate, AI Insights, Money Flow (Sankey Diagram), and Recent Activity.
2.  **📉 Debts:** Track liabilities, visualize debt composition, and calculate "True Cost" (Principal vs Interest).
3.  **📈 Investments:** Monitor asset allocation and visualize Monthly SIP vs Total Invested.
4.  **👛 Accounts:** Manage liquid cash, bank accounts, credit cards, and loans. Includes auto-summing of liquid vs. debt.
5.  **📝 Activity:** A searchable, filterable history of all income, expenses, and transfers with Edit/Delete capabilities.
6.  **📅 Calendar:** A visual heatmap of your spending habits. Click any day to see transaction details.
7.  **🚀 Future (Strategy):**
    * **FIRE Calculator:** Calculate your "Freedom Number."
    * **Wealth Simulator:** Project compound interest over time.
    * **Budgets & Goals:** Set monthly limits and savings targets.
    * **Quick Tools:** Instant SIP and EMI calculators.
8.  **📄 Reports:** Generate printable, month-by-month Financial Statements and Category Breakdowns.
9.  **👤 Profile & Settings:**
    * **Theme Switcher:** Choose between Indigo, Emerald, Rose, or Violet themes.
    * **Data Management:** Export CSV, Backup JSON, Restore JSON, or Reset App.
    * **Currency:** Toggle between ₹ (INR) and $ (USD).

---

## 🚀 Quick Start

### Prerequisites
* A modern web browser (Chrome, Safari, Edge, Firefox).
* A Google Account (for Firebase).

### Installation

1.  **Download** the `index.html` file.
2.  **Open** the file in any code editor (VS Code, Notepad++, etc.).
3.  **Configure Firebase** (See section below).
4.  **Open** `index.html` in your browser. That's it!

---

## 🔥 Firebase Configuration (Required)

To make the app save your data to the cloud, you need your own free Firebase API keys.

1.  Go to the [Firebase Console](https://console.firebase.google.com/).
2.  Click **"Add Project"** and give it a name (e.g., "MyCashFlow").
3.  **Disable Google Analytics** (not needed) and create the project.
4.  **Setup Authentication:**
    * Go to **Build** -> **Authentication** -> **Get Started**.
    * Select **Google** -> **Enable** -> Save.
5.  **Setup Database:**
    * Go to **Build** -> **Firestore Database** -> **Create Database**.
    * Choose **Start in production mode** -> Next -> Enable.
    * Go to the **Rules** tab in Firestore and change `allow read, write: if false;` to:
        ```javascript
        allow read, write: if request.auth != null;
        ```
    * Click **Publish**.
6.  **Get API Keys:**
    * Click the **Project Settings** (Gear icon) -> General.
    * Scroll down to "Your apps" -> Click the **</> (Web)** icon.
    * Register app (nickname it "Web").
    * **Copy the `firebaseConfig` object.**

### Applying the Keys
Open your `index.html` file, scroll to the bottom script section, and replace the placeholder with your keys:

```javascript
// --- PASTE YOUR FIREBASE CONFIG HERE ---
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT.firebaseapp.com",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_PROJECT.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
};

```

---

## 📱 Mobile vs Desktop

* **Desktop:** Features a persistent sidebar for easy navigation and expanded charts.
* **Mobile:** Features a **scrollable bottom dock**, streamlined headers, and touch-optimized inputs. Also includes a floating "Add Transaction" button (FAB).

---

## 💾 Data Management

Your data belongs to you.

* **Cloud Sync:** Data is synced to your private Firebase Firestore instance.
* **Backup:** Go to **Profile -> Backup JSON** to download a local copy of all your data.
* **Restore:** Go to **Profile -> Restore JSON** to load data from a backup file.
* **Export:** Go to **Profile -> Export CSV** to get a spreadsheet-compatible file of all transactions.

---

## 🛠️ Built With

* **Core:** HTML5, Vanilla JavaScript (ES6 Modules).
* **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN).
* **Charts:** [Chart.js](https://www.chartjs.org/) (via CDN).
* **Database & Auth:** [Firebase v10](https://firebase.google.com/) (via CDN).
* **Icons:** [FontAwesome](https://fontawesome.com/).

---

## 📄 License

This project is open-source. Feel free to modify and distribute it for personal use.

---

**Happy Tracking! 🚀**

```

```
