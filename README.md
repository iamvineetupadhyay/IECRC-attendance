# 📋 AttendTrack — Smart Attendance System

AttendTrack is a lightweight, browser-based attendance management system powered by Google Sheets.
It allows you to manage student records, take attendance, and export reports — all without a backend server.

---

## 🚀 Features

* 🔐 Simple Login System (LocalStorage-based)
* 📊 Take Attendance (Present / Absent / Late)
* 📅 Attendance History (Google Sheets sync)
* 📥 Import Students via CSV
* ➕ Add Students Manually
* 📤 Export Attendance to Excel
* 🔄 Real-time Sync with Google Sheets
* 📈 Attendance Summary

---

## 🧠 How It Works

* Data is stored in:

  * **LocalStorage** (temporary/local)
  * **Google Sheets** (permanent storage)

* Uses:

  * Google OAuth 2.0
  * Google Sheets API

---

## 📂 Project Structure

```
AttendTrack/
│
├── index.html      # Main application (UI + logic)
├── README.md       # Documentation
```

---

## ⚙️ Setup Instructions

### 1. Run the Project

Open `index.html` using:

* VS Code Live Server
* OR directly in browser

---

### 2. Setup Google Sheets API

#### Step 1: Create Project

* Go to Google Cloud Console
* Create a new project
* Enable **Google Sheets API**

---

#### Step 2: Create OAuth Client ID

* Application Type: **Web Application**

Add these:

```
Authorized JavaScript Origins:
http://127.0.0.1:5500
http://localhost:5500
```

---

#### Step 3: Add Client ID in App

Go to:

```
Settings → Google Client ID
```

Paste your OAuth Client ID there.

---

### 3. Authorize

* Click **"Authorize Google Sheets Access"**
* Grant permissions

---

## 📊 Required Google Sheet Structure

### Sheet: `Students`

Columns:

* Name
* Roll Number
* Year
* Section

---

### Sheet: `Records`

Columns:

* Date
* Time
* Roll Number
* Student Name
* Year
* Section
* Status

---

## 📥 CSV Import Format

Your CSV file must contain these columns:

```
Roll Number,Student Name,Year,Section
```

⚠️ Rules:

* Roll Number must be unique
* No empty required fields
* Header names should match (case-insensitive)

---

## 📤 Export Feature

You can export:

* Full data
* Last 7 / 30 / 90 days
* Custom date range

Export includes:

* All attendance records
* Date-wise sheets
* Summary sheet

---

## 🔐 Default Login

```
Username: admin
Password: attend123
```

(Change credentials in Settings)

---

## ⚠️ Known Limitations

* Direct Excel (.xlsx) import is not supported (use CSV instead)
* OAuth errors occur if:

  * Client ID is incorrect
  * Origin is not authorized

---

## 🛠 Tech Stack

* HTML, CSS, JavaScript
* Google Sheets API
* Google OAuth 2.0
* XLSX.js

---

## 💡 Future Improvements

* Role-based authentication
* QR-based attendance
* Face recognition
* Backend integration (Node.js / Firebase)

---

## 📌 Author

Vineet
Engineering Student | Java Backend Focus

---

## ⭐ Support

If you find this useful, consider improving or extending it.
