# Student Management System

A modern, responsive web application for managing student records, built as a final project for university. This system provides a clean and efficient interface for administrators to perform CRUD (Create, Read, Update, Delete) operations on student data. It's built with React for the frontend and Firebase for the backend, demonstrating key principles of modern web development.

---

## ✨ Key Features

* **Add, Edit, and Delete Students:** Easily manage student records through an intuitive modal form.
* **Real-time Database:** Powered by Firebase Firestore, all data is synchronized instantly.
* **Live Search:** Instantly search for students by name, email, or student ID.
* **Fully Responsive Design:** The user interface works flawlessly on desktops, tablets, and mobile devices.
* **Secure Sessions:** Uses Firebase Anonymous Authentication to create a secure session for each user.

---

## 🛠️ Technologies Used

* **Frontend:**
    * [**React**](https://reactjs.org/) - A JavaScript library for building user interfaces.
    * [**Tailwind CSS**](https://tailwindcss.com/) - A utility-first CSS framework for rapid UI development (via CDN).
    * [**Lucide React**](https://lucide.dev/) - For clean and consistent icons.

* **Backend & Database:**
    * [**Firebase Firestore**](https://firebase.google.com/docs/firestore) - A scalable NoSQL cloud database for real-time data.
    * [**Firebase Authentication**](https://firebase.google.com/docs/auth) - For handling secure user sessions.

---

## ⚙️ Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

* Node.js (version 14 or later)
* npm (Node Package Manager)
* A free Firebase account

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/student-app-final.git](https://github.com/your-username/student-app-final.git)
    ```

2.  **Navigate to the project directory:**
    ```bash
    cd student-app-final
    ```

3.  **Install dependencies:**
    ```bash
    npm install
    ```

### Firebase Configuration

1.  **Create a Firebase Project:** Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project.

2.  **Create a Web App:** Inside your project, create a new Web App and copy the `firebaseConfig` object.

3.  **Add Config to Code:** Open `src/App.js` and replace the placeholder `firebaseConfig` variable with the one you copied from your Firebase project.

4.  **Enable Authentication:**
    * In the Firebase Console, go to **Build > Authentication**.
    * Click "Get started".
    * Select **"Anonymous"** from the list of providers, enable it, and click **Save**.

5.  **Set Up Firestore Rules:**
    * In the Firebase Console, go to **Build > Firestore Database**.
    * Create a database (start in **test mode**).
    * Go to the **Rules** tab and replace the existing rules with the following:
        ```javascript
        rules_version = '2';
        service cloud.firestore {
          match /databases/{database}/documents {
            match /{document=**} {
              allow read, write: if true;
            }
          }
        }
        ```
    * Click **Publish**.

### Running the Application

1.  **Start the development server:**
    ```bash
    npm start
    ```

2.  Open your browser and navigate to `http://localhost:3000`. The application should now be running.

---

## 📄 License

This project is licensed under the MIT License.
