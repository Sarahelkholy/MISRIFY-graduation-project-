# MISRIFY – Graduation Project (Mobile App + Backend Integration)

> **Note on authorship:** I built **only the Flutter mobile app** and **connected it to the existing backend**.  
> The server code/configs belong to the team project; my scope here is the mobile client and API integration.

---

## ✨ Overview

MISRIFY is a mobile e-commerce experience built with **Flutter**.  
The app features onboarding, authentication, product catalog, cart, wishlist, checkout, notifications, and profile management.  
It consumes REST APIs from a Node.js/Express backend (MongoDB, JWT, Redis, Stripe/Paymob, Cloudinary, Nodemailer).

---

## 📱 Mobile App Demo

Put your PNGs/JPGs into `docs/demo/` using the names below and this table will render automatically on GitHub.

| Screen            | Demo                                                                 |
|-------------------|----------------------------------------------------------------------|
| Sign up            | !<img width="1080" height="2400" alt="sign_up" src="https://github.com/user-attachments/assets/50b692bd-a36d-4605-a512-3d7a27262d65" />
                          |
| Login        | <img width="1080" height="2400" alt="login" src="https://github.com/user-attachments/assets/4d0b467b-dbb5-4121-96de-47284691028b" />
                      |
| Home              | <img width="1080" height="2400" alt="home" src="https://github.com/user-attachments/assets/a2a3c5c8-a9b4-450b-98e1-691317b4be1a" />
                        |
| Product Details   | <img width="1080" height="2400" alt="product_details" src="https://github.com/user-attachments/assets/87f9cd10-4100-4840-974f-dd68f59ed477" />
                  |
| Cart              | <img width="1080" height="2400" alt="cart" src="https://github.com/user-attachments/assets/d2385661-5db4-44d4-9aed-a3ffabbb92c3" />
             |
| Wishlist          | <img width="1080" height="2400" alt="whishlist" src="https://github.com/user-attachments/assets/66599e39-0c69-48c8-81fc-11418dfae2d8" />
       |
| Checkout          | <img width="1080" height="2400" alt="confirm_order" src="https://github.com/user-attachments/assets/110fccb2-727f-4779-ad90-52427ec8e0db" />
                      |
| Orders   | <img width="1080" height="2400" alt="orders" src="https://github.com/user-attachments/assets/de7b5a33-e69d-41f7-8091-f1801fd3c87c" />
                    |
| Notifications     | <img width="1080" height="2400" alt="notifications" src="https://github.com/user-attachments/assets/5e8dd8d2-b6d0-48e6-b37c-efc98a9d6a27" />
           |
| Profile             | <img width="1080" height="2400" alt="profile" src="https://github.com/user-attachments/assets/846f5d6e-85fa-4e94-ae82-b961d4f74c97" />
                      |


---

## 🧱 Tech Stack

**Mobile (this repo’s focus)**  
- Flutter, Dart  
- flutter_native_splash, flutter_screenutil

---

## 📁 Repository Structure (simplified)

/mobile # Flutter app (this is what I built)
└─ lib/
├─ main.dart
├─ constants/constants.dart # <-- API base URL lives here (appBaseUrl)
├─ controllers/...
└─ views/...

/server # Node/Express backend (team project)
├─ server.js
├─ routes/
├─ controllers/
├─ models/
└─ lib/ (redis, cloudinary, stripe, etc.)

yaml
Copy code

---

## 🚀 Getting Started

### 1) Clone
```bash
git clone https://github.com/Sarahelkholy/MISRIFY-graduation-project-.git
cd MISRIFY-graduation-project-
2) Mobile setup (Flutter)
bash
Copy code
cd mobile
flutter pub get
Configure API base URL (point to your running backend):

Open mobile/lib/constants/constants.dart

Set:

dart
Copy code
const String appBaseUrl = "http://<YOUR-LAN-IP>:5000/api";
On Windows you can find your IPv4 with ipconfig (e.g. 192.168.1.4).
Use your LAN IP so real devices on the same Wi-Fi can reach your PC’s server.

Run on a device:

bash
Copy code
flutter run
# or select a device in VS Code/Android Studio and press Run
3) Backend (if you need to run it locally)
I did not build the backend; these steps are to help you run it for development.

bash
Copy code
cd server
npm ci
Create .env in /server (example placeholders):

env
Copy code
PORT=5000
NODE_ENV=development
CLIENT_URL=http://localhost:5173

MONGO_URL=<your-mongodb-uri>

JWT_SECRET=<secret>
JWT_REFRESH_TOKEN=<secret>

# Redis (local or hosted)
REDIS_URL=redis://127.0.0.1:6379

# Stripe / Paymob / Cloudinary / Email (optional, for full flows)
STRIPE_SECRET_KEY=<key>
PAYMOB_API_KEY=<key>
PAYMOB_INTEGRATION_ID=<id>
PAYMOB_IFRAME_ID=<id>
PAYMOB_HMAC_SECRET=<secret>
CLOUDINARY_CLOUD_NAME=<name>
CLOUDINARY_API_KEY=<key>
CLOUDINARY_API_SECRET=<secret>
NODEMAILER_EMAIL=<email>
NODEMAILER_PASS=<app-password>
(Optional) start Redis locally with Docker:

bash
Copy code
docker run -d --name redis-dev -p 6379:6379 redis:7.2
Start the server:

bash
Copy code
npm run dev   # nodemon
# or
npm start
⚙️ Important Config Notes
CORS: CLIENT_URL in the backend .env should include the app/preview origins you use.
For a Flutter mobile app hitting http://<LAN-IP>:5000, CORS should allow that origin.

LAN Testing: Device and PC must be on the same Wi-Fi; use the PC’s IPv4 in appBaseUrl.

Do not commit secrets: .env files are ignored via .gitignore.

🧪 Features (Mobile)
Onboarding & Auth (login/register/OTP flows, token storage)

Product list, search, filters, brands & categories

Product details with gallery, reviews & rating

Cart & Wishlist (persisted locally + synced with API)

Checkout (cash/online payments depending on backend config)

Orders history, profile, and notifications

Responsive layout (ScreenUtil), native splash


