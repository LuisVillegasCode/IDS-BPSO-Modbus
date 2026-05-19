# Lightweight IDS para Redes OT: Optimización BPSO-RF para Edge Computing

Implementación empírica de un Sistema de Detección de Intrusiones (IDS) ligero, diseñado específicamente para entornos de Tecnologías de Operación (OT). Este proyecto propone una arquitectura *wrapper* que integra la Optimización por Enjambre de Partículas Binario (BPSO) y un ensamble Random Forest (RF) para mitigar la "maldición de la dimensionalidad" en el tráfico de red industrial (Modbus/TCP).

El objetivo principal es viabilizar el despliegue de modelos de Inteligencia Artificial en dispositivos perimetrales (Edge) con recursos físicos estrictamente limitados, garantizando la detección de Ataques de Inyección de Datos Falsos (FDIA) en tiempo real.

## 🚀 Resultados Clave de Eficiencia Computacional

La experimentación controlada sobre el *ICS Cyber Attack Dataset* demostró que el motor de selección BPSO logró un rendimiento óptimo aplicable a la industria:

* **Compresión Dimensional:** Reducción del **55.47%** del espacio de búsqueda (de 128 a 57 características críticas).
* **Huella de Hardware (Edge):** Consumo pico de memoria volátil limitado a **2.37 MB**, garantizando escalabilidad en nodos IoT/IIoT industriales.
* **Latencia de Inferencia:** Tiempo de respuesta ultrabajo de **0.0239 ms** por flujo de red.
* **Resiliencia Predictiva:** Mantenimiento de una alta asertividad frente a ciberataques con un **F1-Score de 0.9166**.

## 📂 Estructura del Repositorio

* `Paper_BPSO_RF_IDS_OT.pdf`: Documento completo de la investigación científica, que detalla la metodología empírica, formulación matemática y discusión de resultados.
* `IDS_BPSO_OT_Experiment.ipynb`: Notebook de Google Colab que contiene el código fuente de la investigación, incluyendo el preprocesamiento de datos, implementación de la metaheurística (BPSO) y el perfilamiento de hardware (`tracemalloc`, `psutil`).
* `referencias/`: Directorio que contiene el material bibliográfico de soporte y referencias de literatura.

## 🛠️ Tecnologías y Herramientas

* **Lenguaje:** Python 3
* **Machine Learning & Enjambre:** `scikit-learn`, `pyswarms`, `imbalanced-learn`
* **Perfilamiento de Hardware:** `tracemalloc`, `psutil`
* **Protocolos y Entornos:** Modbus/TCP, Edge Computing, Smart Grids (SCADA)

## ✉️ Contacto

**Luis Javier Villegas Noblecilla**
Estudiante de Ingeniería de Ciberseguridad
* [LinkedIn](https://www.linkedin.com/in/luis-javier-villegas-noblecilla-/)
* [ResearchGate](https://www.researchgate.net/profile/Luis-Villegas-23)
