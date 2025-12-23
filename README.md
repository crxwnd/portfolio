<!-- LUXURY NEON HEADER -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,25:161b22,50:7c3aed,75:06b6d4,100:0d1117&height=150&section=header&text=PORTFOLIO&fontSize=70&fontColor=ffffff&animation=twinkling&fontAlignY=40"/>

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=1000&color=06B6D4&center=true&vCenter=true&random=false&width=600&lines=Backend+Systems+%26+Production-Scale+Applications;Enterprise+Architecture+%7C+Real-Time+Systems"/>

<br>

[![GitHub](https://img.shields.io/badge/Back_to_Profile-0d1117?style=for-the-badge&logo=github&logoColor=7c3aed)](https://github.com/crxwnd)
[![Email](https://img.shields.io/badge/Contact_Me-0d1117?style=for-the-badge&logo=gmail&logoColor=06b6d4)](mailto:ravenot.oni@gmail.com)

</div>

<br>

<!-- ANIMATED LINE SEPARATOR -->
<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="100%">

<br>

<div align="center">

> **⚠️ Note:** These projects were developed under NDA for enterprise clients.
> Source code is confidential, but I'm sharing architecture decisions, technical challenges, and solutions.

</div>

<br>

<!-- ANIMATED LINE SEPARATOR -->
<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="100%">

<br>

<!-- PROJECT 1: DIGITAL SIGNAGE -->
<div align="center">

## <img src="https://raw.githubusercontent.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/main/GIF/Monitor.gif" width="40"/> &nbsp; Distributed Display Management Platform

<br>

<table>
<tr>
<td><b>🎯 Role</b></td>
<td>Lead Backend Developer</td>
</tr>
<tr>
<td><b>🏢 Industry</b></td>
<td>Hospitality / Enterprise</td>
</tr>
<tr>
<td><b>📊 Scale</b></td>
<td>100+ concurrent endpoints</td>
</tr>
<tr>
<td><b>📡 Status</b></td>
<td><img src="https://img.shields.io/badge/Production_Ready-06b6d4?style=flat-square"/></td>
</tr>
</table>

</div>

<br>

### 💡 The Challenge

Enterprise client needed centralized control over a large network of distributed display endpoints. Requirements included:

- **Real-time synchronization** across 100+ displays
- **Department-level access control** (different teams managing different screens)
- **High availability** for 24/7 operation
- **Media processing** for large video files (multi-TB storage)

<br>

### 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────────────────┐
│                        MANAGEMENT INTERFACE                              │
│                       (React + TypeScript)                               │
└────────────────────────────────┬────────────────────────────────────────┘
                                 │ REST + WebSocket
                                 ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                            CORE API                                      │
│                  (Node.js + Express + Socket.io)                         │
│                                                                          │
│   ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────────┐     │
│   │   Auth Service  │  │  Media Service  │  │    Sync Engine      │     │
│   │   (JWT/RBAC)    │  │  (Processing)   │  │ (Real-time Broadcast)│     │
│   └─────────────────┘  └─────────────────┘  └─────────────────────┘     │
└────────────────────────────────┬────────────────────────────────────────┘
                                 │
              ┌──────────────────┼──────────────────┐
              ▼                  ▼                  ▼
        ┌──────────┐       ┌──────────┐       ┌──────────┐
        │PostgreSQL│       │  Redis   │       │  Object  │
        │ (Prisma) │       │ (Cache)  │       │ Storage  │
        └──────────┘       └──────────┘       └──────────┘
                                 │
                                 ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                    DISTRIBUTED ENDPOINTS (100+)                          │
│                  (Web-based clients, always-on)                          │
└─────────────────────────────────────────────────────────────────────────┘
```

<br>

### 🛠️ Tech Stack

<div align="center">

| Layer | Technologies |
|:------|:-------------|
| **Frontend** | ![React](https://img.shields.io/badge/React_18-0d1117?style=flat-square&logo=react&logoColor=06b6d4) ![TypeScript](https://img.shields.io/badge/TypeScript-0d1117?style=flat-square&logo=typescript&logoColor=7c3aed) ![TailwindCSS](https://img.shields.io/badge/Tailwind-0d1117?style=flat-square&logo=tailwindcss&logoColor=06b6d4) ![Zustand](https://img.shields.io/badge/Zustand-0d1117?style=flat-square&logo=react&logoColor=7c3aed) |
| **Backend** | ![Node.js](https://img.shields.io/badge/Node.js-0d1117?style=flat-square&logo=nodedotjs&logoColor=06b6d4) ![Express](https://img.shields.io/badge/Express-0d1117?style=flat-square&logo=express&logoColor=7c3aed) ![Socket.io](https://img.shields.io/badge/Socket.io-0d1117?style=flat-square&logo=socketdotio&logoColor=06b6d4) ![Prisma](https://img.shields.io/badge/Prisma-0d1117?style=flat-square&logo=prisma&logoColor=7c3aed) |
| **Database** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL_16-0d1117?style=flat-square&logo=postgresql&logoColor=06b6d4) ![Redis](https://img.shields.io/badge/Redis-0d1117?style=flat-square&logo=redis&logoColor=7c3aed) |
| **Infrastructure** | ![Docker](https://img.shields.io/badge/Docker-0d1117?style=flat-square&logo=docker&logoColor=06b6d4) ![Nginx](https://img.shields.io/badge/Nginx-0d1117?style=flat-square&logo=nginx&logoColor=7c3aed) |
| **Security** | ![JWT](https://img.shields.io/badge/JWT-0d1117?style=flat-square&logo=jsonwebtokens&logoColor=06b6d4) ![RBAC](https://img.shields.io/badge/RBAC-0d1117?style=flat-square&logo=shield&logoColor=7c3aed) |

</div>

<br>

### ⚡ Technical Challenges & Solutions

<table>
<tr>
<td width="50%">

**🔴 Challenge**

Frame-perfect synchronization across 100+ displays on different network conditions

</td>
<td width="50%">

**🟢 Solution**

Server-side timestamp coordination with client drift correction. All endpoints request sync state on connection and adjust playback position accordingly.

</td>
</tr>
<tr>
<td>

**🔴 Challenge**

Handling 2-8TB of media files efficiently without blocking the main thread

</td>
<td>

**🟢 Solution**

Chunked uploads with resumability, lazy loading for previews, and background job queue (BullMQ) for video processing and thumbnail generation.

</td>
</tr>
<tr>
<td>

**🔴 Challenge**

Network reliability in a distributed environment with potential disconnections

</td>
<td>

**🟢 Solution**

Automatic reconnection with exponential backoff, local caching of current playlist state, and heartbeat monitoring to detect offline endpoints.

</td>
</tr>
<tr>
<td>

**🔴 Challenge**

Department-level isolation without compromising system-wide monitoring

</td>
<td>

**🟢 Solution**

RBAC implementation with granular permissions per endpoint group. Super admins see everything, department managers only see their assigned displays.

</td>
</tr>
</table>

<br>

<!-- ANIMATED LINE SEPARATOR -->
<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="100%">

<br>

<!-- PROJECT 2: FLEET ANALYTICS -->
<div align="center">

## <img src="https://raw.githubusercontent.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/main/GIF/Hot%20Flame.gif" width="40"/> &nbsp; Real-Time Fleet Analytics System

<br>

<table>
<tr>
<td><b>🎯 Role</b></td>
<td>Full Stack Developer</td>
</tr>
<tr>
<td><b>🏢 Industry</b></td>
<td>Hospitality / Logistics</td>
</tr>
<tr>
<td><b>📡 Status</b></td>
<td><img src="https://img.shields.io/badge/Delivered-06b6d4?style=flat-square"/></td>
</tr>
</table>

</div>

<br>

### 💡 The Challenge

Internal transportation service required visibility into vehicle positions and passenger metrics to:

- Optimize routes and reduce wait times
- Track vehicles in real-time
- Generate analytics for operational decisions
- Integrate with existing infrastructure

<br>

### 🏗️ Solution Overview

Real-time tracking module providing:

```
┌──────────────────┐     ┌──────────────────┐     ┌──────────────────┐
│   Mobile Units   │────▶│   API Gateway    │────▶│   Live Dashboard │
│  (GPS Tracking)  │     │  (Socket.io)     │     │   (React + Map)  │
└──────────────────┘     └────────┬─────────┘     └──────────────────┘
                                  │
                    ┌─────────────┴─────────────┐
                    ▼                           ▼
              ┌──────────┐               ┌──────────┐
              │  Redis   │               │ PostGIS  │
              │ (Buffer) │               │(Storage) │
              └──────────┘               └──────────┘
```

<br>

### 🛠️ Tech Stack

<div align="center">

| Component | Technology |
|:----------|:-----------|
| **Backend** | ![Node.js](https://img.shields.io/badge/Node.js-0d1117?style=flat-square&logo=nodedotjs&logoColor=06b6d4) ![TypeScript](https://img.shields.io/badge/TypeScript-0d1117?style=flat-square&logo=typescript&logoColor=7c3aed) ![Socket.io](https://img.shields.io/badge/Socket.io-0d1117?style=flat-square&logo=socketdotio&logoColor=06b6d4) |
| **Database** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0d1117?style=flat-square&logo=postgresql&logoColor=7c3aed) ![PostGIS](https://img.shields.io/badge/PostGIS-0d1117?style=flat-square&logo=postgresql&logoColor=06b6d4) |
| **Cache** | ![Redis](https://img.shields.io/badge/Redis-0d1117?style=flat-square&logo=redis&logoColor=7c3aed) |
| **Frontend** | ![React](https://img.shields.io/badge/React-0d1117?style=flat-square&logo=react&logoColor=06b6d4) ![Mapbox](https://img.shields.io/badge/Mapbox_GL-0d1117?style=flat-square&logo=mapbox&logoColor=7c3aed) |

</div>

<br>

### 📊 Results

- ✅ Real-time visibility into all active vehicles
- ✅ Historical data collection for route optimization
- ✅ Measurable reduction in average wait times
- ✅ Seamless integration with existing operations

<br>

<!-- ANIMATED LINE SEPARATOR -->
<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="100%">

<br>

<!-- PROJECT 3: MOBILE APP -->
<div align="center">

## <img src="https://raw.githubusercontent.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/main/GIF/Phone.gif" width="40"/> &nbsp; Mobile Logistics Application

<br>

<table>
<tr>
<td><b>🎯 Role</b></td>
<td>Mobile Developer</td>
</tr>
<tr>
<td><b>📱 Platform</b></td>
<td>Android (Native)</td>
</tr>
<tr>
<td><b>📡 Status</b></td>
<td><img src="https://img.shields.io/badge/In_Production-06b6d4?style=flat-square"/></td>
</tr>
</table>

</div>

<br>

### 💡 Overview

Native Android application for field operators, providing route management, status tracking, and real-time communication with dispatch.

<br>

### ✨ Key Features

<table>
<tr>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/🗺️-0d1117?style=for-the-badge"/>
<br><b>Navigation</b>
<br><sub>Turn-by-turn guidance</sub>
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/📸-0d1117?style=for-the-badge"/>
<br><b>Documentation</b>
<br><sub>Photo proof of delivery</sub>
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/📴-0d1117?style=for-the-badge"/>
<br><b>Offline-First</b>
<br><sub>Works without connection</sub>
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/🔔-0d1117?style=for-the-badge"/>
<br><b>Push Notifications</b>
<br><sub>Real-time assignments</sub>
</td>
</tr>
</table>

<br>

### 🛠️ Tech Stack

<div align="center">

| Component | Technology |
|:----------|:-----------|
| **Language** | ![Kotlin](https://img.shields.io/badge/Kotlin-0d1117?style=flat-square&logo=kotlin&logoColor=7c3aed) |
| **Architecture** | ![MVVM](https://img.shields.io/badge/MVVM-0d1117?style=flat-square&logo=android&logoColor=06b6d4) ![Clean Architecture](https://img.shields.io/badge/Clean_Architecture-0d1117?style=flat-square&logo=android&logoColor=7c3aed) |
| **Networking** | ![Retrofit](https://img.shields.io/badge/Retrofit-0d1117?style=flat-square&logo=square&logoColor=06b6d4) ![OkHttp](https://img.shields.io/badge/OkHttp-0d1117?style=flat-square&logo=square&logoColor=7c3aed) |
| **Local Storage** | ![Room](https://img.shields.io/badge/Room_DB-0d1117?style=flat-square&logo=sqlite&logoColor=06b6d4) |
| **Maps** | ![Google Maps](https://img.shields.io/badge/Google_Maps_SDK-0d1117?style=flat-square&logo=googlemaps&logoColor=7c3aed) |

</div>

<br>

<!-- ANIMATED LINE SEPARATOR -->
<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="100%">

<br>

<!-- INFRASTRUCTURE EXPERIENCE -->
<div align="center">

## <img src="https://raw.githubusercontent.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/main/GIF/Developer%20Desk.gif" width="40"/> &nbsp; Infrastructure Experience

</div>

<br>

Beyond application development, I have hands-on experience with:

```yaml
Containerization:
  - Docker multi-stage builds for optimized images
  - Docker Compose orchestration for multi-service deployments
  - Container networking & volume management

Networking:
  - Cisco switch configuration (SF110, SG500 series)
  - VLAN segmentation for network isolation
  - PoE management for IP cameras & VoIP
  - Structured cabling installation

Server Administration:
  - Linux server management
  - Windows Server & Active Directory
  - User provisioning & permission management
  - Group Policy configuration

Version Control:
  - Git workflows (feature branching, rebasing)
  - GitHub for collaboration
  - CI/CD fundamentals with GitHub Actions
```

<br>

<!-- ANIMATED LINE SEPARATOR -->
<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="100%">

<br>

<!-- CONTACT SECTION -->
<div align="center">

## <img src="https://raw.githubusercontent.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/main/GIF/Contact.gif" width="40"/> &nbsp; Let's Talk

<br>

*Interested in working together or discussing these projects in more detail?*

<br>

[![Email](https://img.shields.io/badge/ravenot.oni@gmail.com-0d1117?style=for-the-badge&logo=gmail&logoColor=7c3aed)](mailto:ravenot.oni@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0d1117?style=for-the-badge&logo=linkedin&logoColor=06b6d4)](https://linkedin.com/in/janick-etorres)
[![GitHub](https://img.shields.io/badge/GitHub-0d1117?style=for-the-badge&logo=github&logoColor=7c3aed)](https://github.com/crxwnd)

<br>

### 🇲🇽 Based in Mexico · Open to Remote Opportunities

<br>

<sub>Last updated: December 2024</sub>

</div>

<br>

<!-- FOOTER -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,25:161b22,50:7c3aed,75:06b6d4,100:0d1117&height=100&section=footer"/>
