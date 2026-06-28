# Tyes Ubuntu Homelab 

A self-hosted, homelab environment deployed on a dedicated Ubuntu Linux laptop. This project serves as a production-style testing ground for container orchestration, localized networking, and automated IoT systems.

## Architecture & Tech Stack
* **Operating System:** Ubuntu Linux (Headless CLI)
* **Container Setup:** Docker & Portainer
* **Applications:** Home Assistant
* **Protocols:** MQTT, Zigbee, IPv4 DHCP/Static Routing

---

## System Blueprint & Deployment

### 1. Host OS & Resource Management
The underlying host runs a lightweight Ubuntu environment optimized for 24/7 uptime. Power-saving features (like laptop lid suspension sleep) are disabled to ensure continuous service availability.

### 2. Containerization (Docker + Portainer)
All application services are containerized to ensure complete environment isolation, portability, and security. 
* Managed exclusively via **Portainer UI** for real-time log analysis and container lifecycle states.
* Isolated network bridges prevent unauthorized cross-container communication.

### 3. Home Assistant
Acting as the central event engine, Home Assistant aggregates telemetric data from 20+ smart devices.
* **Automation-as-Code:** Custom routines are written using structured YAML configurations.
* **Integrations:** Connected via third-party web APIs and local hardware dongles.

---

## Access + Controls
* **Secure Shell (SSH):** Configured for remote server acsess and management.
* **Local Firewall (UFW):** Strict ingress rules implemented; only essential service ports (e.g., 22 for SSH, 8123 for Home Assistant, 9000 for Portainer) are exposed locally.

---

## Notes
* **Uptime:** Maintained a stable environment with proactive log monitoring.
* **Efficiency:** Reduced overall compute overhead by replacing heavy VM architecture with lightweight Docker containers.

---
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
