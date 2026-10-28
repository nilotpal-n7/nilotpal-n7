# Hi there, I'm Nilotpal Gupta 👋

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/nilotpal-n7)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nilotpal-n7)
[![Codeforces](https://img.shields.io/badge/Codeforces-1683_(Expert)-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white)](https://codeforces.com/profile/nilotpal-n7)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:nilotpalgupta0701@gmail.com)

**Computer Science & Engineering** (Major) with a **Minor in Mathematics** at **IIT Guwahati** | **Projects Head**, Coding Club IITG.

I operate across the computing stack: from **binary reverse engineering, virtual machine devirtualization, and hardware PCB design** to **compiler internals, distributed campus backends, and edge AI engines**.

---

## 🛠️ Technical Arsenal

| Category | Technologies & Tools |
| :--- | :--- |
| **Languages** | C / C++, Rust, Python, Go, TypeScript, JavaScript, Dart, Verilog, x86-64 / ARM Assembly |
| **Reverse Engineering & Security** | IDA Pro, Ghidra, x64dbg, Intel Pin (DBI), Unicorn Engine, Capstone, Z3 SMT, Claripy, Wireshark, TLS 1.3, PE Internals |
| **Hardware & Embedded** | Altium Designer (4-Layer High-Speed PCB), ESP32 (FreeRTOS / PlatformIO), RISC-V ISA, I2C, SPI, I2S, UART, BLE (NimBLE) |
| **Distributed Systems & Backend** | Rust (Axum), Node.js, Express, FastAPI, Redis, PostgreSQL, MongoDB, Qdrant (Vector DB), Memgraph (Graph DB), Docker |
| **AI, Edge & App Development** | PyTorch, ONNX Runtime, Chaquopy, HuggingFace, Tree-sitter, Flutter, React, Next.js, TailwindCSS |

---

## 🔬 Featured Systems, Security & Hardware Projects

### 🛡️ Program Analysis, Security & Reverse Engineering

#### [GameSecLab & REAForge](https://github.com/nilotpal-n7/GameSecLab)
*Autonomous binary analysis framework, VMProtect 3.11 & Themida devirtualizer, and anti-tamper laboratory.*
* **Devirtualization Engine:** Built a custom taint-symbolic execution engine (`claripy` / `z3`) modeling x86-64 semantics, MBA transforms (`vNAND`/`vNOR`), and EFLAGS to symbolically recover hidden algorithms without path explosion.
* **Modern Protector Defeat:** Defeated VMProtect 3.11 Ultra and Themida via CPU emulation (`Unicorn` + `vmp-lazy-unpack`), bypassing RDTSC timing, KUSER_SHARED_DATA checks, direct syscalls, and self-checksumming.
* **SMT Formal Proofs:** Implemented round-peeling and anti-unification to prove mathematical equivalence of unrolled hash loops across all $2^{32}$ inputs in Z3. Validated on commercial runtimes (*Dead Cells* HashLink runtime `hl_hash_utf8`).

#### [Security Lab & Telemetry Suite](https://github.com/nilotpal-n7/reverse_shell)
*Cross-platform remote administration, forensics, and steganography laboratory across Linux, Windows, and Android (Termux).*
* Built an encrypted TLS 1.3 socket server with newline-delimited JSON and HMAC-SHA256 challenge-response mutual authentication.
* Implemented defensive inspection tools: live process hierarchy inspectors, open socket-to-PID observers, and Shannon entropy file-anomaly detectors.
* Engineered LSB steganography in PNG pixel matrices and inert PDF comment/attachment carriers.

---

### 💻 Compilers, Computer Architecture & Open Source

#### [rust-lang/rust](https://github.com/rust-lang/rust)
*Upstream Contributor to the Rust Programming Language Compiler.*
* Resolved diagnostic-error rendering and AST span issues in `rustc` and `compiletest` to enhance error messages for the global community.
* Executed internal codebase migrations aligning with updated core compiler APIs while strictly upholding memory safety guarantees.

#### [High-Performance 5-Stage RISC-V Processor](https://github.com/nilotpal-n7/riscv)
*Pipelined 32-bit RISC-V (RV32I) microarchitecture in Verilog.*
* Designed a standard 5-stage instruction pipeline: Fetch, Decode, Execute, Memory, and Writeback.
* Implemented hazard detection units, pipeline stall logic, and data forwarding paths to minimize stalls and maximize Instructions Per Cycle (IPC).

---

### ⚡ Hardware Design & Embedded Systems

#### [AuthKey-ESP32](https://github.com/nilotpal-n7/auth-esp32)
*Standalone hardware security key (FIDO2 / Passkeys / TOTP) with multi-transport Windows & Android integration.*
* **FIDO2 / WebAuthn:** Implemented CTAP 2.0 over Bluetooth Low Energy (BLE), USB (via `usbip-win2` virtual HID), and hybrid QR tunnels (caBLE v2 / Noise KNpsk0) without requiring a smartphone.
* **Platform Security:** Windows DPAPI-backed service providing cryptographic walk-away screen lock and zero-touch HMAC-SHA256 challenge-response unlock.
* **On-Device Hardware:** Runs on ESP32 with SSD1306 OLED, hardware PIN verification, AES-256-GCM encrypted backup/restore, and an automated background IITG campus network keep-alive daemon.

#### [Nano-D1: RISC-V Single Board Computer](https://github.com/nilotpal-n7/NanoD1)
*Custom 66 × 38 mm 4-layer learning-grade RISC-V SBC designed in Altium Designer.*
* Engineered around the Sophgo SG2002 SoC (C906 @ 1 GHz / Cortex-A53 + 256 MB in-package SIP DDR3).
* Designed power tree sequencing (0.95V Core @ 2A, 1.8V LDO, 1.35V DDR3L, and PWR_SEQ2-gated 3.3V) with clean impedance-matched routing (DIFF90 USB, SE50 antenna, QFN88 0.35mm pitch escape).
* Integrated on-board digital I2S audio architecture (MAX98357A amplifier and INMP441 MEMS microphone) and AP6212 Wi-Fi.

---

### 🚀 Distributed Systems, RAG & Edge AI

#### [Ruskit: Polyglot Codebase RAG](https://github.com/nilotpal-n7/ruskit)
*High-throughput code knowledge graph and retrieval-augmented generation engine.*
* **Multi-Service Architecture:** Rust core (`Axum`) with WebSocket telemetry, integrated with `Qdrant` (768-dim embeddings) and `Memgraph` for AST code graph traversal.
* Ingests syntax trees across 12+ programming languages using `tree-sitter` and incorporates a 24-hour Redis semantic cache to slash LLM API latency.
* Interactive `Ratatui` terminal user interface (TUI) with real-time voice I/O, secret scrubbing, and an agentic 4-iteration reasoning loop.

#### [CreekUI (Inter-IIT Adobe PS)](https://github.com/nilotpal-n7/creek-ui)
*Edge AI image composition and on-device neural synthesis platform.*
* Engineered an asynchronous on-device ML pipeline running under Chaquopy / ONNX (<30ms composition analysis, ~500ms BiRefNet segmentation).
* Served quantized diffusion and vision-language models (Flux, Stable Diffusion, Florence-2) optimized for low-VRAM (<4GB) real-time sketch-to-image synthesis.

#### [HABit Campus Infrastructure](https://github.com/nilotpal-n7/HABit)
*Unified campus management platform serving 8,000+ students and administrators at IIT Guwahati.*
* Engineered a versioned microservices API gateway (`Express 5`) routing traffic to distinct services backed by PostgreSQL, MongoDB, and Redis.
* Containerized multi-environment Docker deployment pipelines powering 7 production clients across Web and mobile (App Store / Google Play).

---

## 📈 Competitive Programming & Academics

* **Codeforces:** [Expert](https://codeforces.com/profile/nilotpal-n7) (Peak Rating: **1683**)
* **LeetCode:** [nilotpal-n7](https://leetcode.com/u/nilotpal-n7/)
* **Academics:** B.Tech Major in Computer Science & Engineering, Minor in Mathematics at **IIT Guwahati**
* **Leadership:** Projects Head, **Coding Club IIT Guwahati**

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=nilotpal-n7&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="Nilotpal's GitHub Stats" />
</p>

---
<p align="center">
  <i>"Oh, Death... Become my blade, once more"</i>
</p>
