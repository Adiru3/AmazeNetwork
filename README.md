# Amaze Network 🚀

<img width="355" height="196" alt="image" src="https://github.com/user-attachments/assets/ce216002-82c7-4de6-8d8f-76747a29293e" />

**Amaze Network** is a high-performance system utility written in C#, designed for deep optimization of the Windows network stack and CPU resource management in real-time. It is specifically engineered for gamers and power users looking to minimize latency (ping) and maximize system responsiveness.

---

## 🛠 Core Features

The engine operates across five distinct system layers to ensure peak performance:

### 1. Hardware Level Optimization
* **Direct Cache Access (DCA) & NetDMA:** Enables direct cache access to reduce CPU overhead during network packet processing.
* **RSS (Receive Side Scaling):** Enables scaling to distribute network traffic processing across multiple CPU cores.
* **Interrupt Moderation:** Disables network adapter interrupt moderation globally via PowerShell to ensure instant packet handling.

### 2. Traffic & System Prioritization
* **Network Throttling Bypass:** Sets the `NetworkThrottlingIndex` to `0xFFFFFFFF` to disable Windows' built-in throttling for non-multimedia traffic.
* **System Responsiveness:** Adjusts the system profile to `0%` responsiveness to prioritize user tasks over background system services.
* **QoS DSCP Tagging:** Implements Quality of Service (QoS) policies to tag traffic with `DSCP 46` (High Priority), ensuring preferred routing.

### 3. Protocol Stack (TCP/IP Tweaks)
* **Disable Nagle's Algorithm:** Modifies `TcpAckFrequency` and `TCPNoDelay` in the registry to send small packets without delay.
* **TCP Fast Open (TFO):** Enables `Fast Open` to speed up the data exchange process during connection establishment.
* **UDP/TCP RSC Disable:** Disables Receive Segment Coalescing to reduce jitter in real-time applications.

### 4. Dynamic Process Optimization
The script continuously monitors the foreground window and applies specific optimizations to detected games:
* **CPU Affinity:** Automatically masks the process to exclude `Core 0`, preventing conflicts with system interrupts and OS tasks.
* **Process Priority:** Dynamically elevates the game process priority to `High`.

### 5. Deployment & Automation
* **Auto-Installer:** Automatically deploys itself to `Program Files\AmazeGaming` if executed from a different directory.
* **Persistence:** Utilizes Windows Task Scheduler (`schtasks`) to create a logon task with `HIGHEST` privileges.
* **Tray Integration:** Runs a system tray icon for background management, allowing users to toggle the debug console.

---

## 🚀 Getting Started

1. **Requirements:** .NET Framework and Windows 10/11.
2. **Permissions:** The application requires **Administrator** privileges to modify registry keys and network configurations; it will automatically prompt for elevation if needed.
3. **Usage:** Simply run the compiled `AmazeNetwork.exe`. Upon the first run, it will install itself and start the optimization loop.

### Command Line Arguments
* `-silent` — Launches the application directly to the system tray without showing the console window.

---

## ⚠️ Disclaimer
This utility makes significant changes to the Windows Registry and network interface configurations. It is intended for advanced users. Use it at your own risk.

---

## 🔗 Connect with me
[![YouTube](https://img.shields.io/badge/YouTube-@adiruaim-FF0000?style=for-the-badge&logo=youtube)](https://www.youtube.com/@adiruaim)
[![TikTok](https://img.shields.io/badge/TikTok-@adiruhs-000000?style=for-the-badge&logo=tiktok)](https://www.tiktok.com/@adiruhs)

### 💰 Legacy Crypto
* **BTC:** `bc1qflvetccw7vu59mq074hnvf03j02sjjf9t5dphl`
* **ETH:** `0xf35Afdf42C8bf1C3bF08862f573c2358461e697f`
* **Solana:** `5r2H3R2wXmA1JimpCypmoWLh8eGmdZA6VWjuit3AuBkq`
* **USDT (TRC20):** `TNgFjGzbGxztHDcSHx9DEPmQLxj2dWzozC`
* **USDT (TON):** `UQC5fsX4zON_FgW4I6iVrxVDtsVwrcOmqbjsYA4TrQh3aOvj`

### 🌍 Support Links
[![Donatello](https://img.shields.io/badge/Support-Donatello-orange?style=for-the-badge)](https://donatello.to/Adiru3)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-Support-blue?style=for-the-badge&logo=kofi)](https://ko-fi.com/adiru)
[![Steam](https://img.shields.io/badge/Steam-Trade-blue?style=for-the-badge&logo=steam)](https://steamcommunity.com/tradeoffer/new/?partner=1124211419&token=2utLCl48)
