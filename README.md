<div align="center">

# 🔐 ConnectX

### Secure. Private. Connected.

**An Android-first secure messaging application built with end-to-end encryption, multi-device support, secure media sharing, and voice messaging, with calling, group chats, offline messaging, and file sharing on the way.**

<br>

![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active%20Development-orange?style=for-the-badge)
![Security](https://img.shields.io/badge/Security-End--to--End%20Encrypted-2563EB?style=for-the-badge&logo=letsencrypt&logoColor=white)
![Updates](https://img.shields.io/badge/Updates-Frequent-7C4DFF?style=for-the-badge)

<br>

[Download](#-download) • [Features](#-features) • [Roadmap](#-roadmap) • [Architecture](#-architecture) • [Installation](#-installation) • [Contact](#-contact)

</div>

<br>

---

<!-- ===================== DOWNLOAD BLOCK ===================== -->

<div align="center">

## 📦 Download

<table>
<tr>
<td align="center" width="620">

<br>

### ⬇️ Get ConnectX for Android

**Latest development build • Free for testers & early users**

<br>

<a href="https://github.com/vamsi-0609/ConnectX-App/releases/download/V0.1.0/ConnectX-App-release.apk">
  <img src="https://img.shields.io/badge/⬇_DOWNLOAD_APK-7C4DFF?style=for-the-badge&logo=android&logoColor=white" alt="Download APK" height="52">
</a>

<br><br>

<a href="https://github.com/YOUR_USERNAME/ConnectX/releases">
  <img src="https://img.shields.io/badge/All_Releases-6D28D9?style=for-the-badge&logo=github&logoColor=white" alt="All Releases">
</a>

<br><br>

| 📱 Requires | 🏷️ Version | 📥 Type |
|:---:|:---:|:---:|
| Android 8.0+ | 2.0 | Development APK |

<sub>🚧 ConnectX is under active development. Try it, use it, and check back often: new updates are released frequently.</sub>

<br>

</td>
</tr>
</table>

</div>

<br>

### 🚀 Getting Started

```text
  Download APK
       ↓
  Install ConnectX
       ↓
  Create Account / Sign In
       ↓
  Set Your Username
       ↓
  Find Your Connections
       ↓
  Start Messaging
```

---

## 📱 About ConnectX

**ConnectX** is an Android-first secure messaging application designed around privacy, reliability, and modern messaging experiences.

The project treats security as part of the **architecture**, not a feature added later. Every new capability, including calling and group chats, is being planned with a secure-by-design approach.

> 🚧 **ConnectX is in active development.**
> The APKs in this repository are development builds for testing, demonstration, and feedback. Features and UI will keep evolving, and updates ship frequently.

<br>

<div align="center">

<table>
<tr>
<td align="center" width="33%">

### 🔐 Private by Design
End-to-end encrypted messaging with account-aware and device-aware security.

</td>
<td align="center" width="33%">

### 📱 One Account, Many Devices
Device identity, secure sessions, and multi-device message delivery.

</td>
<td align="center" width="33%">

### 🚀 Always Improving
Active development with frequent updates and a growing roadmap.

</td>
</tr>
</table>

<table>
<tr>
<td align="center" width="25%">

### 💬 Message
Text, editing, forwarding, search, and read receipts.

</td>
<td align="center" width="25%">

### 🖼️ Share
Images, videos, and voice messages.

</td>
<td align="center" width="25%">

### 🎤 Talk
Record, send, and play encrypted voice messages.

</td>
<td align="center" width="25%">

### 👥 Connect
Find people by their ConnectX username and start chatting.

</td>
</tr>
</table>

</div>

---

## ✨ Features

### 💬 Messaging

- Text messaging, editing, and forwarding
- Chat-level and global message search
- Starred messages
- Delivery status and read receipts
- Message lifecycle handling

### 🔐 Security & Privacy

ConnectX is built on an end-to-end encrypted messaging architecture.

- End-to-end encrypted messaging
- Device-based identity
- Secure device lifecycle
- Encrypted media handling
- Account isolation
- Secure local storage and encrypted message history
- Secure recovery architecture
- Anti-downgrade protections
- Device and session validation

> Sensitive cryptographic operations are intentionally separated from normal UI and feature development, so new functionality doesn't unnecessarily touch the security layer.

### 📱 Multi-Device

- Device identity and registration
- Device bundles
- Device lifecycle management
- Secure session establishment
- Device replacement handling
- Stale-device protection
- Multi-device message delivery

### 🖼️ Media

| Type | Capabilities |
|:---|:---|
| 📷 **Images** | Sharing, image grids, full-screen viewing, secure handling, image-specific actions |
| 🎬 **Videos** | Sharing, secure delivery, playback, media-specific UI |
| 🎤 **Voice** | Recording with pause/resume, waveform, playback progress, duration, background playback |

Voice messages appear as **voice messages** in the UI, without exposing the underlying media transport.

### 🔎 Search

- Chat-level search
- Global message search
- Search across available conversations
- Works on local encrypted history while respecting account isolation

### 🔔 Notifications

- Background message delivery and push notifications
- Account-scoped notification state
- Notification cleanup on logout

### 👥 Connections

ConnectX uses **username-based discovery** instead of phone numbers or device contacts.

- Global connection discovery
- Connection search and existing conversations
- Profile information
- Account-aware relationship handling

### 📍 Location Sharing

Static location sharing with secure message delivery.

### 🎨 User Experience

- Smooth message transitions and context-aware scrolling
- Media grids and voice message animations
- Loading and empty states
- Responsive layouts and accessibility support
- Account-aware and multi-device UX

### 🐞 Feedback & Bug Reports

Found a bug or have a suggestion? You can send it directly from the app:

**Profile → Settings → User Feedback**

---

## 🗺️ Roadmap

ConnectX is actively growing. Here's what's coming.

| Feature | Status |
|:---|:---:|
| 📴 **Offline messaging** (major update) | 🔜 Coming next |
| 📄 **File sharing**: PDF, DOC/DOCX, XLS/XLSX, PPT/PPTX, TXT, CSV, ZIP and more (major update) | 🔜 Coming next |
| 📞 **Voice & video calling** | 🛠️ In development |
| 👥 **Group chats** | 🛠️ In development |
| 🔐 **Secure architecture for calls & groups** | 🧭 Being planned |

> 🔒 Calling and group chats are being designed with security first, so they meet the same privacy standards as the rest of ConnectX before release.

---

## 🏗️ Architecture

ConnectX uses a layered architecture that keeps security, persistence, synchronization, and UI concerns separate.

```text
                 ┌─────────────────────┐
                 │     Android UI      │
                 │   Jetpack Compose   │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │    ViewModels /     │
                 │      UI State       │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Repository / Domain │
                 │        Layer        │
                 └──────────┬──────────┘
                            │
           ┌────────────────┼────────────────┐
           ▼                ▼                ▼
    ┌─────────────┐  ┌─────────────┐  ┌─────────────┐
    │ Local Store │  │  Sync /     │  │  Secure     │
    │ Room /      │  │  Outbox     │  │  Media      │
    │ SQLCipher   │  │             │  │  Pipeline   │
    └──────┬──────┘  └──────┬──────┘  └──────┬──────┘
           │                │                │
           └────────────────┼────────────────┘
                            ▼
                 ┌─────────────────────┐
                 │   Spring Boot API   │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │        MySQL        │
                 └─────────────────────┘
```

### 🧰 Tech Stack

| Layer | Technology |
|:---|:---|
| **UI** | Kotlin, Jetpack Compose |
| **State** | ViewModels, UI State |
| **Local Storage** | Room, SQLCipher |
| **Sync** | Outbox pattern |
| **Backend** | Spring Boot |
| **Database** | MySQL |

---

## 🛠️ Installation

1. **Download** the latest APK from the [Download](#-download) section or the [Releases](https://github.com/YOUR_USERNAME/ConnectX/releases) page.
2. On your Android device, allow installs from your browser or file manager (**Settings → Install unknown apps**).
3. Open the downloaded APK and tap **Install**.
4. Launch **ConnectX**, create an account or sign in, and choose your username.
5. Search for a friend's username and start your first conversation.

> 💡 If Play Protect shows a warning, that's expected for development builds distributed outside the Play Store.

---

## 📊 Project Status

| Area | Status |
|:---|:---:|
| Secure messaging | ✅ Available |
| Images, videos & voice messages | ✅ Available |
| Search & notifications | ✅ Available |
| Multi-device support | ✅ Available |
| Static location sharing | ✅ Available |
| Offline messaging | 🔜 Coming next |
| File sharing | 🔜 Coming next |
| Calling | 🛠️ In development |
| Group chats | 🛠️ In development |
| Play Store release | 🧭 Planned |

---

<!-- ===================== CONTACT BLOCK ===================== -->

<div align="center">

## 📬 Contact

<table>
<tr>
<td align="center" width="620">

<br>

### 👋 Let's Connect

**Questions, feedback, or collaboration ideas? I'd love to hear from you.**

<br>

<a href="mailto:vamsib0609@gmail.com">
  <img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
</a>
&nbsp;
<a href="https://www.linkedin.com/in/vamsi-b-67a711259">
  <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
</a>
&nbsp;
<a href="https://github.com/vamsi-0609">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
</a>

<br><br>

**Vamsi krishna** • *Creator & Developer of ConnectX*

<br>

</td>
</tr>
</table>

<br>

<a href="#-connectx">
  <img src="https://img.shields.io/badge/⬆_Back_to_Top-7C4DFF?style=for-the-badge" alt="Back to Top">
</a>

<br><br>

<sub>Made with ❤️ for private, reliable messaging • © 2026 ConnectX</sub>

</div>
