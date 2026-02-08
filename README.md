# CampusClick | The Living Archive

CampusClick is a dynamic, modern community platform designed to serve as a digital hub for campus life. It combines event management, social features, and a living archive of memories into a seamless, meaningful user experience.

## 🚀 Overview

CampusClick is built to connect students, capturing the essence of campus life through a digitized timeline, event participation, and shared galleries. It features a robust Role-Based Access Control (RBAC) system, ensuring secure management of content and users while providing a vibrant interface for students and contributors.

## ✨ Key Features

### 👤 User Features
*   **Create Memories:** Users can upload photos to the shared Gallery (subject to moderation).
*   **Event Discovery:** Browse and save upcoming campus events.
*   **Tech Hub & Insights:** Access educational resources and campus insights.
*   **Interactive Timeline:** View a chronological history of campus milestones.
*   **Leaderboard:** Engage with gamified elements of the platform.
*   **Personal Dashboard:** Manage saved events, track profile activity, and customize settings.
*   **Secure Authentication:** Sign up and login securely via Firebase Auth.

### 🛡️ Admin & Moderation
*   **Admin Dashboard:** Centralized control functionality for the platform.
*   **User Management:** View, block, or delete users to maintain community standards.
*   **Content Moderation:** Review and approve/reject user uploads to the gallery.
*   **Activity Logs:** Comprehensive audit trails of all administrative actions.
*   **Analytics:** Visual insights into user engagement and platform usage.

## 🛠️ Technology Stack

This project leverages a modern, high-performance web stack:

### Frontend
*   **Core:** [React 19](https://react.dev/)
*   **Build Tool:** [Vite](https://vitejs.dev/)
*   **Routing:** [React Router Dom](https://reactrouter.com/)
*   **State Management:** React Context API
*   **Language:** JavaScript (ES Modules)

### Styling & UI
*   **Framework:** [Tailwind CSS](https://tailwindcss.com/)
*   **Animations:** [Framer Motion](https://www.framer.com/motion/)
*   **Icons:** [Lucide React](https://lucide.dev/)
*   **Notifications:** React Toastify
*   **Charts:** Chart.js & Recharts

### Backend & Services
*   **BaaS:** [Firebase](https://firebase.google.com/) (Authentication, Firestore, Storage)
*   **AI Integration:** [Google Gemini API](https://deepmind.google/technologies/gemini/) (for content analysis/generation)

## ⚙️ How It Works

1.  **Client-Side Rendering:** The application is a Single Page Application (SPA) served by Vite, providing instant navigation and rich interactivity.
2.  **Authentication Flow:** Users authenticate directly with Firebase Auth. Their session state is managed via `AuthContext` across the app.
3.  **Data Management:** User data, events, and gallery items are stored in Firebase Firestore. Images are stored in Firebase Storage.
4.  **Role Security:** Protected routes (`RequireAuth`, `RequireAdmin`) actively check user claims before granting access to sensitive pages.
5.  **AI Power:** The `gemini.js` service leverages Google's Gemini AI to assist with content generation and insights.

## 🚀 Getting Started

Follow these steps to set up the project locally.

### Prerequisites
*   Node.js (v18 or higher recommended)
*   npm or yarn

### Installation

1.  **Clone the repository**
    ```bash
    git clone <repository-url>
    cd Campusclick
    ```

2.  **Install Dependencies**
    ```bash
    npm install
    ```

### Configuration

Create a `.env` file in the root directory and configure your Firebase and Gemini credentials:

```env
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_bucket.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id
VITE_FIREBASE_MEASUREMENT_ID=your_measurement_id
VITE_GEMINI_API_KEY=your_gemini_api_key
```

### Running the Application

Start the development server:

```bash
npm run dev
```

The application will be available at `http://localhost:5173`.

### Building for Production

To create an optimized production build:

```bash
npm run build
```

## 📂 Project Structure

```
Campusclick/
├── public/              # Static assets
├── src/
│   ├── assets/          # Images and fonts
│   ├── components/      # Reusable UI components
│   │   ├── Auth/        # Auth guards and forms
│   │   ├── Layout/      # Header, Footer, Transitions
│   │   └── ...
│   ├── context/         # AuthContext, ThemeContext
│   ├── pages/           # Application route pages
│   │   ├── Admin/       # Admin dashboards and management
│   │   ├── Auth/        # Login/Register pages
│   │   └── ...
│   ├── services/        # Firebase, Gemini, and API services
│   ├── App.jsx          # Main App component
│   ├── Router.jsx       # Route definitions
│   └── main.jsx         # Entry point
└── ...config files
```

## 🤝 Workflow

### For Contributors (Users)
1.  **Sign Up:** Create an account via the registration page.
2.  **Explore:** Browse events and the gallery.
3.  **Engage:** Upload photos or save events to your profile.
4.  **Manage:** Update profile settings in the Dashboard.

### For Admins
1.  **Login:** Access the dedicated Admin Portal.
2.  **Monitor:** Check the Dashboard for real-time stats.
3.  **Moderate:** Go to the Moderation tab to approve/reject user content.
4.  **Manage Users:** specific user oversight in the User Management tab.
