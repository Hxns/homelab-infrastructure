<div align="center">
  <h1>🌌 Mi Homelab Infrastructure 🌌</h1>
  <p><i>Entorno centralizado para la experimentación, el despliegue de servicios y el aprendizaje continuo en ciberseguridad.</i></p>
  <p><i>A centralized environment for experimentation, service deployment, and continuous learning in cybersecurity.</i></p>

  [![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)](#)
  [![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](#)
  [![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)](#)
  [![Network](https://img.shields.io/badge/Network-000000?style=for-the-badge&logo=ubiquiti&logoColor=white)](#)
</div>

---

## 🗺️ Arquitectura de Red / Network Architecture

La infraestructura está diseñada para garantizar estabilidad, segmentación y rendimiento óptimo de todos los servicios. El diagrama muestra la topología general: interconexión de dispositivos, enrutamiento y distribución de servicios en la red local.

*The infrastructure is designed to ensure stability, segmentation, and optimal performance across all services. The diagram below shows the overall topology: device interconnection, routing, and service distribution across the local network.*

<div align="center">
  <img src="img/Diagrama.png" alt="Diagrama de Arquitectura del Homelab" width="800px">
</div>

> **Nota / Note:** El diagrama ilustra el flujo de red, los nodos principales y la segmentación de VLANs, facilitando una comprensión rápida del aislamiento y la conectividad entre servicios y dispositivos físicos. / *The diagram illustrates network flow, main nodes, and VLAN segmentation, enabling a quick understanding of isolation and connectivity between services and physical devices.*

---

## 💻 Hardware del Homelab / Homelab Hardware

El entorno de cómputo se distribuye en cuatro máquinas, cada una con un rol específico dentro de la red: virtualización, servicios de infraestructura, operaciones defensivas y operaciones ofensivas.

*The computing environment is distributed across four machines, each with a specific role in the network: virtualization, infrastructure services, defensive operations, and offensive operations.*

<br>

### 🖥️ Ordenador 1: Mini PC HP T620

Actúa como hipervisor principal. Su función es distribuir los recursos físicos (CPU, RAM, almacenamiento) para crear, alojar y gestionar de forma aislada todas las máquinas virtuales que conforman la red de víctimas.

*Acts as the primary hypervisor. Its role is to allocate physical resources (CPU, RAM, storage) to create, host, and manage all virtual machines that make up the victim network in isolation.*

<div align="center">
  <img src="img/Ordenador-1.jpeg" alt="Ordenador 1 — Mini PC HP T620" width="400px" style="border-radius: 10px; box-shadow: 0px 4px 10px rgba(0,0,0,0.5);">
</div>

#### 🛠️ Especificaciones Técnicas / Technical Specifications
| Componente / Component | Detalle / Detail |
| :--- | :--- |
| **Procesador (CPU)** | `AMD Ryzen Embedded R1305G` |
| **Memoria RAM** | `8 GB DDR4` |
| **Almacenamiento** | `250 GB SSD` |
| **Rol / Sistema Operativo** | `Proxmox VE` |

<br>

### 🖥️ Ordenador 2: Raspberry Pi 4 B

Actúa como anfitrión de servicios críticos de infraestructura de red: filtrado de DNS a nivel de red y sensores de detección de intrusos (IDS), manteniéndolos operativos de forma continua y con bajo consumo energético.

*Acts as the host for critical network infrastructure services: network-level DNS filtering and intrusion detection sensors (IDS), keeping them running continuously with low power consumption.*

#### 🛠️ Especificaciones Técnicas / Technical Specifications
| Componente / Component | Detalle / Detail |
| :--- | :--- |
| **Procesador (CPU)** | `ARM Cortex-A72` |
| **Memoria RAM** | `4 GB LPDDR4` |
| **Almacenamiento** | `64 GB MicroSD` |
| **Rol / Sistema Operativo** | `Raspberry Pi OS Lite` |

<br>

### 🖥️ Ordenador 3: ASUS — Old Model

Actúa como estación de operaciones defensivas (Blue Team). Aloja herramientas de monitorización, análisis de tráfico, respuesta a incidentes y correlación de eventos, sirviendo como plataforma principal de defensa y detección dentro del laboratorio.

*Acts as the defensive operations workstation (Blue Team). It hosts monitoring tools, traffic analysis, incident response, and event correlation, serving as the primary defense and detection platform within the lab.*

<div align="center">
  <img src="img/Ordenador-2.jpeg" alt="Ordenador 3 — ASUS Old Model" width="400px" style="border-radius: 10px; box-shadow: 0px 4px 10px rgba(0,0,0,0.5);">
</div>

#### 🛠️ Especificaciones Técnicas / Technical Specifications
| Componente / Component | Detalle / Detail |
| :--- | :--- |
| **Procesador (CPU)** | `Intel Core i5-4570` |
| **Memoria RAM** | `16 GB DDR3` |
| **Almacenamiento** | `500 GB SSD` |
| **Rol / Sistema Operativo** | `Kali Purple` |

<br>

### 🖥️ Ordenador 4: ASUS — New Model

Actúa como base de operaciones ofensivas (Red Team). Concentra todo el arsenal necesario para ejecutar reconocimientos, lanzar exploits y comprometer los sistemas de la red de víctimas de forma controlada.

*Acts as the offensive operations base (Red Team). It houses all the tools needed to perform reconnaissance, launch exploits, and compromise victim network systems in a controlled manner.*

<div align="center">
  <img src="img/Ordenador-3.jpeg" alt="Ordenador 4 — ASUS New Model" width="400px" style="border-radius: 10px; box-shadow: 0px 4px 10px rgba(0,0,0,0.5);">
</div>

#### 🛠️ Especificaciones Técnicas / Technical Specifications
| Componente / Component | Detalle / Detail |
| :--- | :--- |
| **Procesador (CPU)** | `Intel Core i5-1235U` |
| **Memoria RAM** | `32 GB DDR5` |
| **Almacenamiento** | `2 TB SSD` |
| **Rol / Sistema Operativo** | `Kali Linux` |

---
