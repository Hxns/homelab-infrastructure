<div align="center">
  <h1>🌌 Mi Homelab Infrastructure 🌌</h1>
  <p><i>Un entorno centralizado para experimentación, despliegue de servicios y aprendizaje continuo.</i></p>
  
  [![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)](#)
  [![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](#)
  [![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)](#)
  [![Network](https://img.shields.io/badge/Network-000000?style=for-the-badge&logo=ubiquiti&logoColor=white)](#)
</div>

---

## 🗺️ Arquitectura de Red y Organización

La infraestructura de este homelab está diseñada para garantizar estabilidad, seguridad y un rendimiento óptimo de todos los servicios locales. A continuación se presenta el diagrama general de la topología de red, mostrando cómo se interconectan los dispositivos, el enrutamiento y la distribución de los servicios clave en la red local.

<div align="center">
  <img src="img/Diagrama.png" alt="Diagrama de Arquitectura del Homelab" width="800px">
</div>

> **Nota:** Este diagrama ilustra el flujo de red, los nodos principales y la segmentación, facilitando una rápida comprensión de cómo están aislados o conectados los distintos servicios y dispositivos físicos.

---

## 💻 Hardware del Homelab

El entorno de computación se distribuye en tres ordenadores principales. Cada equipo cumple un rol específico dentro de la red (virtualización, almacenamiento, servicios ligeros, etc.).

<br>

### 🖥️ Ordenador 1: Nodo Principal

Este equipo es el músculo principal de la infraestructura, encargado de manejar las cargas de trabajo más intensas y la virtualización principal.

<div align="center">
  <img src="img/Ordenador-1.jpeg" alt="Ordenador 1" width="400px" style="border-radius: 10px; box-shadow: 0px 4px 10px rgba(0,0,0,0.5);">
</div>

#### 🛠️ Especificaciones Técnicas
| Componente | Detalle |
| :--- | :--- |
| **Procesador (CPU)** | `[ Escribe aquí el procesador, ej: Intel Core i7 ]` |
| **Memoria RAM** | `[ Escribe aquí la RAM, ej: 64GB DDR4 ]` |
| **Almacenamiento** | `[ Escribe aquí el almacenamiento, ej: 2TB NVMe ]` |
| **Rol / Sistema Operativo**| `[ Ej: Hypervisor Proxmox VE / Ubuntu Server ]` |

<br>

### 🖥️ Ordenador 2: Nodo Secundario

Un nodo ideal para almacenamiento masivo o despliegue de contenedores que no requieren la misma potencia bruta que el nodo principal.

<div align="center">
  <img src="img/Ordenador-2.jpeg" alt="Ordenador 2" width="400px" style="border-radius: 10px; box-shadow: 0px 4px 10px rgba(0,0,0,0.5);">
</div>

#### 🛠️ Especificaciones Técnicas
| Componente | Detalle |
| :--- | :--- |
| **Procesador (CPU)** | `[ Escribe aquí el procesador ]` |
| **Memoria RAM** | `[ Escribe aquí la RAM ]` |
| **Almacenamiento** | `[ Escribe aquí el almacenamiento ]` |
| **Rol / Sistema Operativo**| `[ Ej: NAS TrueNAS / Docker Compose ]` |

<br>

### 🖥️ Ordenador 3: Nodo Edge y Experimentación

Este equipo de bajo consumo es excelente para servicios 24/7 de alta disponibilidad, domótica (Home Assistant) o como servidor DNS (Pi-hole).

<div align="center">
  <img src="img/Ordenador-3.jpeg" alt="Ordenador 3" width="400px" style="border-radius: 10px; box-shadow: 0px 4px 10px rgba(0,0,0,0.5);">
</div>

#### 🛠️ Especificaciones Técnicas
| Componente | Detalle |
| :--- | :--- |
| **Procesador (CPU)** | `[ Escribe aquí el procesador ]` |
| **Memoria RAM** | `[ Escribe aquí la RAM ]` |
| **Almacenamiento** | `[ Escribe aquí el almacenamiento ]` |
| **Rol / Sistema Operativo**| `[ Ej: Debian Server / K3s ]` |

---

<div align="center">
  <i>Documentación creada para mantener el registro, mantenimiento y escalabilidad de la infraestructura.</i>
</div>
