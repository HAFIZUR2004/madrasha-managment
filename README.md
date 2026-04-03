# Madrasa Management System (Next.js + TypeScript + Firebase)

A complete **school/madrasa management system** built with **Next.js**, **TypeScript**, and **Firebase**, featuring **biometric attendance**, **real-time results**, **finance management**, and **student/parent dashboards**. Designed for both **administrators** and **students/parents**, with advanced features for modern educational institutions.

---

## 🏗 Core Modules

### 1. Dashboard & Role Management (RBAC)
The system provides **three separate panels** for different user roles:

- **Super Admin (Principal/Owner)**  
  View total income, student count, teacher activities, and overall school metrics.

- **Teacher/Staff**  
  Manage attendance and enter exam results for their assigned classes only.

- **Student/Parent**  
  Access personal profile, fee information, attendance reports, and results.

---

### 2. Student Information System (SIS)
- **Admission Form**: Upload photos and documents.
- **Automatic Roll Number & QR Code** generation.
- **Class & Section Filtering** for easy student search.

---

### 3. Biometric & Auto-Attendance (Main Feature)
- **Biometric Sync**: Connect with fingerprint machines via API.
- **Auto SMS**: Notify parents instantly using **Twilio** or any bulk SMS gateway.
- **Daily/Monthly Reports**: Automatic absent student reports based on date.

---

### 4. Finance & Payment Management
- **Fee Calculator**: Tuition, exam, and other fees.
- **Payment History & Invoices** (PDF download).
- **Due Payment Notifications** for students and parents.

---

### 5. Advanced Features
- **Notice Board**: Publish digital notices directly from the app.
- **ID Card Generator**: One-click ID card printing for all students.
- **Performance Analytics**: Graphical student performance using **Recharts** or **Chart.js**.

---

## 📄 Feature Pages Overview

### 1. Results Page
- **Real-time Data**: Uses Firebase `onSnapshot` for live updates.
- **CRUD Operations**: Add, edit, delete results directly from the browser.
- **Sorting**: Order results by academic year.

### 2. System Settings
- **Institution Profile**: Change name (English & Bengali), phone, email, and address.
- **Language Switching**: English ↔ Bengali using `LanguageContext`.
- **Security UI**: "Dangerous Zone" for critical actions like cache clearing.

### 3. Students Management (SIS)
- **Advanced UI**: Table & card-based student list.
- **QR Code Integration**: Unique QR code per student via `qrcode.react`.
- **Search & Filter**: Search by name/roll or filter by class/section.

### 4. Admin Admissions Page
- **Real-time Application Data** via Firebase `onSnapshot`.
- **Actions**: View or delete specific applications.
- **UI**: Table format showing student name, department, and phone number.

### 5. Attendance Page
- **Live Feed**: Shows students punching in real-time.
- **Status Cards**: Summary of total, present, absent, and SMS notifications.
- **Auto SMS Control**: Toggle automatic parent notifications.
- **Absent List & Parent Call**: Direct call feature for absent students.

### 6. Dashboard Page
- **Data Visualization**: Academic improvement & class distribution charts via `Recharts`.
- **Activity Tracking**: Timeline of recent activities (admissions, notices, etc.).
- **Quick Actions**: Shortcut buttons for attendance & fee collection.

### 7. Finance Page
- **Payment Calculator**: Auto-calculates total fees.
- **Invoice Generation**: Download PDF receipts using `jspdf` & `html2canvas`.
- **History**: Full record of past payments.

### 8. Messages & Notice Board
- **Messages**: Read & delete parent or staff messages.
- **Notice Board**: Publish and manage important school notices.

---

## 🔧 Additional Features
- **Automated Salary Management** for teachers/staff based on attendance.
- **Dynamic Routine Builder**: Drag-and-drop class schedule, auto-updated in student panels.
- **Student/Parent PWA**: Installable Progressive Web App for quick access on mobile devices.

---

## 👩‍🎓 Student/Parent Panel

### Dashboard
- **Attendance Percentage**: Quick summary of monthly attendance.
- **Due Balance**: Highlight remaining fees.
- **Next Class Timing**: Today's upcoming class info.
- **Performance Graph**: Improvement chart over past exams.

### Attendance Page
- **Calendar View**: Color-coded attendance (Green = Present, Red = Absent).
- **History**: Access past attendance records.

### Finance / Fees Page
- **Digital Fee Card**: Total paid & due summary.
- **Payment History**: View previous transactions.
- **PDF Receipt Download**: Generate professional receipts.
- **Online Payment**: Integration with **bKash/Nagad**.

### Results / Marksheet Page
- **Subject-wise Marks**: Table of grades, points, and GPA.
- **Downloadable Report**: Printable marksheet format.
- **Improvement Chart**: Compare current & previous results graphically.

### Notice Board
- **Category Filter**: Exams, holidays, or urgent notices.
- **Timestamp**: Date & time of notice.
- **Detailed View**: Click to read full notice.

### Leave Request
- **Date Selector**: Select leave duration.
- **Reason Box**: Provide leave reason.
- **Status**: Admin approval reflected automatically in attendance.

### Student Profile
- **Personal Info**: Name, parent details, contact info, address.
- **Academic Data**: Roll number, class, section, admission year.
- **Digital ID Card**: QR code-enabled ID card preview & download.

---

## 🛠 Tech Stack
- **Frontend**: Next.js + TypeScript + React + Recharts
- **Backend**: Firebase Firestore & Firebase Auth
- **Payment Gateway**: bKash / Nagad / Stripe
- **SMS Gateway**: Twilio / Bulk SMS API
- **PDF Generation**: jsPDF + html2canvas
- **QR Codes**: `qrcode.react`
- **Biometric Integration**: Fingerprint machine API

---

## 📌 Installation

```bash
# Clone the repo
git clone https://github.com/username/madrasa-management.git

# Install dependencies
cd madrasa-management
npm install

# Run locally
npm run dev
