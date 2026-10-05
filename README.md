# IDS ligero para redes OT con BPSO y Random Forest

Este repositorio contiene una investigación académica sobre selección de características para sistemas de detección de intrusiones en entornos de Tecnologías de Operación (OT).

La propuesta utiliza Binary Particle Swarm Optimization (BPSO) para reducir la dimensionalidad del tráfico industrial y un clasificador Random Forest para evaluar el impacto de esa selección sobre el desempeño y el costo computacional.

## Objetivo

El trabajo estudia si una selección de características basada en BPSO puede reducir el número de variables procesadas por un IDS sin perder de forma significativa su capacidad de detección.

El escenario experimental utiliza tráfico asociado a sistemas eléctricos y ataques de inyección de datos falsos (FDIA).

## Flujo experimental

```text
Dataset de tráfico OT
        |
        v
Limpieza y preprocesamiento
        |
        v
Balanceo del conjunto de entrenamiento
        |
        v
Selección de características con BPSO
        |
        v
Random Forest
        |
        v
Evaluación predictiva y computacional
```

## Resultados obtenidos

En la configuración evaluada se obtuvieron los siguientes resultados:

- Reducción dimensional: 128 a 57 características.
- Compresión del espacio de entrada: 55.47 %.
- F1-Score: 0.9166.
- Latencia de inferencia medida: 0.0239 ms por flujo.
- Memoria pico reportada durante el perfilamiento: 2.37 MB.

Estas cifras corresponden al entorno y dataset utilizados en el experimento. No deben interpretarse como garantía de rendimiento en una red OT de producción.

## Contenido del repositorio

- `Luis_Villegas_EP_v1.0.ipynb`: notebook principal del experimento.
- `Paper_BPSO_RF_IDS_OT.pdf`: documento de investigación con metodología y discusión de resultados.
- `Referencias/`: bibliografía utilizada como soporte del estudio.
- `README.md`: resumen técnico del proyecto.

## Tecnologías

- Python
- pandas
- NumPy
- scikit-learn
- imbalanced-learn
- pyswarms
- Matplotlib
- Seaborn
- psutil
- tracemalloc

## Ejecución

El notebook fue preparado para ejecutarse en Google Colab o en un entorno local con Python 3.

Instala las dependencias con:

```bash
pip install -r requirements.txt
```

El dataset no se incluye en el repositorio. La ruta de entrada debe ajustarse en el notebook antes de ejecutar el pipeline.

## Aspectos evaluados

El experimento considera tanto métricas de clasificación como indicadores relacionados con eficiencia computacional:

- número de características seleccionadas;
- porcentaje de reducción dimensional;
- F1-Score y otras métricas de clasificación;
- tiempo de entrenamiento;
- latencia de inferencia;
- consumo de memoria;
- comportamiento de convergencia del proceso de selección.

## Limitaciones

El proyecto corresponde a una validación experimental y no a un IDS desplegado en una infraestructura OT real.

Las mediciones de latencia y memoria dependen del entorno de ejecución. Además, el rendimiento observado sobre un dataset específico no garantiza el mismo comportamiento frente a otros protocolos, topologías o familias de ataques.

## Autor

Luis Javier Villegas Noblecilla  
Estudiante de Ingeniería de Ciberseguridad - Universidad Nacional de Ingeniería
