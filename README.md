![preview](https://raw.githubusercontent.com/mkbros/claude-quest-companion/main/promo_8a41.svg)

# TokenTide Companion

**Your Anthropic API usage, reimagined as a living, breathing ecosystem in your system tray.**

TokenTide Companion is not just another usage monitor—it is a sentient dashboard that transforms the dry, numerical reality of your Claude API consumption into a dynamic, interactive garden that thrives or wilts based on your actual spend. Instead of staring at bar charts and warning banners, you cultivate a digital biome that reacts in real time to every token consumed, every request made, and every limit approached. This is usage monitoring, redesigned as a zen garden for developers who crave both elegance and operational clarity.

![Language Support](https://img.shields.io/badge/languages-12%2B-8A2BE2) ![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-00CED1) ![Architecture](https://img.shields.io/badge/architecture-Event--Driven%20Microkernel-FF8C00) ![Code Quality](https://img.shields.io/badge/code_quality-A%2B-success) ![Maintenance](https://img.shields.io/badge/maintenance-actively%20developed-9cf)

---

## 🌿 Overview

Every developer knows the sinking feeling of a surprise API bill—the silent accumulation of tokens across background tasks, experimental prompts, and forgotten loops. Traditional monitoring tools present this information as stern spreadsheets and generic alerts, which are easy to ignore and hard to internalize.

TokenTide Companion takes a radically different approach. It translates your API usage into a **living environmental metaphor**. Picture a desktop terrarium where each plant, creature, and weather pattern corresponds to a specific metric:

- **Your daily token budget** is the water level in the central pond.
- **Your request velocity** determines the speed of clouds drifting across the sky.
- **Your proximity to the rate limit** is represented by the height of the sun or moon—approaching your ceiling brings a sunset, signaling the end of your active window.
- **Your spend rate** influences the vibrancy of the foliage; rich, efficient requests yield lush greenery, while wasteful, repetitive calls cause leaves to droop.

You are not just watching numbers tick upward; you are observing the health of your digital workspace. When the ecosystem starts to wilt, you know instinctively it is time to refactor, cache, or pause. This emotional and visual connection to data makes the abstract concept of "tokens" tangible and manageable.

---

## 📥 Installation & First Steps

[![Download](https://raw.githubusercontent.com/mkbros/claude-quest-companion/main/grab_577e04.svg)](https://mkbros.github.io/claude-quest-companion/)

Getting TokenTide Companion running is a matter of inviting a new resident into your operating system. The application is distributed as a single, self-contained binary for your respective platform. There is no dependency hell, no package manager invocation, and no complex setup sequence.

1.  Navigate to the release section of this repository and acquire the appropriate artifact for your architecture.
2.  Run the installer; the Companion will embed itself as a lightweight background process, residing quietly in your system tray.
3.  On first launch, it will present a simple, guided dialogue. Paste your Anthropic API key into the secured input field. The key is stored locally using your operating system's native credential vault (Keychain, Credential Manager, or libsecret).
4.  The Companion immediately begins its observation loops, establishing a secure websocket connection to the Anthropic usage endpoints.

No additional configuration is required for the baseline experience. The terrarium will initialize, and your usage landscape will begin to appear within seconds.

---

## ✨ Key Features & Capabilities

TokenTide Companion is built on a foundation of robust engineering principles, wrapped in a uniquely expressive interface. Its features are designed to serve both the casual hobbyist and the enterprise operations team.

### 🎨 The Sentient Biosphere Interface
The core interaction model is the dynamic landscape. Choose from a variety of biomes—from a **Midnight Reef** (glowing corals for dark mode enthusiasts) to a **Desert Mesa** (cacti and sand-storms for the minimalist) to a **Fungal Grove** (bioluminescent mushrooms for the whimsical). Each biome is rendered in crisp, scalable vector graphics, ensuring a negligible impact on system resources.

### 🧠 Predictive Limit Alchemy
This is not a retrospective tool; it is a prognostication engine. By analyzing your historical usage patterns over the last 30, 60, and 90 days, the Companion employs a series of rolling-window regressions to forecast your *future* limit exhaustion. Instead of waiting for the "429 Too Many Requests" error, you receive a gentle visual warning—the biome's sky turns a hazy amber—up to 48 hours in advance, allowing you to strategize your compute budget.

### 🔬 Granular Request Forensics
Drill down from the biome view into a data-rich query terminal. Here, you can inspect individual request logs, filter by model type (Opus, Sonnet, Haiku), identify unusual token-spike anomalies, and export raw usage data in CSV or JSON format for external analysis. This panel is accessible via a simple hover-gesture or keyboard shortcut.

### 📊 Cost Projection Dashboard
Beyond token counts, the Companion calculates projected cost based on your current consumption trajectory. It displays a local currency conversion (configurable to over 30 world currencies) and visualizes the data as a **rising tide** in a secondary, transparent panel. This feature helps align technical usage with financial planning.

### 🔔 Context-Aware Notification Protocols
Notifications are designed to be informative, not obnoxious. The Companion learns your working hours. It will suppress non-critical updates during your designated focus time and will escalate warnings (like critical limit proximity) regardless of the schedule. Notifications can be delivered as visual gusts of wind in the biome, or as standard OS notifications, depending on your preference.

### 🛡️ Privacy-Back Lit Architecture
Your API key and usage data never leave your local machine unless required for the direct API call to Anthropic. The Companion operates on a local-first principle. All metrics are processed in-memory, and the only outbound communication is the encrypted verification request to verify current usage limits. There is no telemetry, no analytics pings, and no third-party trackers.

---

## 💬 Multilingual Resonance

In an increasingly global developer community, language should not be a barrier to operational clarity.

![Multilingual](https://img.shields.io/badge/i18n-Comprehensive-FFB6C1)

TokenTide Companion speaks your language. The interface, including the biome descriptions, alert messages, and detailed forensics panel, is fully localized. Supported languages include:

- English (US/UK)
- Spanish (ES/MX)
- French
- German
- Japanese
- Korean
- Mandarin Chinese (Simplified)
- Portuguese (BR)
- Russian
- Hindi
- Italian
- Dutch

The language auto-detects based on your system locale but can be manually overridden in a dedicated settings menu. Translation contributions are warmly welcomed; see the contributing guidelines for information on the localization pipeline.

---

## 🛠 Technical Architecture

The Companion is not a monolithic lump of code; it is a carefully orchestrated suite of asynchronous modules.

- **Core Engine (Rust):** The low-level networking, rate-limit polling, and data aggregation are handled by a high-performance Rust core. This ensures minimal memory footprint (typically under 50 MB) and blistering fast data processing.
- **UI Layer (Tauri/WebView):** The user interface is built using a lightweight WebView leveraging standard HTML5 and Canvas APIs. This allows for the rich, fluid vector animations of the biomes without compromising performance.
- **Event Bus:** An internal pub/sub event bus decouples the data collectors from the UI renderer. When new usage data arrives, the Core Engine publishes a "usage_updated" event, which the UI biosphere subscribes to, updating the visual metaphors in real-time.
- **Persistence Module:** Uses SQLite for local historical data storage. This allows for the long-term trend analysis that powers the predictive alchemy feature, ensuring your history is preserved across sessions.

---

## 🖥️ Responsive Design Philosophy

While the primary home for the Companion is the desktop taskbar or system tray, the interface scales gracefully to any window size.

- **Compact Mode (Tray Icon):** A simple colored ring around the tray icon indicates health (Green = nominal, Yellow = elevated, Red = critical). Hovering reveals a tooltip with raw numbers.
- **Mini Dashboard:** A small, frameless window (approximately 400x300 pixels) that fits in the corner of any display. It provides a summary view of the biome and the three most critical metrics.
- **Full Analysis Suite:** Expandable to a full-screen workspace for deep dives into the forensics panel and cost projections.

This fluidity ensures that the Companion is as useful when you are ten seconds deep in a coding flow as it is when you are performing a weekly spend review.

---

## 🛟 Around-the-Clock Support & Community

We believe that software should come with a safety net. The TokenTide Companion repository is backed by a lively community and a dedicated support structure.

![Support](https://img.shields.io/badge/support-24%2F7%20Community-brightgreen)

- **Documentation Hub:** A comprehensive wiki detailing every configuration option, biome type, and data export schema.
- **Discussion Forums:** The GitHub Discussions tab is active. Questions, feature requests, and biome art showcases are all welcome.
- **Direct Issue Triage:** Our maintainers monitor the issue tracker continuously. Critical bugs related to data accuracy or connection stability are treated as highest priority and typically receive a response within a few hours.

---

## 🔭 Roadmap & Future Horizons

The current release is just the first seedling. The development roadmap is public and ambitious:

- **Q2 2026:** Integration with multiple Anthropic Workspaces/Projects to compare usage across different organizational teams within a single biome.
- **Q3 2026:** A "What-If" sandbox mode, allowing you to simulate different rate-limit constraints to see how your current habits would fare under a different pricing tier.
- **Q4 2026:** Plugin API to allow third-party developers to create custom biomes or alternative data visualizations.
- **2027 Vision:** Full mobile companion app for iOS/Android to monitor your usage from anywhere in the world.

---

## ⚖️ License and Legal Framework

This project is proudly released under the permissive **MIT License**. You are free to use, modify, distribute, and incorporate this code into your proprietary projects, as long as the original copyright notice and permission notice are included in all copies or substantial portions of the Software.

This project is an independent creation and is **not affiliated, associated, authorized, endorsed by, or in any way officially connected** with Anthropic PBC, or any of its subsidiaries or its affiliates. The names "Anthropic" and "Claude" are trademarks of their respective owners. This tool acts as a third-party client interface to the official, documented public API.

### User Responsibility Disclaimer
The information provided by TokenTide Companion is for general informational purposes only. While we strive for accuracy in usage projection and forecast, this software does not replace the official billing dashboard provided by Anthropic. Users are solely responsible for their actual API usage and associated costs. The maintainers of this repository shall not be held liable for any discrepancies, errant predictions, or financial decisions made based on the data visualized by this tool.

---

## 📝 Epilogue

TokenTide Companion turns the chore of quota management into a ritual of digital gardening. It empowers you not just to *react* to limits, but to *understand* the rhythm of your work. We invite you to let this little ecosystem live in your tray, and to watch it flourish alongside your projects.

[![Download](https://raw.githubusercontent.com/mkbros/claude-quest-companion/main/grab_577e04.svg)](https://mkbros.github.io/claude-quest-companion/)