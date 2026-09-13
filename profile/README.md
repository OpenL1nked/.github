<p align="center">
  <a href="https://github.com/OpenL1nked">
    <img width="160" alt="OpenL1nked logo" src="https://github.com/user-attachments/assets/6405da6e-fcd3-4ab9-a295-87ee91a687df" />
  </a>
</p>

<h1 align="center">OpenL1nked</h1>
<p align="center"><i>Unifying your digital life, open-source.</i></p>

<p align="center">
  <a href="https://openl1nked.site">Website</a> ·
  <a href="https://github.com/OpenL1nked/openl1nked-Windows">Desktop App</a> ·
  <a href="https://github.com/OpenL1nked/scrcpy-wrapper">App Mirroring</a> ·
  <a href="#contributing">Contributing</a>
</p>

---

> **Status: concept and planning phase.** Development is just getting started, and we're
> looking for founding contributors — developers, designers, and documenters — as well as a
> small group of pre-alpha testers. Community channels (Discord, etc.) will be announced here
> once they're live; in the meantime, open an issue on any repository to get involved.

## About

**OpenL1nked** is an open-source project to build a cross-platform bridge between desktop and
mobile devices — the functionality of tools like Phone Link or KDE Connect, built entirely on
open standards, with no proprietary lock-in.

The goal is a secure, fast, and feature-rich way to link your devices, whether they're on the
same network or connected remotely over the internet.

### Why OpenL1nked?

| | |
|---|---|
| **Cross-platform** | Desktop clients for Windows, macOS, and Linux; mobile for Android, with limited iOS support planned. |
| **Open source** | Transparent, community-driven development under the MIT License — no telemetry, no vendor lock-in. |
| **Feature-rich** | App mirroring, notification sync, file transfer, shared clipboard, messaging, and remote desktop control. |
| **Privacy-first** | End-to-end encryption across all communication channels. |
| **Works anywhere** | Local connections over Wi-Fi, with a self-hostable relay server for connectivity over mobile data. |
| **Modern stack** | Rust and Tauri power a lightweight, fast, and secure desktop client. |

## Proposed technology stack

| Component | Technology |
|---|---|
| Desktop app | [Tauri](https://tauri.app/) (Rust backend, web frontend) |
| Mobile app (Android) | [Kotlin](https://kotlinlang.org/), inspired by [KDE Connect](https://kdeconnect.kde.org/)'s architecture |
| Device protocol | [KDE Connect Protocol](https://github.com/KDE/kdeconnect-kde/blob/master/README.md) (end-to-end encrypted) |
| Remote connectivity | Custom WebSocket relay server (Rust/Node.js) |
| App mirroring | Approach inspired by [scrcpy](https://github.com/Genymobile/scrcpy) |

## Repositories

| Repository | Description |
|---|---|
| [`openl1nked-Windows`](https://github.com/OpenL1nked/openl1nked-Windows) | The desktop client — device discovery, KDE Connect pairing, and the devices dashboard UI. |
| [`scrcpy-wrapper`](https://github.com/OpenL1nked/scrcpy-wrapper) | Desktop wrapper around scrcpy for high-performance Android screen mirroring. |
| [`openl1nked.com`](https://github.com/OpenL1nked/openl1nked.com) | Source for the project website. |

## Roadmap

- **Phase 1 — Foundation & LAN connectivity**: Tauri desktop project structure, KDE Connect
  device discovery and pairing over UDP/TLS, and a foundational Android app connecting reliably
  over the local network.
- **Phase 2 — Remote connectivity**: A privacy-focused WebSocket relay server with automatic
  LAN-to-relay fallback, keeping all relayed traffic end-to-end encrypted.
- **Phase 3 — Core features & messaging**: Notification sync, shared clipboard, file transfer,
  and full SMS/MMS/RCS messaging support.
- **Phase 4 — High-bandwidth features & polish**: High-performance app mirroring, remote desktop
  controls, full macOS/Linux clients, a limited iOS client, and comprehensive documentation and
  CI/CD.

Each repository tracks its own detailed progress; this roadmap reflects the project's overall
direction.

## Contributing

OpenL1nked is a 100% volunteer-driven, open-source project. We are not funded and cannot offer
payment for contributions — we're building this for the community, with the community.

Whether you're an experienced developer, a UI/UX designer, or a documentation contributor,
there's room to help shape the project from the ground up. To get started:

1. Browse the [repositories](#repositories) above and check open issues for a good first task.
2. Open an issue to discuss significant changes before starting work.
3. Submit a pull request — each repository's README has its own setup and development
   instructions.

## License

OpenL1nked projects are published under the [MIT License](https://github.com/OpenL1nked/scrcpy-wrapper/blob/main/LICENSE).

---

<p align="center"><i>OpenL1nked: Unlink from the proprietary, link to the open.</i></p>
