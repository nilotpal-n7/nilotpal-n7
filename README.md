<div align="center">
  <h1>Nilotpal Gupta</h1>
  <p><strong>Systems & Software Engineer | Security Researcher | Hardware Designer</strong></p>
  <p>Computer Science & Engineering (Major) • Minor in Mathematics • Indian Institute of Technology Guwahati</p>
  <p><em>Projects Head, Coding Club IIT Guwahati</em></p>

  <p>
    <a href="https://linkedin.com/in/nilotpal-n7"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
    <a href="https://github.com/nilotpal-n7"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" /></a>
    <a href="mailto:nilotpalgupta0701@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
    <a href="https://instagram.com/nil7.xeno"><img src="https://img.shields.io/badge/Instagram-E4405F?style=flat-square&logo=instagram&logoColor=white" alt="Instagram" /></a>
  </p>
</div>

---

### 📌 Overview

I design and build across the full computing stack: from **binary reverse engineering, VM deobfuscation, and high-speed PCB design** to **compiler internals, distributed systems, and on-device machine learning architectures**.

---

### 🛠️ Technical Arsenal

| Domain | Technologies, Frameworks & Protocols |
| :--- | :--- |
| **Languages** | C, C++, Rust, Python, Go, TypeScript, JavaScript, Dart, Verilog, x86-64 / ARM Assembly |
| **Security & Reverse Engineering** | IDA Pro, Ghidra, x64dbg, Intel Pin (DBI), Unicorn Engine, Capstone, Z3 SMT, Claripy, Wireshark, TLS 1.3, PE Internals |
| **Hardware & Embedded** | Altium Designer (High-Speed Multi-Layer PCB), ESP32 (FreeRTOS / PlatformIO), RISC-V ISA, I2C, SPI, I2S, UART, BLE (NimBLE) |
| **Distributed Systems & Backend** | Rust (Axum), Node.js, Express, FastAPI, Redis, PostgreSQL, MongoDB, Qdrant (Vector DB), Memgraph (Graph DB), Docker |
| **Edge AI & Application Dev** | PyTorch, ONNX Runtime, Chaquopy, HuggingFace, Tree-sitter, Flutter, React, Next.js, TailwindCSS |

---

### 🔬 Featured Systems & Engineering Work

#### 🛡️ Program Analysis, Security & Reverse Engineering

* **[GameSecLab & REAForge](https://github.com/nilotpal-n7/GameSecLab)**  
  *Automated binary analysis framework, VMProtect 3.11 & Themida devirtualizer, and anti-tamper laboratory.*
  * **Taint-Symbolic Execution:** Developed a custom symbolic engine using `claripy` and `z3` modeling x86-64 semantics, MBA transforms (`vNAND`/`vNOR`), and EFLAGS to mathematically recover virtualized algorithms without path explosion.
  * **Commercial Protector Deobfuscation:** Emulated execution pipelines via `Unicorn` to unpack VMProtect 3.11 Ultra and Themida targets, bypassing RDTSC timing constraints, `KUSER_SHARED_DATA` checks, direct syscalls, and self-checksum integrity loops.
  * **SMT Formal Equivalence:** Automated loop unrolling and sub-expression anti-unification in Z3, verifying bit-level algorithmic equivalence over all $2^{32}$ input spaces for protected game binaries (*Dead Cells* HashLink runtime).

* **[Cross-Platform Security Lab & Telemetry Suite](https://github.com/nilotpal-n7/reverse_shell)**  
  *Multi-platform administration, forensics, and steganography laboratory across Linux, Windows, and Android (Termux).*
  * **Secure Communications:** Engineered a custom TLS 1.3 telemetry server featuring line-delimited JSON and HMAC-SHA256 challenge-response mutual authentication.
  * **Defensive Forensics:** Built runtime inspection tools for live process trees, socket-to-PID correlation, and Shannon entropy analysis for executable anomalies.
  * **Data Hiding:** Implemented LSB steganographic encoders for PNG image streams and non-rendering PDF comment/attachment structures.

---

#### 💻 Compilers, Computer Architecture & Core Open Source

* **[rust-lang/rust](https://github.com/rust-lang/rust)**  
  *Upstream Contributor to the Rust Programming Language Compiler.*
  * Resolved AST span issues and diagnostic rendering errors within `rustc` and `compiletest` to enhance compiler feedback clarity.
  * Completed internal codebase refactors to align compiler diagnostics with updated internal APIs while upholding strict memory safety guarantees.

* **[High-Performance 5-Stage RISC-V Processor](https://github.com/nilotpal-n7/riscv)**  
  *Pipelined 32-bit RISC-V (RV32I) microarchitecture implemented in Verilog.*
  * Designed a classic 5-stage execution pipeline: Fetch, Decode, Execute, Memory, and Writeback.
  * Implemented hazard detection, branch stall logic, and direct data-forwarding paths to eliminate pipeline stalls and maximize Instructions Per Cycle (IPC).

---

#### ⚡ Hardware Engineering & Embedded Systems

* **[AuthKey-ESP32](https://github.com/nilotpal-n7/auth-esp32)**  
  *Hardware security key (FIDO2 / Passkeys / TOTP) with multi-transport authentication.*
  * **FIDO2 / WebAuthn:** Implemented full CTAP 2.0 specifications over BLE, virtual USB HID (via `usbip-win2`), and hybrid QR signaling channels (caBLE v2 / Noise KNpsk0).
  * **Host Integration:** Designed a Windows DPAPI background service enabling cryptographic walk-away screen locking and zero-touch HMAC-SHA256 challenge-response authentication.
  * **Firmware & Security:** Features an SSD1306 OLED interface, physical button approvals, AES-256-GCM encrypted backup/restore, and background campus network keep-alives.

* **[Nano-D1: RISC-V Single Board Computer](https://github.com/nilotpal-n7/NanoD1)**  
  *Custom 66 × 38 mm 4-layer RISC-V SBC designed in Altium Designer.*
  * Built around the Sophgo SG2002 SoC (C906 @ 1 GHz / Cortex-A53 with 256 MB in-package SIP DDR3).
  * Engineered a complete power tree (0.95V Core @ 2A, 1.8V LDO, 1.35V DDR3L, and PWR_SEQ2-gated 3.3V) with impedance-controlled routing (DIFF90 USB, SE50 antenna, 0.35 mm pitch QFN88 escape).
  * Integrated dedicated digital I2S audio interfaces (MAX98357A amplifier and INMP441 MEMS microphone) alongside an AP6212 Wi-Fi module.

---

#### 🚀 Distributed Systems, RAG & Edge AI

* **[Ruskit: Polyglot Codebase RAG](https://github.com/nilotpal-n7/ruskit)**  
  *High-throughput code knowledge graph and retrieval-augmented generation engine.*
  * **Core Architecture:** Built an asynchronous Rust core using `Axum` and WebSockets, routing to a `Qdrant` vector database (768-dim embeddings) and `Memgraph` for AST traversal.
  * **Parsing Pipeline:** Ingests syntax trees across 12+ programming languages using `tree-sitter` and incorporates an active 24-hour Redis semantic cache to reduce query latency.
  * **Terminal Interface:** Developed a native `Ratatui` terminal UI supporting voice I/O, automated secret scrubbing, and an agentic 4-iteration reasoning loop.

* **[CreekUI (Inter-IIT Adobe PS)](https://github.com/nilotpal-n7/creek-ui)**  
  *On-device edge AI engine for interactive sketch-to-image synthesis.*
  * Built an asynchronous mobile ML pipeline utilizing Chaquopy and ONNX Runtime (<30 ms composition analysis, ~500 ms BiRefNet segmentation).
  * Deployed quantized diffusion and vision-language models (Flux, Stable Diffusion, Florence-2) optimized for low-VRAM (<4 GB) edge environments.

* **[HABit Campus Infrastructure](https://github.com/nilotpal-n7/HABit)**  
  *Unified campus management platform serving 8,000+ active students and administrators at IIT Guwahati.*
  * Engineered a versioned microservices API gateway (`Express 5`) orchestrating services across PostgreSQL, MongoDB, and Redis.
  * Automated Dockerized CI/CD pipelines managing end-to-end multi-platform client releases across web and mobile platforms.

---

<div align="center">
  <sub>"Oh, Death... Become my blade, once more"</sub>
</div>
