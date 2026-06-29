# StreetPulse 🚦

**StreetPulse** is a modern, full-stack civic engagement platform that empowers citizens to easily report, track, verify, and resolve local infrastructure and community issues. By combining dynamic mapping, real-time notifications, camera capabilities, and AI-powered insights, StreetPulse bridges the gap between local residents and municipal administration to foster cleaner, safer, and stronger neighborhoods.

---

## 🚀 Key Features

*   **Report Local Issues** — Snap a photo using the active camera, add details, select a category, and report issues instantly.
*   **Interactive Issue Map & Feed** — View a dynamic, high-contrast local map featuring marked issue pinpoints, heatmap filters, and list views.
*   **AI-Powered Pulse Assistant** — Chat with an intelligent AI assistant trained to guide civic queries, recommend reporting guidelines, and summarize community feedback.
*   **Community Verification** — Upvote and downvote issues to signal urgency, or confirm when an issue has been resolved.
*   **Real-Time Notifications** — Stay informed with immediate alerts regarding new reports, status changes, or administrative updates in your vicinity.
*   **Impact Leaderboard** — Reward active citizenship with gamified badges, points, and community recognition.
*   **Administrative Command Centre** — Empower administrators to update issue statuses, manage community reports, and send notifications.

---

## 🛠️ Technology Stack

*   **Frontend**: React 18, Vite, Tailwind CSS, Lucide Icons, Framer Motion
*   **Backend**: Node.js, Express (custom full-stack runner with Vite middleware proxy)
*   **Database & Auth**: Google Cloud Firestore (Firebase Client SDK)
*   **AI Intelligence**: Gemini API (Google GenAI SDK)
*   **Animations**: Framer Motion / Motion

---

## 📦 Getting Started

### 📋 Prerequisites

*   [Node.js](https://nodejs.org/) (v18 or higher recommended)
*   [npm](https://www.npmjs.com/) (packaged with Node.js)
*   A Firebase / Firestore database setup
*   A Gemini API Key (for the Pulse AI Assistant)

### ⚙️ Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/streetpulse.git
    cd streetpulse
    ```

2.  **Install the dependencies:**
    ```bash
    npm install
    ```

3.  **Environment Variables:**
    Create a `.env` file in the root directory and define the following variables:
    ```env
    # Gemini API Credentials
    GEMINI_API_KEY=your_gemini_api_key_here
    ```

4.  **Firebase Credentials Configuration:**
    Ensure you place your `firebase-applet-config.json` file in the root directory to authorize Firestore connections:
    ```json
    {
      "apiKey": "YOUR_API_KEY",
      "authDomain": "YOUR_AUTH_DOMAIN",
      "projectId": "YOUR_PROJECT_ID",
      "storageBucket": "YOUR_STORAGE_BUCKET",
      "messagingSenderId": "YOUR_MESSAGING_SENDER_ID",
      "appId": "YOUR_APP_ID",
      "firestoreDatabaseId": "YOUR_DATABASE_ID"
    }
    ```

### 🏃 Running the Application

*   **Development Mode:**
    Starts the full-stack server (with Hot Module Replacement support via custom proxy middleware):
    ```bash
    npm run dev
    ```
    Open `http://localhost:3000` in your browser.

*   **Production Build:**
    Bundles the frontend assets and builds the server code with `esbuild`:
    ```bash
    npm run build
    npm start
    ```

---

## 📸 Camera Guidelines for Mobile (iOS & Android)

StreetPulse uses modern browser `getUserMedia` constraints to provide native, high-performance rear-camera resolution on mobile devices:
- Falls back gracefully to any secondary or basic environment camera if specific rear-lens properties are restricted by the system.
- Leverages continuous autofocus, muted preview streaming, and inline play commands to bypass autoplay sandboxes on Safari (iOS) and Chrome (Android).
- Make sure to accept browser and app-level camera and location permissions when prompted.
