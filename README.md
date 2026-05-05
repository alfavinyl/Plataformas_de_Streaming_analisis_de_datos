# 🎬 Análisis Comparativo de Plataformas de Streaming

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12-4c72b0)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7-orange)
![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?logo=kaggle)
![Estado](https://img.shields.io/badge/Estado-Completado-brightgreen)

---

## 📌 Descripción del proyecto

Este proyecto analiza y compara los catálogos de **Netflix**, **Disney+** y **Prime Video** utilizando datos reales de Kaggle. A través de limpieza de datos, análisis estadístico y visualizaciones, se identifican patrones, fortalezas y diferencias estratégicas entre las tres plataformas.

### ❓ Pregunta de investigación

> ¿Qué plataforma de streaming ofrece el catálogo más diverso, actualizado y relevante para diferentes tipos de audiencia, y qué estrategias de contenido distinguen a cada una?

---

## 📦 Dataset

| Plataforma | Fuente | Registros |
|---|---|---|
| Netflix | [Kaggle — Shivam Bansal](https://www.kaggle.com/datasets/shivamb/netflix-shows) | 8,807 |
| Prime Video | [Kaggle — Shivam Bansal](https://www.kaggle.com/datasets/shivamb/amazon-prime-movies-and-tv-shows) | 9,668 |
| Disney+ | [Kaggle — Shivam Bansal](https://www.kaggle.com/datasets/shivamb/disney-movies-and-tv-shows) | 1,450 |
| **Total combinado** | `df_universal` | **19,925** |

**Variables analizadas:** tipo de contenido, título, director, país, año de lanzamiento, rating, duración, géneros y fecha de agregación a la plataforma.

---

## 🗂️ Estructura del proyecto

```
streaming_analisis_de_datos/
│
├── data/
│   ├── netflix_titles.csv
│   ├── amazon_prime_titles.csv
│   └── disney_plus_titles.csv
│
├── Streaming.ipynb        # Notebook principal
└── README.md
```

---

## 🔍 Fases del análisis

### 🧹 Fase 1 — Exploración inicial
- Registros y títulos únicos por plataforma
- Proporción de películas vs series
- Rango de años de lanzamiento por plataforma

### 📊 Fase 2 — Análisis de contenido
- Plataforma con contenido más reciente (mediana)
- Top 10 géneros del catálogo combinado
- Géneros dominantes por plataforma
- Duración promedio de películas

### 🌍 Fase 3 — Países y directores
- Top 5 países productores por plataforma
- Directores más prolíficos por plataforma
- Análisis de nulos en `country` con criterio analítico

### 👥 Fase 4 — Agrupaciones comparativas
- Crecimiento del catálogo año con año
- Patrones estacionales de agregación de contenido
- Tabla resumen comparativa por plataforma

### 📈 Fase 5 — Visualizaciones
- Gráfico de barras agrupadas: películas vs series
- Línea temporal: crecimiento del catálogo
- Bar chart horizontal: top 10 géneros
- **Heatmap: contenido agregado por mes y plataforma**

### 🔗 Fase 6 — Análisis cruzado
- Títulos compartidos entre plataformas con `pd.merge()`
- Diversidad y distribución de ratings por plataforma

---

## 📋 Principales hallazgos

1. **Prime Video** es la plataforma más grande con 9,668 títulos, pero tiene un 93% de nulos en `country` y 98% en `date_added`, lo que limita varios análisis.
2. **Netflix** tiene el contenido más reciente con una mediana de 2017 en año de lanzamiento.
3. Cada plataforma tiene una identidad clara de géneros: Disney+ con *Family*, Netflix con *International Movies* y Prime Video con *Drama*.
4. **Netflix y Prime Video** comparten 389 títulos, mientras Disney+ apenas comparte 43 con Netflix — consistente con su modelo de contenido exclusivo.
5. **Disney+** tiene las películas más cortas (71.91 min en promedio) vs Netflix con las más largas (99.58 min).
6. Ambas plataformas alcanzaron su pico de crecimiento en **2019**, coincidiendo con la guerra del streaming.

---

## 💡 Propuestas basadas en el análisis

- **Disney+:** Invertir en contenido internacional reciente para atraer audiencias adultas más allá del público familiar.
- **Netflix:** Fortalecer contenido original exclusivo y reducir dependencia de títulos compartidos con Prime Video.
- **Prime Video:** Priorizar la completitud de metadatos del catálogo para mejorar sistemas de recomendación.

---

## 🛠️ Tecnologías utilizadas

- **Python 3.10**
- **Pandas** — manipulación y limpieza de datos
- **Matplotlib** — visualizaciones
- **Seaborn** — heatmap y gráficos estadísticos
- **KaggleHub** — descarga de datasets
- **Google Colab** — entorno de desarrollo

---

## 🚀 ¿Cómo ejecutar el proyecto?

1. Clona el repositorio:
```bash
git clone https://github.com/alfavinyl/streaming_analisis_de_datos.git
```

2. Abre `Streaming.ipynb` en Google Colab o Jupyter Notebook.

3. Los datasets se descargan automáticamente con `kagglehub` al ejecutar la primera celda.

---

## 👤 Autor

**Fernando Teodoro**  
Estudiante de Data Science | Proyecto de portafolio  
[GitHub](https://github.com/alfavinyl)

---

> Este es el segundo proyecto de un portafolio de Data Science en construcción.  
> Proyecto 1: [Análisis Sísmico de México](https://github.com/alfavinyl) 🌎
