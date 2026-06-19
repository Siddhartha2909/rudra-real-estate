# 🏡 Rudra Real Estate Pvt. Ltd. — Website

**Quazipura Middhi Road, Harpur, Ballia, Uttar Pradesh 277001**
📞 +91 85889 74638

---

## 📁 Folder Structure

```
rudra-real-estate/
│
├── index.html              ← Main website (open this in browser)
│
├── css/
│   ├── style.css           ← All design & layout styles
│   └── admin.css           ← Admin panel styles
│
├── js/
│   ├── firebase.js         ← Firebase database connection
│   ├── app.js              ← Core utilities, navigation, animations
│   ├── admin.js            ← Admin login/logout, password
│   ├── properties.js       ← Add, edit, delete, render properties
│   └── contact.js          ← Contact form → WhatsApp
│
├── images/
│   └── (add your property photos and logo here)
│
├── sitemap.xml             ← For Google search indexing
└── README.md               ← This file
```

---

## 🚀 How to Open the Website (Right Now)

Simply double-click `index.html` — it opens in your browser immediately.
No installation needed.

---

## 🔐 Admin Login

- Click **"🔐 Admin"** in the top navigation bar
- Password: **`rudra2025`**
- ⚠️ Change the password before going live!
  Open `js/admin.js` → find `const ADMIN_PASSWORD = 'rudra2025';` → change it

---

## 🔥 Setting Up Firebase (Real Database)

Without Firebase, property data is saved only on that one device.
With Firebase, data is saved in the cloud — visible on ALL devices.

### Step 1 — Create Firebase Project (Free)
1. Go to https://console.firebase.google.com
2. Click **"Add Project"** → Name it `rudra-real-estate`
3. Click Continue (you can disable Google Analytics here if you want)
4. Click **Create Project**

### Step 2 — Get Your Config
1. In the Firebase console, click the **`</>`** (Web) icon
2. Name your app **"Rudra Website"** → Click **Register App**
3. You'll see a `firebaseConfig` object. **Copy it.**

### Step 3 — Paste Config into the Website
Open `js/firebase.js` and replace these lines:

```javascript
const firebaseConfig = {
  apiKey:            "REPLACE_WITH_YOUR_API_KEY",
  authDomain:        "REPLACE_WITH_YOUR_AUTH_DOMAIN",
  projectId:         "REPLACE_WITH_YOUR_PROJECT_ID",
  storageBucket:     "REPLACE_WITH_YOUR_STORAGE_BUCKET",
  messagingSenderId: "REPLACE_WITH_YOUR_SENDER_ID",
  appId:             "REPLACE_WITH_YOUR_APP_ID"
};
```

With your actual values from Firebase.

### Step 4 — Enable Firestore Database
1. In Firebase console → **Firestore Database**
2. Click **Create Database**
3. Select **"Start in Test Mode"** → Click **Next** → **Done**

### Step 5 — Enable Storage (for photos)
1. In Firebase console → **Storage**
2. Click **Get Started** → **Next** → **Done**

✅ Done! Your properties and enquiries now save to the cloud.

---

## 📊 Setting Up Google Analytics (Free)

1. Go to https://analytics.google.com
2. Create a new property → Select **Web**
3. Enter your website URL and name
4. Copy your **Measurement ID** (looks like `G-XXXXXXXXXX`)
5. Open `index.html` → Find `G-XXXXXXXXXX` → Replace with your ID
6. Also open `js/app.js` → Find `const GA_ID = 'G-XXXXXXXXXX';` → Replace

---

## 🌐 How to Put the Website Online

### Option A — Netlify (Easiest, Free)
1. Go to https://netlify.com → Sign up free
2. Drag and drop the **entire `rudra-real-estate` folder** onto Netlify
3. Your site is live instantly at a free URL like `rudra-real-estate.netlify.app`
4. You can connect a custom domain like `rudrarealestate.in` later

### Option B — Firebase Hosting (Free)
1. Install Node.js from https://nodejs.org
2. Open terminal/command prompt in the project folder
3. Run: `npm install -g firebase-tools`
4. Run: `firebase login`
5. Run: `firebase init hosting`
6. Run: `firebase deploy`

### Option C — Hostinger/GoDaddy (Paid Hosting)
1. Buy hosting + domain (₹500–₹1,500/year)
2. Upload all files via File Manager or FTP
3. Point your domain to the hosting

---

## 🗺️ Google Search Console (Get on Google)

1. Go to https://search.google.com/search-console
2. Add your website URL
3. Verify ownership (they'll guide you)
4. Submit sitemap: `https://www.yourdomain.in/sitemap.xml`
5. Google will start showing your site in search results within 1–4 weeks

---

## ✏️ How to Customize

### Change Company Details
- Search for `85889 74638` in all files → Replace with your number
- Search for `Harpur, Ballia` → Replace with exact address
- Search for `Director Name` in `index.html` → Replace with real names

### Change Admin Password
- Open `js/admin.js`
- Line 1: `const ADMIN_PASSWORD = 'rudra2025';`
- Change `rudra2025` to your secret password

### Add Your Logo
- Add your logo image to the `images/` folder (e.g. `logo.png`)
- In `index.html`, find `.logo-icon` and replace with:
  `<img src="images/logo.png" alt="Rudra Real Estate" style="width:40px;height:40px;border-radius:8px;"/>`

### Change Colors
- Open `css/style.css`
- At the top, find `:root { ... }`
- Change `--gold`, `--deep-green`, `--mid-green` to your preferred colors

---

## 📞 Support

For any help with the website:
- WhatsApp: +91 85889 74638
- Office: Quazipura Middhi Rd, Harpur, Ballia UP 277001

---

© 2025 Rudra Real Estate Pvt. Ltd. All rights reserved.
