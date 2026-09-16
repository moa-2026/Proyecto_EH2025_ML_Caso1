# 📊 Análisis de la Deserción Escolar en Bolivia
## Proyecto de Machine Learning con Datos de la EH2025

---

## 🎯 Descripción del proyecto

Este proyecto aplica técnicas de **ciencia de datos y machine learning** para analizar los factores que influyen en la **deserción escolar en Bolivia**, utilizando los microdatos de la **Encuesta de Hogares (EH) 2025** del Instituto Nacional de Estadística (INE).

El análisis se enfoca en la población de **6 a 18 años** (edad escolar obligatoria) y busca identificar patrones geográficos, socioeconómicos y demográficos que permitan **focalizar políticas públicas** para reducir la deserción.

---

## ❓ Pregunta de investigación

> **¿Cuáles son los factores sociodemográficos, económicos y geográficos que más influyen en la deserción escolar en Bolivia?**

---

## 🎯 Variables objetivo

| Variable | Tipo | Descripción |
|---|---|---|
| `Asistencia_Escolar` | Binaria | 1 = asiste, 0 = no asiste |
| `Nivel_Educativo_Alcanzado` | Categórica (3 clases) | Ninguno, Primaria, Secundaria |

---

## 📚 Fuente de datos

| Aspecto | Detalle |
|---|---|
| **Encuesta** | Encuesta de Hogares (EH) 2025 |
| **Institución** | Instituto Nacional de Estadística (INE) — Bolivia |
| **Acceso** | Archivo Nacional de Datos (ANDA) |
| **Formato original** | SPSS (`.sav`) |
| **Tablas utilizadas** | `EH2025_Persona`, `EH2025_Vivienda_1` |
| **Unidad de análisis** | Individuo (6-18 años) |
| **Tamaño final** | 9,895 individuos × 293 variables |

---

## 📁 Estructura del repositorio

```
Proyecto_EH2025_ML_DesercionEscolar/
├── data/
│   └── dataset_procesado.csv          # Dataset final (9,895 × 293)
├── notebooks/
│   └── EH2025_Analisis_ML.ipynb       # Notebook completo con todo el pipeline
├── outputs/
│   ├── storytelling.pdf               # PDF ejecutivo (Parte 4)
│   ├── predicciones.csv               # Predicciones del modelo
│   ├── importancia_variables.csv      # Importancia de variables (RF binario)
│   ├── tasa_desercion_depto.csv       # Tasa de deserción por departamento
│   ├── mapa_desercion.html            # Mapa interactivo (Folium)
│   └── imagenes/                      # 18 gráficos generados
├── docs/
│   └── README.md                      # Este archivo
└── requirements.txt                   # Dependencias del proyecto
```

---

## 🛠️ Instalación y ejecución

### Opción 1: Google Colab (recomendado)

1. Abre el notebook `notebooks/EH2025_Analisis_ML.ipynb` en Google Colab.
2. Ejecuta la primera celda para montar Google Drive.
3. Ajusta las rutas de los archivos `.sav` según tu estructura.
4. Ejecuta todas las celdas en orden.

### Opción 2: Entorno local

```bash
git clone https://github.com/[tu-usuario]/Proyecto_EH2025_ML_DesercionEscolar.git
cd Proyecto_EH2025_ML_DesercionEscolar
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/EH2025_Analisis_ML.ipynb
```

---

## 📊 Metodología

El proyecto se organiza en 4 partes:

| Parte | Contenido |
|---|---|
| **Parte 1** | Obtención y preprocesamiento de datos |
| **Parte 2** | Análisis exploratorio y visualización |
| **Parte 3** | Modelos de Machine Learning |
| **Parte 4** | Storytelling y recomendaciones de política pública |

---

## 🤖 Resultados del modelo

### Modelo binario (Asistencia Escolar)

| Métrica | Valor |
|---|---|
| **Accuracy** | 0.937 |
| **Precision** | 0.984 |
| **Recall** | 0.950 |
| **F1-Score** | 0.967 |
| **AUC-ROC** | **0.907** |

### Modelo multiclase (Nivel Educativo Alcanzado)

| Métrica | Valor |
|---|---|
| **Accuracy** | 0.888 |
| **F1-Macro** | 0.854 |
| **F1-Weighted** | 0.891 |

### Top 5 variables más importantes (modelo binario)

1. **Edad** (30.62%)
2. **Años de estudio** (22.44%)
3. **Ingreso per cápita** (10.03%)
4. **Ratio de dependencia** (8.42%)
5. **Nivel educativo del jefe** (7.00%)

---

## 🎯 Recomendaciones de política pública

1. **Focalizar transferencias condicionadas** en el decil más pobre.
2. **Programa especial para adolescentes** (15-18 años).
3. **Infraestructura educativa rural** focalizada.
4. **Alfabetización digital y conectividad** en hogares vulnerables.
5. **Sistema de alerta temprana** basado en el modelo Random Forest.
6. **Programa de nivelación académica** para estudiantes con rezago.

---

## 📚 Referencias

- **INE Bolivia (2025):** Encuesta de Hogares (EH) 2025.
- **UNESCO (2020):** Informe de seguimiento de la educación en el mundo.
- **UNICEF (2020):** Análisis de la situación de la niñez en Bolivia.
- **Banco Mundial (2024):** Indicadores de desarrollo educativo.

---

## 👤 Autor

**MARCOS ORMACHEA ARAYA**

MAESTRANTE UPEA

