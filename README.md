<div align="center">

# 🔐 ConnectX

### Secure. Private. Connected.

**An Android-first secure messaging application built with end-to-end encryption, offline-first messaging, multi-device support, secure media sharing, voice messaging, and more.**

<p>
  <a href="#-features">Features</a> •
  <a href="#-screenshots">Screenshots</a> •
  <a href="#-download">Download</a> •
  <a href="#-installation">Installation</a> •
  <a href="#-project-status">Status</a>
</p>

<br>

![ConnectX](https://img.shields.io/badge/ConnectX-Android%20Messaging-7C4DFF?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active%20Development-orange?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge)
![Security](https://img.shields.io/badge/Security-End--to--End%20Encrypted-blue?style=for-the-badge)

</div>

---

## 📱 About ConnectX

**ConnectX** is an Android-first secure messaging application designed around privacy, reliability, offline-first behavior, and modern messaging experiences.

The project focuses on building a messaging system where security and reliability are part of the architecture rather than features added later.

ConnectX currently supports secure messaging, media sharing, voice messages, offline messaging, message search, multi-device usage, notifications, message lifecycle management, and other modern messaging capabilities.

> 🚧 **ConnectX is currently in active development.**
>
> The APKs provided through this repository are development builds intended for testing, demonstration, and feedback. Features and UI may continue to evolve.

---

# ✨ Features

## 💬 Messaging

- Text messaging
- Message editing
- Message forwarding
- Message search
- Global message search
- Starred messages
- Delivery status
- Read receipts
- Offline messaging
- Automatic synchronization
- Message lifecycle handling

---

## 🔐 Security & Privacy

ConnectX is designed around an end-to-end encrypted messaging architecture.

Key security principles include:

- End-to-end encrypted messaging
- Device-based identity
- Secure device lifecycle
- Encrypted media handling
- Account isolation
- Secure local storage
- Encrypted message history
- Secure recovery architecture
- Anti-downgrade protections
- Device/session validation

Sensitive cryptographic operations are intentionally separated from normal UI and feature development so that new functionality does not unnecessarily modify the security layer.

---

## 📱 Multi-Device

ConnectX is designed to support multiple devices for the same account.

The architecture includes:

- Device identity
- Device registration
- Device bundles
- Device lifecycle management
- Secure session establishment
- Device replacement handling
- Stale-device protection
- Multi-device message delivery

---

## 📴 Offline-First

ConnectX is designed to remain useful even when the network is unavailable.

Supported behavior includes:

- Offline message composition
- Durable outgoing messages
- Offline media sending
- Background synchronization
- Automatic retry
- Local-first message access
- Network-aware synchronization

Messages created while offline can remain pending until connectivity is restored.

---

# 🖼️ Media

ConnectX supports multiple types of media.

### 📷 Images

- Image sharing
- Image grids
- Full-screen image viewing
- Secure media handling
- Image-specific actions

### 🎬 Videos

- Video sharing
- Secure media delivery
- Video playback
- Media-specific UI

### 📄 Documents

Support for common document/file formats including:

- PDF
- DOC / DOCX
- XLS / XLSX
- PPT / PPTX
- TXT
- CSV
- ZIP
- and other supported formats

### 🎤 Voice Messages

ConnectX includes a dedicated voice messaging experience:

- Voice recording
- Pause / resume recording
- Voice waveform
- Voice message bubbles
- Playback
- Play / pause
- Playback progress
- Voice message duration
- Offline voice sending
- Secure voice media handling
- Background playback support

Voice messages are represented semantically as **voice messages** in the UI rather than exposing their underlying media transport implementation.

---

# 🔎 Search

ConnectX provides message discovery through:

- Chat-level search
- Global message search
- Local encrypted message history
- Search across available conversations

Search is designed to work with the local encrypted message history while respecting account isolation.

---

# 🔔 Notifications

ConnectX supports messaging notifications with account-aware handling.

The notification system is designed to work with:

- Background message delivery
- Push notifications
- Offline catch-up
- Account-scoped notification state
- Notification cleanup on logout

---

# 👥 Connections

ConnectX uses username-based discovery rather than relying on phone numbers or device contacts.

The Connections experience supports:

- Global connection discovery
- Online/offline behavior
- Existing conversations
- Connection search
- Profile information
- Account-aware relationship handling

---

# 📍 Location Sharing

ConnectX supports location messaging with secure message delivery and dedicated location handling.

The location experience is being further refined as development continues.

---

# 🎨 User Experience

ConnectX focuses on a clean modern messaging experience.

Current UI work includes:

- Smooth message transitions
- Context-aware scrolling
- Media grids
- Voice message animations
- Loading states
- Offline states
- Responsive layouts
- Accessibility support
- Modern empty states
- Account-aware UI
- Multi-device UX

The interface is continuously refined during development.

---

# 🏗️ Architecture

ConnectX uses a layered architecture designed to keep security, persistence, synchronization, and UI concerns separated.

High-level structure:

```text
                    ┌─────────────────────┐
                    │      Android UI     │
                    │   Jetpack Compose   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    ViewModels /     │
                    │    UI State         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Repository / Domain │
                    │      Layer          │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              ▼                ▼                ▼
       ┌─────────────┐ ┌─────────────┐ ┌─────────────┐
       │ Local Store │ │ Sync /      │ │ Secure      │
       │ Room /      │ │ Outbox      │ │ Media       │
       │ SQLCipher   │ │             │ │ Pipeline    │
       └─────────────┘ └─────────────┘ └─────────────┘
              │                │                │
              └────────────────┼────────────────┘
                               ▼
                    ┌─────────────────────┐
                    │   Spring Boot API   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │       MySQL         │
                    └─────────────────────┘