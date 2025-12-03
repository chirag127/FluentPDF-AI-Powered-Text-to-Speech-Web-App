# FluentPDF: AI-Powered Text-to-Speech Web Application

[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App/ci.yml?style=flat-square&label=Build)](https://github.com/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App?style=flat-square)](https://codecov.io/gh/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App)
[![Language](https://img.shields.io/github/languages/top/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App?style=flat-square&color=3A4E9A)](https://github.com/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App)
[![License](https://img.shields.io/github/license/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App?style=flat-square&color=FF6600)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App?style=flat-square)](https://github.com/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App)

<p align="center">
  <a href="https://github.com/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App">
    <img src="https://img.shields.io/badge/Star%20%E2%98%85%EF%B8%8F%20this%20Repo-blue?style=flat-square" alt="Star this Repo"/>
  </a>
</p>

--- 

**FluentPDF** is a cutting-edge web application engineered to bridge the accessibility gap by transforming static PDF documents into highly natural, context-aware spoken audio streams.
This system couples robust, high-performance PDF parsing with modern Text-to-Speech (TTS) synthesis, optimized for low-latency web delivery via WebAssembly modules.

## 📐 Architecture Overview

The application utilizes a modern micro-frontend approach, ensuring feature isolation and rapid iteration. Core document processing leverages WebAssembly (WASM) for near-native speed in the browser, offloading heavy computation from the main JavaScript thread.

mermaid
graph TD
    A[User Interface: React/Vite] --> B{Client-Side Parsing: PDF.js / WASM Module};
    B --> C[Extracted Text Content];
    C --> D{AI Orchestration Layer: Web Worker}; 
    D -- Sanitize & Contextualize --> E[Final Text Chunks];
    E --> F[Browser Native Web Speech API / External TTS Service];
    F --> G(High-Fidelity Audio Output);
    
    subgraph Backend Service (Optional)
        H[Metadata & History Storage]
    end
    
    D -. API Call .-> H


## 📚 Table of Contents
1.  [Key Features](#-key-features)
2.  [Technology Stack](#-technology-stack)
3.  [Development Workflow](#-development-workflow)
4.  [Contributing](#-contributing)
5.  [Agent Directives (System Context)](#-ai-agent-directives-system-context)

## ✨ Key Features

*   **High-Fidelity TTS:** Utilization of the latest Web Speech Synthesis voices for superior auditory experience.
*   **PDF Structure Awareness:** Intelligent parsing that respects document headings and section breaks for meaningful narration.
*   **Performance Critical:** Core logic containerized and optimized using **WebAssembly** for rapid processing.
*   **Accessibility First:** Designed to WCAG standards, providing high utility for visually impaired users.
*   **Type-Safe Development:** Built entirely in **TypeScript** for compile-time safety and long-term maintainability.

## 🚀 Technology Stack

| Category | Technologies |
| :--- | :--- |
| **Frontend** | React 19, TypeScript 5.x, Vite 5, Tailwind CSS v4 |
| **Core Logic** | WebAssembly (Rust/AssemblyScript compilation target) |
| **State Management**| Signals (Standardized) |
| **Testing** | Vitest (Unit/Integration), Playwright (E2E) |
| **Linting/Formatting**| Biome (Unified toolchain) |

## 🛠️ Development Workflow

This project adheres to the **Apex Development Principles** enforced by integrated CI/CD pipelines.

### Prerequisites
Ensure Node.js (v20+), npm/uv, and the required build tools are installed.

### Setup

bash
# 1. Clone the repository
git clone https://github.com/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App.git
cd FluentPDF-AI-Powered-Text-to-Speech-Web-App

# 2. Install Dependencies using uv (If applicable for backend/shared modules) or npm
npm install
# or:
uv sync


### Execution Scripts

| Command | Description |
| :--- | :--- |
| `npm run dev` | Start the Vite development server with Hot Module Replacement. |
| `npm run build` | Compile production-ready assets, including WASM bundling. |
| `npm test` | Run Vitest unit and component tests. |
| `npm run test:e2e` | Execute end-to-end scenarios using Playwright. |
| `npx @biomejs/biome check .` | Comprehensive linting and formatting check. |

### Core Principles

*   **SOLID:** Strict adherence to Single Responsibility and Interface Segregation principles in component design.
*   **DRY (Don't Repeat Yourself):** Abstract common parsing and speech-handling logic into reusable utility modules.
*   **YAGNI (You Ain't Gonna Need It):** Only implement features required for immediate high-value accessibility outcomes.

## 🤖 AI Agent Directives (System Context)

<details>
<summary><strong>APEX AGENT INSTRUCTIONS (DECEMBER 2025)</strong></summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context (`FluentPDF-AI-Powered-Text-to-Speech-Web-App`).
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs. Focus on browser/WASM capabilities first.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, especially regarding **Browser TTS Benchmarks**, **WASM Performance Gains**, and **Accessibility APIs**.
    *   **Validation:** Use `docfork` to verify *every* external API signature (e.g., Web Speech API constraints).
    *   **Reasoning:** Engage `clear-thought-two` to architect complex parsing/TTS synchronization flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type (Web/Frontend) and apply the corresponding **Apex Toolchain**.

*   **PRIMARY SCENARIO: WEB / APP / GUI (Modern Frontend)**
    *   **Stack:** **TypeScript (Strict)**, **Vite 7** (for bundling/HMR), **TailwindCSS v4** (Utility-first styling), **Tauri v2** (If native compilation is required, otherwise pure browser focus). Focus on **Client-Side Performance**.
    *   **Lint/Test:** **Biome** (Speed/Format) + **Vitest** (Unit) + **Playwright** (E2E).
    *   **Architecture:** Feature-Sliced Design (FSD) principles for component organization. Core focus on minimal main thread blocking.

## 4. VERIFICATION & GUARANTEES
*   **Type Safety:** All new TypeScript code must use `strict: true` settings.
*   **Performance Guardrail:** Any function handling PDF rendering or text segmentation must be benchmarked against the **500KB PDF Load Time Target (under 1.5 seconds)**.
*   **Code Review Standard:** All PRs must pass Biome checks and achieve **90%+** unit test coverage on modified modules.

</details>

## 🤝 Contributing

We welcome contributions that enhance performance, fidelity, or accessibility. Please adhere to the following professional standards:

1.  **Fork** the repository.
2.  Create a descriptive feature branch (e.g., `feat/improve-wasm-parser`).
3.  Ensure all new code passes Biome checks (`npx @biomejs/biome check --apply .`).
4.  Submit a Pull Request referencing any relevant issues.

Refer to the `.github/CONTRIBUTING.md` for detailed guidelines.

## 🛡️ Security

This project handles external file input. Security is paramount. All input sanitization against XSS vectors during text extraction and before passing to speech synthesis APIs is mandatory.

See `.github/SECURITY.md` for reporting vulnerabilities.
