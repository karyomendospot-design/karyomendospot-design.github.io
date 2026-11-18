# LokaServe — Decentralized Local Home Services Marketplace

**LokaServe** is a mobile-first local service directory and booking application built for the **Pi Network** ecosystem. It connects Pioneers with trusted local technicians (AC repair, handymen, electricians, and home cleaning) using Pi cryptocurrency for booking down-payments (DP).

## Live Demo & Ecosystem Links
- **Live Application (Open via Pi Browser):** `https://github.io`
- **Network Environment:** Pi Testnet

## Key Features
1. **Instant Pi Authentication (`Pi.authenticate`):** Frictionless user onboarding using Pioneer credentials (`username` and `payments` scopes).
2. **Service Discovery & Booking Form:** Users can browse verified local service categories, review transparent DP rates, and submit customer details (name, WhatsApp contact, address, and visit date).
3. **Server-Validated Pi Payments (`Pi.createPayment`):** Secure down-payment processing via Pi Wallet with full server-side approval and completion callbacks.
4. **On-Chain Order Receipt (`TXID`):** Completed bookings are automatically logged in the user's *Pesanan Saya* (My Orders) tab with a verifiable blockchain Transaction ID.

## Technical Architecture
- **Frontend:** Responsive HTML5, CSS3, and Vanilla JavaScript hosted on **GitHub Pages**, integrated directly with **Pi SDK v2.0**.
- **Backend (Serverless):** **Google Apps Script** Web App handling `POST` requests to communicate securely with the official Pi Platform API (`/v2/payments/{paymentId}/approve` and `/complete`) using the developer's Server API Key.
- **Storage:** Client-side `localStorage` for instant order history persistence and blockchain receipt tracking.

## How to Test (For Hackathon Judges)
1. Open **Pi Browser** on your mobile device.
2. Navigate to `https://github.io`.
3. Tap **"Masuk dengan Akun Pi"** (Login with Pi Account) and authorize permissions.
4. Select any local service card and tap **"Pesan Jasa"** (Book Service).
5. Fill in the booking form and tap **"Bayar DP via Pi Wallet"**.
6. Confirm the **Test-Pi** transaction in Pi Wallet. Once completed, view your order receipt and `TXID` under the **"Pesanan Saya"** tab.
