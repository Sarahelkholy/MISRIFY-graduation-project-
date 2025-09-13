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

| Screen           | Demo |
|------------------|------|
| Sign up          | <img src="https://github.com/user-attachments/assets/50b692bd-a36d-4605-a512-3d7a27262d65" alt="sign_up" width="300" /> |
| Login            | <img src="https://github.com/user-attachments/assets/4d0b467b-dbb5-4121-96de-47284691028b" alt="login" width="300" /> |
| Home             | <img src="https://github.com/user-attachments/assets/a2a3c5c8-a9b4-450b-98e1-691317b4be1a" alt="home" width="300" /> |
| Product Details  | <img src="https://github.com/user-attachments/assets/87f9cd10-4100-4840-974f-dd68f59ed477" alt="product_details" width="300" /> |
| Cart             | <img src="https://github.com/user-attachments/assets/d2385661-5db4-44d4-9aed-a3ffabbb92c3" alt="cart" width="300" /> |
| Wishlist         | <img src="https://github.com/user-attachments/assets/66599e39-0c69-48c8-81fc-11418dfae2d8" alt="wishlist" width="300" /> |
| Checkout         | <img src="https://github.com/user-attachments/assets/110fccb2-727f-4779-ad90-52427ec8e0db" alt="checkout" width="300" /> |
| Orders           | <img src="https://github.com/user-attachments/assets/de7b5a33-e69d-41f7-8091-f1801fd3c87c" alt="orders" width="300" /> |
| Notifications    | <img src="https://github.com/user-attachments/assets/5e8dd8d2-b6d0-48e6-b37c-efc98a9d6a27" alt="notifications" width="300" /> |
| Profile          | <img src="https://github.com/user-attachments/assets/846f5d6e-85fa-4e94-ae82-b961d4f74c97" alt="profile" width="300" /> |

---

## 🧱 Tech Stack

**Mobile (this repo’s focus)**  
- Flutter, Dart  
- flutter_native_splash, flutter_screenutil


---

##🧪 Features (Mobile)
Onboarding & Auth (login/register/OTP flows, token storage)

Product list, search, filters, brands & categories

Product details with gallery, reviews & rating

Cart & Wishlist (persisted locally + synced with API)

Checkout (cash/online payments depending on backend config)

Orders history, profile, and notifications

Responsive layout (ScreenUtil), native splash




