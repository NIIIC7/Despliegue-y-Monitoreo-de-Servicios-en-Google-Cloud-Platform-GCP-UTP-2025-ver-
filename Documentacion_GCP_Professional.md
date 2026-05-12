# Documentación Técnica: Despliegue y Monitoreo en Google Cloud Platform (GCP)

## 1. Identificación del Proyecto
**Curso:** Integración de servicios cloud GCP  
**Integrantes:** * Nick Christian Uchasara Gonzales (U21318040)
**Institución:** Universidad Tecnológica del Perú (UTP)  
**Fecha:** 2025

---

## 2. Resumen Ejecutivo
Implementación de infraestructura híbrida en la nube utilizando **Google Cloud Platform**. El proyecto abarca desde el despliegue de servidores **Windows Server (2016/2022)** mediante Compute Engine, hasta la gestión de bases de datos relacionales con **Cloud SQL (MySQL)** y la supervisión avanzada a través de **Cloud Monitoring**.

---

## 3. Arquitectura y Componentes
### 3.1. Compute Engine (IaaS)
* **File Server:** Windows Server 2016 | e2-medium | 5 TB Storage.
* **VPN Server:** Windows Server 2022 | e2-standard | 2 TB Storage.
* **Región:** us-west-1 (Oregón).

### 3.2. Cloud SQL (PaaS)
* **Motor:** MySQL 8.0 Enterprise.
* **Configuración:** Conectividad restringida a la red interna de las instancias de cómputo para máxima seguridad.

---

## 4. Guía de Implementación Paso a Paso

### Paso 1: Configuración de Instancias VM
Se procede a la creación de las máquinas virtuales en la consola de Google Cloud, definiendo las políticas de firewall y el acceso RDP.

> ![IMAGE_PLACEHOLDER: Configuración de Instancia en Compute Engine]

### Paso 2: Despliegue de Base de Datos
Creación de la instancia de Cloud SQL asegurando la compatibilidad de red con las instancias creadas anteriormente.

### Paso 3: Monitoreo y Logging
Configuración de los agentes de monitoreo para recolectar métricas de salud (CPU, Memoria, Disco).

> ![IMAGE_PLACEHOLDER: Panel de Cloud Monitoring]

---

## 5. Visualización de Datos (Dashboards)
Se diseñaron tableros personalizados en **Cloud Monitoring** que permiten comparar en tiempo real:
1.  Utilización de CPU por servidor.
2.  Latencia de respuesta de la base de datos.
3.  Registros de eventos críticos (Logging).

> ![IMAGE_PLACEHOLDER: Dashboard de Rendimiento en Tiempo Real]

---

## 6. Conclusiones y Recomendaciones
* **Escalabilidad:** GCP permite ajustar los recursos de las VMs y SQL según la carga de trabajo sin interrupciones significativas.
* **Seguridad:** El uso de IAM y redes privadas virtuales garantiza que los datos sensibles permanezcan protegidos.
* **Recomendación:** Se sugiere implementar **Terraform** para automatizar futuros despliegues y evitar errores de configuración manual.

---

## 7. Referencias
* Documentación oficial de Google Cloud Platform.
* Guías de laboratorio UTP 2025.
