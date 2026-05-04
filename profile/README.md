<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=600&size=14&pause=1000&color=7BB8D4&center=true&vCenter=true&width=600&lines=Open-Source+Embedded+Systems+Community;ARM+Cortex-M4+%C2%B7+FreeRTOS+%C2%B7+AUTOSAR;From+Concept+to+Production+Release" alt="Typing SVG" />

```
  ╔══════════════════════════════════════════════════════╗
  ║                                                      ║
  ║   SS { Electronics }                                 ║
  ║                                                      ║
  ║   Reliable · Scalable · Developer-Friendly           ║
  ║   Open-Source Embedded Systems Frameworks            ║
  ║                                                      ║
  ╚══════════════════════════════════════════════════════╝
```

[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Platform](https://img.shields.io/badge/platform-ARM%20Cortex--M4-orange.svg)](https://github.com/SS-Electronics)
[![RTOS](https://img.shields.io/badge/RTOS-FreeRTOS-green.svg)](https://github.com/SS-Electronics/FreeRTOS-OS)
[![Language](https://img.shields.io/badge/language-C-blue.svg)](https://github.com/SS-Electronics)
[![MISRA](https://img.shields.io/badge/MISRA-C%3A2012-red.svg)](https://github.com/SS-Electronics/FreeRTOS-OS)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](https://github.com/SS-Electronics)

---

![FreeRTOS-OS](https://img.shields.io/github/stars/SS-Electronics/FreeRTOS-OS?style=social)
![Re-BOOT](https://img.shields.io/github/stars/SS-Electronics/Re-BOOT?style=social)
![Re-BOOT-Web](https://img.shields.io/github/stars/SS-Electronics/Re-BOOT-Web?style=social)
![PCAN-View-Linux](https://img.shields.io/github/stars/SS-Electronics/PCAN-View-Linux?style=social)
![ECG_DL](https://img.shields.io/github/stars/SS-Electronics/ECG_DL?style=social)

</div>

---

## 👋 Welcome to SS Electronics

We are an open-source community committed to creating **reliable, scalable, and developer-friendly** solutions in the domain of embedded systems.

---

## 🔭 Our Vision

We envision a future where embedded development is no longer slowed down by repetitive infrastructure work. By building an open, collaborative ecosystem of reusable frameworks and tools, we empower developers to focus entirely on what matters — **innovation at the application level**. As the community grows and contributes, embedded development becomes faster, more reliable, and accessible to engineers at every level.

---

## 🎯 Our Mission

Our mission is to design and maintain **production-grade foundational software** that:

- ⚡ Enables **rapid prototyping** — from blank MCU to running application in hours, not weeks
- 🔄 Streamlines the **concept-to-production** path with battle-tested, modular frameworks
- 🧩 Fosters **code reusability** — write once, deploy across projects, boards, and platforms
- 🔬 Upholds **software quality** — MISRA compliance, static analysis, and CI-driven testing from day one

---

## 🛠️ What We Build

### 🖥️ Embedded OS & Kernel Development
A production-ready OS layer built on top of popular kernels (FreeRTOS, ThreadX) that provides drivers, communication stacks, and service thread architectures — so teams can skip the boilerplate and **start directly on application logic**. Supports everything from learning kernels to production firmware releases on ARM Cortex-M.

### ☁️ Optimized OTA & Remote Update
A secure, transport-agnostic firmware update framework supporting Serial, TCP, UDP, and CAN — with a browser-based management portal. Designed for **delta-efficient** image transfers and multi-node fleet management on constrained embedded targets.

### 🤖 Autonomous Testing Framework
A complete SIL (Software-in-the-Loop) test infrastructure: test bed, firmware stubs, and Python scripts that run **continuous automated validation** without requiring physical hardware. Built for CI/CD integration and regression-free development cycles.

---

---

## 📂 Featured Projects

---

### 🖥️ [FreeRTOS-OS](https://github.com/SS-Electronics/FreeRTOS-OS)

[![Stars](https://img.shields.io/github/stars/SS-Electronics/FreeRTOS-OS?style=flat-square)](https://github.com/SS-Electronics/FreeRTOS-OS/stargazers)
[![Issues](https://img.shields.io/github/issues/SS-Electronics/FreeRTOS-OS?style=flat-square)](https://github.com/SS-Electronics/FreeRTOS-OS/issues)
[![Last Commit](https://img.shields.io/github/last-commit/SS-Electronics/FreeRTOS-OS?style=flat-square)](https://github.com/SS-Electronics/FreeRTOS-OS/commits)
[![License](https://img.shields.io/github/license/SS-Electronics/FreeRTOS-OS?style=flat-square)](https://github.com/SS-Electronics/FreeRTOS-OS/blob/main/LICENSE)

A structured, **Linux-inspired OS layer** built on top of FreeRTOS for ARM Cortex-M4 embedded targets. Provides thread management, IPC message queues, a hardware abstraction layer, service threads, and an interactive UART shell — all sitting above FreeRTOS without replacing it.

**Highlights:**
- Linux-style thread lifecycle API and intrusive linked-list memory management
- Service thread architecture: UART, I2C, SPI, GPIO managed via IPC queues
- Kconfig + XML-driven board/IRQ code generators
- Interactive shell over UART (FreeRTOS+CLI, 115200 8N1)
- MISRA C:2012 static analysis + GitHub Actions CI

> **Default target:** STM32F411VET6 · ARM Cortex-M4F · 100 MHz · 512 KB Flash · 128 KB RAM

```bash
make menuconfig && make config-outputs && make board-gen && make irq_gen
make app && make flash-app
picocom -b 115200 --echo /dev/ttyUSB0
```

---

### ☁️ [Re-BOOT](https://github.com/SS-Electronics/Re-BOOT)

[![Stars](https://img.shields.io/github/stars/SS-Electronics/Re-BOOT?style=flat-square)](https://github.com/SS-Electronics/Re-BOOT/stargazers)
[![Issues](https://img.shields.io/github/issues/SS-Electronics/Re-BOOT?style=flat-square)](https://github.com/SS-Electronics/Re-BOOT/issues)
[![Last Commit](https://img.shields.io/github/last-commit/SS-Electronics/Re-BOOT?style=flat-square)](https://github.com/SS-Electronics/Re-BOOT/commits)
[![License](https://img.shields.io/github/license/SS-Electronics/Re-BOOT?style=flat-square)](https://github.com/SS-Electronics/Re-BOOT/blob/main/LICENSE)

A **cross-platform host-side firmware update utility** that transfers Intel HEX images to an embedded target over Serial (UART), TCP, UDP, or CAN — using a lightweight, event-driven bootloader protocol with CRC32 verification.

**Highlights:**
- Multi-transport: Serial, TCP, UDP, CAN (USB-CAN virtual COM)
- Sector-aligned HEX pipeline with per-sector CRC32 verification
- Node ID routing — multiple targets sharing the same bus
- Event-driven FSM with configurable retry logic
- Builds on Linux and Windows (MinGW-w64 cross-compile)

```bash
./re-boot -f firmware.hex -n 1 -c serial -i /dev/ttyACM0   # UART
./re-boot -f firmware.hex -n 1 -c tcp -i 192.168.1.100 -p 5000  # TCP
./re-boot -f firmware.hex -n 1 -c can -i /dev/ttyUSB0      # CAN
```

---

### 🌐 [Re-BOOT-Web](https://github.com/SS-Electronics/Re-BOOT-Web)

[![Stars](https://img.shields.io/github/stars/SS-Electronics/Re-BOOT-Web?style=flat-square)](https://github.com/SS-Electronics/Re-BOOT-Web/stargazers)
[![Issues](https://img.shields.io/github/issues/SS-Electronics/Re-BOOT-Web?style=flat-square)](https://github.com/SS-Electronics/Re-BOOT-Web/issues)
[![Last Commit](https://img.shields.io/github/last-commit/SS-Electronics/Re-BOOT-Web?style=flat-square)](https://github.com/SS-Electronics/Re-BOOT-Web/commits)
[![License](https://img.shields.io/github/license/SS-Electronics/Re-BOOT-Web?style=flat-square)](https://github.com/SS-Electronics/Re-BOOT-Web/blob/main/LICENSE)

A **lightweight C web server** for remotely flashing embedded firmware via Re-BOOT. Runs on a Raspberry Pi as a Jenkins-style OTA portal — no Python, no Node.js, no heavy runtime.

**Highlights:**
- Upload Intel HEX files and configure flash jobs from the browser
- Live log streaming via Server-Sent Events (SSE) — watch flash progress in real time
- Multi-user login with role-based access (admin / user)
- SQLite3 job history with status, timestamps, and exit codes
- Nginx reverse proxy support with optional HTTPS (self-signed cert)

```bash
make && ./reboot-web          # starts on 0.0.0.0:5000
# or as a systemd service on Raspberry Pi
sudo systemctl enable reboot-web && sudo systemctl start reboot-web
```

---

### 📡 [PCAN-View-Linux](https://github.com/SS-Electronics/PCAN-View-Linux)

[![Stars](https://img.shields.io/github/stars/SS-Electronics/PCAN-View-Linux?style=flat-square)](https://github.com/SS-Electronics/PCAN-View-Linux/stargazers)
[![Issues](https://img.shields.io/github/issues/SS-Electronics/PCAN-View-Linux?style=flat-square)](https://github.com/SS-Electronics/PCAN-View-Linux/issues)
[![Last Commit](https://img.shields.io/github/last-commit/SS-Electronics/PCAN-View-Linux?style=flat-square)](https://github.com/SS-Electronics/PCAN-View-Linux/commits)
[![License](https://img.shields.io/github/license/SS-Electronics/PCAN-View-Linux?style=flat-square)](https://github.com/SS-Electronics/PCAN-View-Linux/blob/main/LICENSE)

An **open-source CAN bus monitor and analyser for Linux**, inspired by PEAK-System PCAN-View. Uses the Linux SocketCAN subsystem (`PF_CAN / SOCK_RAW`) with a GTK 3 GUI featuring real-time tracing, message transmission, bus-load metering, and CSV recording.

**Highlights:**
- CAN 2.0 A/B and CAN FD support (10 kbit/s – 12 Mbit/s)
- Real-time trace: sequence #, direction, timestamp, ID, DLC, data
- Live bus-load bar, error frame highlighting, message deduplication
- One-shot and cyclic message transmit
- Works with virtual CAN (`vcan0`) for off-hardware testing
- Pluggable driver vtable — easy to add new CAN back-ends

```bash
sudo modprobe vcan && sudo ip link add dev vcan0 type vcan && sudo ip link set up vcan0
make && ./pcan-view
# File > Connect → select vcan0 → Connect
cansend vcan0 123#DEADBEEF   # send a test frame
```

---

### 🧠 [ECG_DL](https://github.com/SS-Electronics/ECG_DL)

[![Stars](https://img.shields.io/github/stars/SS-Electronics/ECG_DL?style=flat-square)](https://github.com/SS-Electronics/ECG_DL/stargazers)
[![Issues](https://img.shields.io/github/issues/SS-Electronics/ECG_DL?style=flat-square)](https://github.com/SS-Electronics/ECG_DL/issues)
[![Last Commit](https://img.shields.io/github/last-commit/SS-Electronics/ECG_DL?style=flat-square)](https://github.com/SS-Electronics/ECG_DL/commits)
[![License](https://img.shields.io/github/license/SS-Electronics/ECG_DL?style=flat-square)](https://github.com/SS-Electronics/ECG_DL/blob/main/LICENSE)

A **modular MATLAB deep learning framework** for training and evaluating CNN models on ECG data from the PTB Database for cardiac disease classification. Supports multiple architectures, automated pipelines, and composable signal processing.

**Highlights:**
- Multi-model training: CNN1D and ResNet-inspired ECG classifier
- `TrainingOrchestrator` manages end-to-end training, checkpointing, and evaluation
- Composable `AlgorithmPipeline` for preprocessing (normalize, filter, denoise, augment)
- Classifies 6 conditions: Normal, MI, LBBB, RBBB, Sinus Bradycardia, Atrial Fibrillation
- PTB Database integration, train/val split, early stopping, model comparison tools

> **Requires:** MATLAB R2023b or later · PTB Database

---

## 🤝 How to Contribute

1. **Fork** the repository you'd like to contribute to
2. **Branch** — `git checkout -b feature/my-feature`
3. **Commit** — clear, descriptive messages
4. **Pull Request** — open a PR, join the discussion

All repositories are licensed under **GNU GPL v3** (unless otherwise stated).

---

<div align="center">

**[github.com/SS-Electronics](https://github.com/SS-Electronics)**

*Open Source · GPL v3 · subhajitroy005@gmail.com*

</div>
