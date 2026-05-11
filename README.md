# 🍔 BigBite – AI-Powered Real-Time Food Delivery Platform

> A scalable, real-time food delivery platform powered by AI automation, live logistics tracking, and intelligent multi-role workflows.

---

## 🌟 Executive Summary

**BigBite** is a full-stack, AI-powered food delivery ecosystem designed to automate and streamline interactions between customers, restaurants, and delivery partners in real time.

The platform combines:

* 🧠 Autonomous AI Agents
* ⚡ Real-Time Socket Communication
* 📍 Live GPS Tracking
* 💳 Secure Payment Processing
* 🛵 Intelligent Delivery Logistics

Built with modern technologies like **React**, **Node.js**, **MongoDB**, **Socket.IO**, and **LangChain**, BigBite delivers a highly responsive and scalable user experience.

---

# 🚀 Core Features

## 🧠 Autonomous AI Agent

Engineered an intelligent AI-powered assistant using **LangChain**, **LangGraph**, and **Google Gemini** capable of executing platform actions through natural language and voice commands.

### AI Capabilities

* Add/remove cart items
* Place orders autonomously
* Navigate menus
* Manage wishlists
* Submit reviews
* Execute multi-step workflows using tool-based reasoning

Supports:

* 🎙️ Voice Commands
* 💬 Text-Based Interaction
* 🤖 Multi-Step AI Reasoning Pipelines

---

## ⚡ Real-Time Event-Driven Architecture

Implemented real-time communication using **Socket.IO** for instant updates across the platform.

### Real-Time Features

* Live order tracking
* Rider assignment updates
* Instant restaurant notifications
* Rider location broadcasting
* Dynamic order state synchronization

This architecture significantly reduces API polling and improves platform responsiveness.

---

## 🛠️ Modular Backend Architecture

Designed with a scalable and maintainable architecture using:

* **Node.js**
* **Express.js**
* **MongoDB**
* **Mongoose**
* **JWT Authentication**

### Backend Highlights

* RESTful API design
* Role-based access control
* Protected routes
* Clean controller-service structure
* Async error boundaries
* Session persistence

---

## 💳 Secure Payment System

Integrated **Razorpay** for seamless online payments with support for:

* Online transactions
* Cash on Delivery (COD)
* Payment verification
* Secure checkout workflows

---

## 🛵 Smart Rider Logistics

Implemented geospatial delivery intelligence using the **Haversine Formula**.

### Logistics Features

* Rider detection within a **25km radius**
* Auto-calculated delivery earnings (**₹10/km**)
* Geo-fenced delivery alerts
* Real-time delivery tracking
* Delivery verification using secure PIN handoffs

---

## ⭐ Dynamic Rating & Review System

Customers can provide ratings for:

* Food quality
* Restaurant experience
* Delivery partners

Ratings update dynamically across restaurant dashboards in real time.

---

## 💝 Wishlist & Quick Reordering

Users can:

* Save full carts as wishlists
* Create custom order presets
* Reorder favorite meals in one click

Example:

* “Friday Pizza”
* “Late Night Burger Combo”

---

# 🏢 Platform Services

---

# 🧑‍💼 Customer Features

### 🍽️ Smart Restaurant Browsing

* Discover restaurants using real GPS distance
* Availability-based restaurant filtering
* Interactive restaurant exploration

### 🤖 AI Assistant

* Voice/Text ordering assistant
* Autonomous cart management
* Natural language checkout

### 🛒 Smart Cart & Wishlist

* Save favorite orders
* One-click reordering
* Persistent cart experience

### 📍 Live Order Tracking

* Real-time rider movement
* Live map tracking using React Leaflet
* Order status synchronization

### ⭐ Feedback System

* Rate food and delivery separately
* Post-delivery review prompts

---

# 🏪 Restaurant Features

### 📊 Restaurant Dashboard

Real-time order management with tabs:

* Pending
* Accepted
* Assigned
* Delivered
* Rejected

### 🍔 Menu Management

* Create/Edit food items
* Categorize menus
* Upload food images
* Veg/Non-Veg toggles

### 🔥 Kitchen Control

Temporarily disable incoming orders during rush hours.

### 📈 Analytics

* Ratings overview
* Completed orders tracking
* Live customer feedback

---

# 🛵 Delivery Partner Features

### 🚴 Rider Dashboard

Tabs for:

* Available Deliveries
* Assigned Orders
* Completed Orders

### 📍 Geo-Fenced Delivery Alerts

Riders receive nearby delivery notifications automatically.

### 💰 Earnings Tracker

Tracks:

* Total deliveries
* Daily earnings
* Lifetime earnings
* Distance-based payout calculations

### 🔐 Secure Delivery Verification

4-digit PIN verification system for:

* Restaurant pickup
* Customer handoff

### 🛰️ Live GPS Broadcasting

Real-time location updates every 10 seconds.

---

# 🛠️ Tech Stack

| Domain       | Technologies                                                                                      |
| ------------ | ------------------------------------------------------------------------------------------------- |
| Frontend     | React 18, Vite, React Router, Tailwind CSS, Framer Motion, Axios, Socket.IO Client, React Leaflet |
| Backend      | Node.js, Express.js, MongoDB, Mongoose, Passport.js, JWT, Socket.IO                               |
| AI / NLP     | LangChain, LangGraph, Google Gemini API, Web Speech API                                           |
| Integrations | Razorpay, Cloudinary                                                                              |

---

# 🔧 System Architecture

## 📦 Socket Rooms

| Room                        | Purpose                  |
| --------------------------- | ------------------------ |
| `order_{orderId}`           | Order-specific updates   |
| `restaurant_{restaurantId}` | Restaurant notifications |
| `rider_{riderId}`           | Rider-specific events    |

---

## 📡 Socket Events

| Event                   | Description                      |
| ----------------------- | -------------------------------- |
| `new_order_received`    | Restaurant receives new order    |
| `order_status_changed`  | Broadcast order updates          |
| `new_order_available`   | Notify riders of nearby orders   |
| `order_taken`           | Remove order from available pool |
| `rider_location_update` | Real-time GPS updates            |

---

# 📦 Order State Machine

```txt
pending
   ↓
accepted
   ↓
rider_assigned
   ↓
preparing
   ↓
ready
   ↓
picked_up
   ↓
on_the_way
   ↓
delivered
```

### Additional States

* `cancelled`
* `rejected`
* `auto_rejected`

---

# 📍 Location & Mapping Features

* Haversine distance calculations
* OpenStreetMap integration
* React Leaflet live maps
* Custom map markers
* Rider geo-fencing
* Location permission management

---

# 🎨 UI/UX Features

* Responsive UI
* Smooth animations using Framer Motion
* Optimistic UI updates
* Real-time status badges
* Toast notifications
* Inline modals
* Loading skeletons and transitions

---

# 📱 Major Components

## Customer Components

* `RestaurantExplore.jsx`
* `RestaurantPage.jsx`
* `ViewCart.jsx`
* `OrderTracking.jsx`
* `MyOrders.jsx`

## Restaurant Components

* `RestaurantDashboard.jsx`
* `RestaurantRegistration.jsx`
* `KitchenDetailsModal.jsx`

## Rider Components

* `RiderDashboard.jsx`
* `RiderProfile.jsx`

## Shared Components

* `Navbar.jsx`
* `LoginModal.jsx`
* `SignupModal.jsx`
* `Profile.jsx`
* `LocationPicker.jsx`

---

# 🔐 Authentication & Security

* JWT-based authentication
* Role-based access control
* Secure protected routes
* Session persistence
* Encrypted sensitive payload handling
* Secure Razorpay integration

---

# 🚀 Setup Guide

## 1️⃣ Prerequisites

Ensure the following are installed:

* Node.js (v16+)
* MongoDB
* Git

---

## 2️⃣ Clone Repository

```bash
git clone <repository-url>
cd BigBite
```

---

## 3️⃣ Install Dependencies

### Backend

```bash
cd backend
npm install
```

### Frontend

```bash
cd frontend
npm install
```

---

# ⚙️ Environment Variables

## Backend `.env`

```env
PORT=5000
NODE_ENV=development

# Database
MONGODB_URI=your_mongodb_uri

# Authentication
JWT_SECRET=your_jwt_secret
PASSPORT_CLIENT_ID=your_google_client_id
PASSPORT_CLIENT_SECRET=your_google_client_secret

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# AI APIs
GEMINI_API_KEY=your_gemini_api_key
GROQ_API_KEY=your_groq_api_key

# Razorpay
RAZORPAY_KEY_ID=your_key
RAZORPAY_KEY_SECRET=your_secret
PAYMENT_SECRET=your_payment_secret
```

---

## Frontend `.env`

```env
VITE_SERVER_URL=http://localhost:5000
VITE_SOCKET_URL=http://localhost:5000

VITE_RAZORPAY_KEY_ID=your_razorpay_key

VITE_CLOUDINARY_CLOUD_NAME=your_cloud_name
VITE_CLOUDINARY_UPLOAD_PRESET=your_upload_preset
```

---

# ▶️ Run the Application

## Backend

```bash
cd backend
npm run dev
```

## Frontend

```bash
cd frontend
npm run dev
```

Open:

```txt
http://localhost:5173
```

---

# 🐛 Future Enhancements

* Push notifications
* Advanced analytics dashboard
* Restaurant search & filters
* Multi-language support
* AI-based delivery optimization
* Smart recommendation engine

---

# 👨‍💻 Contributor

## Niketan

Built with ❤️ using React, Node.js, MongoDB, Socket.IO, and AI-powered workflows.
