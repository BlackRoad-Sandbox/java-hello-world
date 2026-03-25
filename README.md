<!-- BlackRoad SEO Enhanced -->

# java hello world

> Part of **[BlackRoad OS](https://blackroad.io)** — Sovereign Computing for Everyone

[![BlackRoad OS](https://img.shields.io/badge/BlackRoad-OS-ff1d6c?style=for-the-badge)](https://blackroad.io)
[![BlackRoad Sandbox](https://img.shields.io/badge/Org-BlackRoad-Sandbox-2979ff?style=for-the-badge)](https://github.com/BlackRoad-Sandbox)
[![License](https://img.shields.io/badge/License-Proprietary-f5a623?style=for-the-badge)](LICENSE)

**java hello world** is part of the **BlackRoad OS** ecosystem — a sovereign, distributed operating system built on edge computing, local AI, and mesh networking by **BlackRoad OS, Inc.**

## About BlackRoad OS

BlackRoad OS is a sovereign computing platform that runs AI locally on your own hardware. No cloud dependencies. No API keys. No surveillance. Built by [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc), a Delaware C-Corp founded in 2025.

### Key Features
- **Local AI** — Run LLMs on Raspberry Pi, Hailo-8, and commodity hardware
- **Mesh Networking** — WireGuard VPN, NATS pub/sub, peer-to-peer communication
- **Edge Computing** — 52 TOPS of AI acceleration across a Pi fleet
- **Self-Hosted Everything** — Git, DNS, storage, CI/CD, chat — all sovereign
- **Zero Cloud Dependencies** — Your data stays on your hardware

### The BlackRoad Ecosystem
| Organization | Focus |
|---|---|
| [BlackRoad OS](https://github.com/BlackRoad-OS) | Core platform and applications |
| [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc) | Corporate and enterprise |
| [BlackRoad AI](https://github.com/BlackRoad-AI) | Artificial intelligence and ML |
| [BlackRoad Hardware](https://github.com/BlackRoad-Hardware) | Edge hardware and IoT |
| [BlackRoad Security](https://github.com/BlackRoad-Security) | Cybersecurity and auditing |
| [BlackRoad Quantum](https://github.com/BlackRoad-Quantum) | Quantum computing research |
| [BlackRoad Agents](https://github.com/BlackRoad-Agents) | Autonomous AI agents |
| [BlackRoad Network](https://github.com/BlackRoad-Network) | Mesh and distributed networking |
| [BlackRoad Education](https://github.com/BlackRoad-Education) | Learning and tutoring platforms |
| [BlackRoad Labs](https://github.com/BlackRoad-Labs) | Research and experiments |
| [BlackRoad Cloud](https://github.com/BlackRoad-Cloud) | Self-hosted cloud infrastructure |
| [BlackRoad Forge](https://github.com/BlackRoad-Forge) | Developer tools and utilities |

### Links
- **Website**: [blackroad.io](https://blackroad.io)
- **Documentation**: [docs.blackroad.io](https://docs.blackroad.io)
- **Chat**: [chat.blackroad.io](https://chat.blackroad.io)
- **Search**: [search.blackroad.io](https://search.blackroad.io)

---


**Live at:** https://java.blackroad.io

A Java 17 HTTP server running on Raspberry Pi 5, exposed to the internet via Cloudflare Tunnel.

## Architecture

```
Internet → java.blackroad.io 
         → Cloudflare Edge 
         → Cloudflared Tunnel 
         → Pi 192.168.4.38:80 (nginx) 
         → localhost:8888 (Java HttpServer)
```

## Features

- Dynamic timestamps (updates every request)
- BlackRoad Design System colors
- Auto-start via systemd
- Zero-config deployment

## Files

- `HelloWorld.java` - Java HTTP server with embedded HTML
- `java-hello.service` - systemd service unit
- `nginx.conf` - nginx reverse proxy configuration
- `index.html` - Static preview page

## Deploy

```bash
# SSH to Pi
ssh pi@192.168.4.38

# Edit code
vi ~/java-hello/HelloWorld.java

# Recompile
javac HelloWorld.java

# Restart
sudo systemctl restart java-hello

# Done! Takes ~2 seconds
```

## Stack

- **Runtime:** Java 17 (OpenJDK)
- **Server:** com.sun.net.httpserver.HttpServer
- **Proxy:** nginx
- **Tunnel:** cloudflared
- **Host:** Raspberry Pi 5

---

🖤 Part of [BlackRoad OS](https://github.com/BlackRoad-OS)
