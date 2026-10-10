# HunarShakti
# HunarShakti (हुनरशक्ति) 🧵⚡

> **Voice-First AI & Fintech Infrastructure for Rural Skill Aggregation & Income Generation**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: TRL-4 Prototype](https://img.shields.io/badge/TRL--4-Functional%20Prototype-blue.svg)](#technology-readiness-level-trl-roadmap)
[![TechFEST 2026](https://img.shields.io/badge/Event-TechFEST%202026%20SLIET-orange.svg)]()
[![Stack: FastAPI + pgvector](https://img.shields.io/badge/Backend-FastAPI%20%7C%20PostgreSQL--pgvector-green.svg)](#system-architecture--tech-stack)

**HunarShakti** is an end-to-end engineered software solution designed to bridge the digital and economic gap for rural Indian women artisans. By replacing traditional text-heavy job boards with a **Voice-First Dialect Pipeline (BHASHINI)**, **Computer Vision Quality Grading (YOLOv8)**, **Vector Similarity Matchmaking (pgvector)**, and **Biometric Settlement (AEPS)**, HunarShakti connects informal micro-artisans directly with enterprise B2B demand while eliminating middleman exploitation.

---

## 🌟 Key Highlights

* **🎙️ Dialect Voice-First Onboarding:** Speech-driven intake removing literacy barriers by converting spoken audio into normalized skill vectors.
* **👁️ YOLOv8 Edge Computer Vision Scoring:** Automated inspection calculating thread density, edge symmetry, and defect indices from raw product photos.
* **📐 pgvector Cosine Similarity Engine:** High-dimensional vector matching matching open B2B enterprise bulk orders with artisan capacity in milliseconds.
* **💳 AEPS Biometric Escrow Settlement:** Direct Aadhaar-linked wallet releases triggering cash payouts upon buyer verification or scan confirmation.
* **📱 Offline-First PWA Resilience:** Local SQLite and WebM/Opus low-bitrate caching allowing seamless usage in low-connectivity rural zones.

---

## 🏗️ System Architecture & Tech Stack

```mermaid
flowchart TD
    subgraph Client [Edge Layer / PWA]
        A[Rural Artisan] -->|Voice Input Opus 16kbps| B[PWA Service-Worker / Local SQLite]
        A -->|Camera Capture| B
    end

    subgraph Pipeline [Data & ML Pipeline]
        B -->|Voice Stream| C[BHASHINI Speech-to-Speech Engine]
        B -->|Image Payload| D[YOLOv8 Edge Computer Vision]
        C -->|Skill Embedding 128d| E[FastAPI Core Server]
        D -->|Quality Score Qi| E
    end

    subgraph Backend [Persistence & Matchmaking]
        E -->|Vector Store Query| F[(PostgreSQL + pgvector)]
        F -->|Cosine Similarity Search| G[Enterprise Buyer Match Engine]
    end

    subgraph Fintech [Settlement Layer]
        G -->|Order Confirmed| H[AEPS / UPI Biometric Escrow Middleware]
        H -->|Milestone Released| I[Aadhaar Wallet Disbursement]
    end
