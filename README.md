# 🌿 Plant Disease Detector Web App

A full-stack web application designed to help farmers and plant lovers diagnose plant diseases by simply uploading a picture of a leaf. 

## 🎯 Features
- **Frontend**: Clean, modern UI using HTML, CSS (Flexbox/Grid), and JavaScript.
- **Drag & Drop**: Easily upload plant images via drag-and-drop or clicking.
- **Backend**: Robust Node.js + Express server for handling API requests.
- **AI Integration Ready**: Placeholder structure to quickly plug-and-play any Free Image Vision API.
- **Responsive**: Works flawlessly on Desktop and Mobile.

---

## 📁 Project Structure

```text
plant-disease-detector/
│
├── frontend/             # User Interface
│   ├── index.html        # Main HTML layout
│   ├── style.css         # Styling and animations
│   └── script.js         # Frontend Logic (Uploads, Fetch calls)
│
├── backend/              # Server Side
│   ├── server.js         # Main Express Server
│   ├── package.json      # Dependencies
│   └── .env              # Store your API keys here
│
├── uploads/              # Temporarily uploaded images
└── README.md             # Instructions
```

---

## 🚀 How to Run the Project Locally

### 1. Prerequisites
Ensure you have [Node.js](https://nodejs.org/) installed on your computer.

### 2. Setup the backend
1. Open your terminal and navigate to the project directory:
   ```bash
   cd plant-disease-detector/backend
   ```
2. Install the necessary Node modules (`express`, `multer`, `cors`, `dotenv`):
   ```bash
   npm install
   ```
3. Run the backend server:
   ```bash
   npm start
   ```
   *You should see "🌱 Plant AI Server running! HTTP://localhost:5000"*

### 3. Open the Frontend
1. Open the `frontend` folder.
2. Double-click on `index.html` to open it in your web browser. 
3. (Optional) For the best experience, use an extension like **Live Server** in VS Code.

---

## 🤖 Integrating a Real AI API

Currently, the app uses **Fake/Mock Data** to demonstrate how the UI will look. To integrate a real AI API (like Plant.id, OpenAI Vision, or any free image API):

1. Open `backend/server.js`.
2. Locate the API Key comment section:
   ```javascript
   // ===============================
   // 🔑 ADD YOUR AI API KEY HERE
   // ===============================
   const AI_API_KEY = process.env.AI_API_KEY || "PASTE_YOUR_API_KEY_HERE";
   ```
3. Update the `/api/analyze` route to send `req.file` to your chosen remote AI API instead of returning the mock JSON.
