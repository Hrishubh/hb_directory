# 🚀 HB Directory – Startup Pitch Platform

> **A modern, scalable platform for discovering, pitching, and curating startup ideas—built with the latest web technologies and a product-focused mindset.**

![Next.js](https://img.shields.io/badge/Next.js-15-black?style=for-the-badge&logo=next.js)
![React](https://img.shields.io/badge/React-19-blue?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=for-the-badge&logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3-38B2AC?style=for-the-badge&logo=tailwind-css)
![Sanity](https://img.shields.io/badge/Sanity-3.88.3-ff2a2a?style=for-the-badge&logo=sanity)

## 🚀 Live Demo
**[Demo Coming Soon](#)**

## 📋 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Technology Stack](#-technology-stack)
- [Architecture](#-architecture)
- [Installation](#-installation)
- [Usage](#-usage)
- [Contact](#-contact)

---

## 🎯 Overview

**HB Directory** is a full-featured platform for the startup ecosystem. It enables founders to pitch their ideas, users to discover and search startups, and editors to curate the best content. The project demonstrates advanced full-stack engineering, modern UI/UX, and a focus on real-world product value.

> **Note:** This project is based on a YouTube tutorial. You can find the original tutorial here: [YouTube Tutorial](https://www.youtube.com/watch?v=Zq5fmkH0T78)

### What Makes This Project Special
- **Real-Time Content:** Instantly updated startup directory powered by Sanity CMS
- **Seamless Authentication:** One-click GitHub login for frictionless onboarding
- **Rich Pitch Experience:** Media-rich submissions, detailed pitch pages, and curated highlights
- **Production-Ready UX:** Minimal, responsive, and accessible design for all devices
- **Cloud-Native Deployment:** Built for Vercel, monitored with Sentry

---

## ✨ Key Features

- **Live Startup Directory:** Instantly updated, filterable, and searchable
- **Pitch Submission:** Founders submit ideas with rich content and media
- **Editor Picks:** Admins highlight top startups for extra visibility
- **Profile Management:** Users manage their own pitches
- **Engagement Analytics:** View counters and curated highlights
- **Minimal, Modern UI:** Built with Tailwind CSS, Radix UI, and shadcn/ui

---

## 🛠 Technology Stack

- **Frontend:** Next.js 15 (React 19), TypeScript, Tailwind CSS, Radix UI, shadcn/ui
- **Authentication:** NextAuth.js (GitHub OAuth)
- **Database/CMS:** Sanity CMS (headless, real-time)
- **Deployment:** Vercel
- **Monitoring:** Sentry

---

## 🏗 Architecture

```
┌───────────────┐     ┌───────────────┐      ┌───────────────┐
│   Frontend    │────►│   API Layer   │─────►│   Sanity CMS  │
│ (Next.js)     │     │ (Next.js API) │      │ (Content Mgmt)│
└───────────────┘     └───────────────┘      └───────────────┘
        │                     │                      │
        ▼                     ▼                      ▼
┌───────────────┐     ┌────────────────┐     ┌───────────────┐
│ Auth (GitHub) │     │   Sentry CMS   │     │     Vercel    │
└───────────────┘     └────────────────┘     └───────────────┘
```

### **Data Flow**
1. **User Authentication** → GitHub OAuth via NextAuth.js
2. **Pitch Submission** → Data sent to Sanity CMS
3. **Content Discovery** → Real-time queries from frontend to Sanity
4. **Admin Curation** → Editor picks managed via Sanity Studio
5. **Monitoring** → Sentry tracks errors across stack

---

## ⚡ Installation

### Prerequisites
- Node.js 18+
- npm or yarn
- GitHub account (for authentication)
- Sanity account (for content management)

### Setup Instructions
1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd hb_directory
   ```
2. **Install dependencies**
   ```bash
   npm install
   ```
3. **Environment Configuration**
   Create a `.env.local` file with your Sanity and GitHub credentials (see Sanity and GitHub OAuth docs).
    ```bash
    NEXT_PUBLIC_SANITY_PROJECT_ID="your_project_id"
    NEXT_PUBLIC_SANITY_DATASET="your_dataset"
    NEXT_PUBLIC_SANITY_API_VERSION="you_sanity_api_version"
    SANITY_WRITE_TOKEN="your_sanity_write_token"
    AUTH_GITHUB_ID="your_github_client_id"
    AUTH_GITHUB_SECRET="your_github_client_secret"
    AUTH_TRUST_HOST="http://localhost:3000"
    AUTH_SECRET="your_auth_secret"
    SENTRY_AUTH_TOKEN="your_sentry_auth_token"
   ```
4. **Sanity Setup**
   ```bash
   cd sanity
   npx sanity deploy
   ```
5. **Run the development server**
   ```bash
   npm run dev
   ```
   Visit [http://localhost:3000](http://localhost:3000)

---

## 📖 Usage

- **Sign in with GitHub** to access the platform
- **Submit a startup pitch** with title, description, and media
- **Browse and search** the live directory
- **View and manage** your own pitches in your profile
- **Admins** can curate and highlight top ideas

---

## 📞 Contact

- **GitHub**: [@Hrishubh](https://github.com/Hrishubh)
- **LinkedIn**: [Hrishubh Bhandari](https://www.linkedin.com/in/hrishubh-bhandari/)
- **Email**: bhandarihrishubh@gmail.com

---

<div align="center">

**⭐ Star this repository if you found it helpful!**

Made with ❤️ by Hrishubh Bhandari

</div>