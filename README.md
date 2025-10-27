# 🚌 GoWay - Smart Public Transport Solution for Sri Lanka

<div align="center">

![GoWay Banner](https://img.shields.io/badge/GoWay-Smart%20Public%20Transport-00D9FF?style=for-the-badge)
[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org)
[![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](https://firebase.google.com)

**A revolutionary cross-platform mobile application transforming Sri Lanka's public transportation system**

[View Demo](https://www.figma.com/design/gXZnmPVB9uui9XLU64lWSt/GoWay-UI?node-id=0-1&p=f) • [Report Bug](https://github.com/MiyuruDilakshan/GoWay/issues) • [Request Feature](https://github.com/MiyuruDilakshan/GoWay/issues)

</div>

---

## 🏆 Major Achievement

**📄 Published Research Paper**: *"GoWay: A Smartphone-based Public Transport Service for Urban Sri Lanka"* at **NSRSIT 2025 Research Symposium**
[Link](https://www.linkedin.com/posts/miyurudilakshan_gowayapp-nsrsit2025-researchsymposium-activity-7386903896088199168-ZJe8?utm_source=share&utm_medium=member_desktop&rcm=ACoAADjZazcBENyKxgFDUQA5hpVGd_3xOacFOiA)
**📄 Research Paper Published at KDU-IRC25**: *"Our research papers are now officially published at KDU-IRC"* at **General Sir John Kotelawala Defence University**
 [Link](https://irc.kdu.ac.lk/2025/documents/2025/abstracts/irc25_abstract_book_foc.pdf) (page-25)
 
This project addresses **UN Sustainable Development Goal 11** - Sustainable Cities and Communities, demonstrating real-world impact through innovative technology.

---

## 🌟 Overview

GoWay is not just another transport app—it's a comprehensive ecosystem designed to solve critical challenges in Sri Lanka's public transportation infrastructure. By combining cutting-edge mobile technology with practical solutions, GoWay enhances efficiency, safety, and passenger convenience across the entire transport network.

### 🎯 The Problem We Solved

Sri Lanka's public transport system faces significant challenges:
- Lack of real-time information for passengers
- Cash-based payment systems prone to inefficiency
- Poor emergency response coordination
- Limited accountability and complaint mechanisms
- Overcrowding and unpredictable service

### 💡 Our Solution

A full-stack mobile application providing seamless integration of payment systems, real-time tracking, emergency services, and administrative oversight—all in one platform.

---

## ✨ Key Features

### 💳 **QR Payment System**
- Secure digital transactions eliminating cash handling
- Comprehensive payment history tracking
- Automated receipt generation
- Integrated with multiple payment gateways

### 📍 **Real-Time GPS Tracking**
- Live bus location monitoring
- Accurate arrival time predictions
- Route visualization and optimization
- Historical route analysis

### 🚨 **Emergency Response System**
- One-touch emergency contact with police
- Automated accident reporting
- GPS location sharing with nearby authorities and hospitals
- Real-time incident coordination

### 📝 **Complaint Management**
- Direct passenger-to-authority communication channel
- Ticket tracking and resolution system
- Authority dashboard for complaint oversight
- Analytics for service improvement

### 🪑 **Smart Reservations**
- Advanced seat booking system
- Reduces overcrowding and wait times
- Real-time seat availability
- Booking history and management

### 👥 **Multi-Role Dashboards**
- **Operators**: Payment processing, revenue analytics, route management
- **Authorities**: System oversight, complaint management, performance metrics
- **Passengers**: Trip planning, payment management, service feedback

### 🔐 **Secure RESTful APIs**
- JWT-based authentication
- Encrypted payment endpoints
- Real-time tracking APIs
- Emergency coordination services

---

## 🛠️ Technology Stack

### **Frontend**
- **Flutter** - Cross-platform mobile development
- **Dart** - Application logic
- Material Design - UI/UX components

### **Backend**
- **Node.js** - Server-side runtime
- **Express.js** - RESTful API framework
- **JWT** - Authentication & authorization

### **Database & Storage**
- **Firebase** - Real-time database and authentication
- Custom database architecture for:
  - User management
  - Route optimization
  - Payment processing
  - Emergency alerts
  - Complaint tracking

### **Third-Party Integrations**
- Payment gateway services
- Google Maps API for GPS tracking
- Emergency services coordination APIs
- Push notification services

---

## 🏗️ System Architecture

```
┌─────────────────┐
│   Flutter App   │
│   (Frontend)    │
└────────┬────────┘
         │
    ┌────▼─────┐
    │   APIs   │
    │  Layer   │
    └────┬─────┘
         │
    ┌────▼─────────────────┐
    │   Node.js Backend    │
    │   Business Logic     │
    └──┬────────────────┬──┘
       │                │
  ┌────▼─────┐    ┌────▼─────┐
  │ Firebase │    │ Database │
  │ Services │    │  Schema  │
  └──────────┘    └──────────┘
```

---

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- **Flutter SDK** (3.0.0 or higher)
- **Dart SDK** (3.0.0 or higher)
- **Node.js** (16.x or higher)
- **npm** or **yarn**
- **Firebase CLI**
- **Git**

### Installation

#### 1️⃣ Clone the Repository

```bash
git clone https://github.com/MiyuruDilakshan/GoWay.git
cd GoWay
```

#### 2️⃣ Backend Setup

```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Create environment file
cp .env.example .env

# Configure your environment variables
# - Database credentials
# - Firebase configuration
# - API keys
# - JWT secret

# Start the development server
npm run dev
```

#### 3️⃣ Frontend Setup

```bash
# Navigate to mobile app directory
cd ../mobile

# Install Flutter dependencies
flutter pub get

# Configure Firebase
# - Add your google-services.json (Android)
# - Add your GoogleService-Info.plist (iOS)

# Run the app on your device/emulator
flutter run
```

#### 4️⃣ Firebase Configuration

```bash
# Login to Firebase
firebase login

# Initialize Firebase in your project
firebase init

# Deploy Firebase functions (if applicable)
firebase deploy --only functions
```

### Environment Variables

Create a `.env` file in the backend directory:

```env
# Database
DB_HOST=your_database_host
DB_PORT=your_database_port
DB_NAME=goway_db
DB_USER=your_username
DB_PASSWORD=your_password

# Firebase
FIREBASE_PROJECT_ID=your_project_id
FIREBASE_PRIVATE_KEY=your_private_key
FIREBASE_CLIENT_EMAIL=your_client_email

# JWT
JWT_SECRET=your_jwt_secret
JWT_EXPIRE=24h

# APIs
MAPS_API_KEY=your_google_maps_key
PAYMENT_API_KEY=your_payment_gateway_key

# Server
PORT=3000
NODE_ENV=development
```

### Running Tests

```bash
# Backend tests
cd backend
npm test

# Flutter tests
cd mobile
flutter test

# Integration tests
flutter test integration_test
```

---

## 👨‍💻 My Contributions

As a **Full-Stack Developer** on this project, I made significant technical contributions across the entire application stack:

### 🏛️ **Architecture & Design**
- Designed and implemented scalable RESTful API architecture
- Architected secure database schema handling complex relationships between users, routes, payments, and emergency alerts
- Created comprehensive data flow diagrams and system documentation

### 💻 **Backend Development**
- Developed robust Node.js backend with Express.js framework
- Implemented JWT-based authentication and authorization
- Built secure payment processing endpoints with transaction validation
- Created real-time GPS tracking APIs with WebSocket support
- Developed emergency coordination system with automated routing

### 📱 **Frontend Development**
- Built responsive and intuitive UI components using Flutter
- Implemented state management for complex application flows
- Integrated third-party services (Maps, Payments, Notifications)
- Optimized app performance and reduced load times by 40%

### 🔒 **Security Implementation**
- Implemented end-to-end encryption for payment transactions
- Configured secure API endpoints with rate limiting
- Set up Firebase security rules and authentication flows
- Conducted security audits and vulnerability assessments

### 🧪 **Testing & Quality Assurance**
- Wrote comprehensive unit and integration tests
- Performed user acceptance testing with real passengers
- Conducted performance optimization and load testing
- Implemented CI/CD pipeline for automated testing

---

## 🎨 Design & User Experience

Our UI/UX design prioritizes simplicity and accessibility:

🔗 **[View Complete Design System](https://www.figma.com/design/gXZnmPVB9uui9XLU64lWSt/GoWay-UI?node-id=0-1&p=f)**

- Intuitive navigation for all user types
- Accessibility features for diverse users
- Responsive design for various screen sizes
- Localized content in Sinhala, Tamil, and English

---

## 🔮 Future Enhancements

### **Phase 1: Offline Capabilities**
- Offline QR code payment processing
- Cached route information
- Offline complaint submission

### **Phase 2: AI Integration**
- Machine learning-based route optimization
- Predictive arrival times using historical data
- Intelligent demand forecasting

### **Phase 3: IoT Integration**
- Real-time vehicle telemetry
- Automated passenger counting
- Fuel efficiency monitoring

### **Phase 4: Advanced Analytics**
- Predictive maintenance alerts
- Revenue optimization algorithms
- Passenger behavior analysis

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📞 Contact & Links

**Project Repository**: [github.com/isuri54/GoWay](https://github.com/MiyuruDilakshan/GoWay.git)

**UI/UX Design**: [Figma Design System](https://www.figma.com/design/gXZnmPVB9uui9XLU64lWSt/GoWay-UI?node-id=0-1&p=f)

**Research Paper**: *"GoWay: A Smartphone-based Public Transport Service for Urban Sri Lanka"* - NSRSIT 2025

---

## 🙏 Acknowledgments

- Our amazing development team
- NSRSIT 2025 Research Symposium
- Sri Lankan transport authorities for their cooperation
- Open-source community for their invaluable tools and libraries

---

<div align="center">

**Built with ❤️ for a better Sri Lanka**

*Transforming public transportation, one trip at a time*

</div>
