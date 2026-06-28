# Tyes Ubuntu Homelab 

A self-hosted, homelab environment deployed on a dedicated Ubuntu Linux laptop.
---
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black) ![Jellyfin](https://img.shields.io/badge/jellyfin-%23000B25.svg?style=for-the-badge&logo=Jellyfin&logoColor=00A4DC) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Home Assistant](https://img.shields.io/badge/home%20assistant-%2341BDF5.svg?style=for-the-badge&logo=home-assistant&logoColor=white) ![Pi-Hole](https://img.shields.io/badge/pihole-%2396060C.svg?style=for-the-badge&logo=pi-hole&logoColor=white)
---

##Hardware
<img

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
