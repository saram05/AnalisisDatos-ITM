# Informe Técnico: Análisis Exploratorio y Reducción de Dimensionalidad

## 1. Información Institucional
*   **Institución:** Instituto Tecnológico Metropolitano (ITM)
*   **Facultad:** Ingenierías
*   **Carrera:** Ingeniería de Sistemas
*   **Materia:** Análisis de Datos
*   **Docente:** Daniel Alexis Nieto Mora
*   **Semestre:** 2026-1

---

## 2. Identificación del Equipo
*   **Estudiante 1:** [1017252383 - Sara Melissa Marroquin Vega] - [saram05]
*   **Estudiante 2:** [1022002249 - Santiago García Londoño] - [SantiagoGarcia555]

---

## 3. Descripción del Proyecto
Este repositorio documenta el desarrollo del segundo evento evaluativo del curso. El objetivo central es aplicar el flujo de trabajo de la ciencia de datos sobre un conjunto de información real, abarcando desde la exploración inicial de diversas fuentes hasta la implementación de técnicas de reducción de dimensionalidad y preprocesamiento.

El proyecto se desarrolla bajo una metodología modular y colaborativa, asegurando la trazabilidad de los aportes individuales mediante el control de versiones con Git.

---

## 4. Fase 1: Exploración y Comparación de Bases de Datos

Se analizaron tres conjuntos de datos de diversa naturaleza técnica para evaluar su pertinencia frente a los objetivos del curso:

| Atributo | Dataset 1: Titanic | Dataset 2: Customer Personality | Dataset 3: MNIST |
| :--- | :--- | :--- | :--- |
| **Tipo de dato** | Tabular (Estructurado) | Tabular (Estructurado) | Imagen (No estructurado) |
| **Fuente** | Secundaria (Kaggle/Registros Históricos) | Secundaria (Kaggle/Marketing Retail) | Secundaria (NIST/Visión Artificial) |
| **Registros** | 891 | 2,240 | 42,000 |
| **Atributos** | 12 | 29 | 784 (28x28 píxeles) |
| **Complejidad** | Baja | Media - Alta | Alta |
| **Aplicación** | Clasificación de supervivencia | Segmentación y Reducción | Reconocimiento de caracteres |

### 4.1 Justificación del Dataset Seleccionado
Se seleccionó el dataset **Customer Personality Analysis** por las siguientes razones técnicas:
1.  **Dimensionalidad:** Al contar con 29 variables, justifica plenamente el uso de técnicas de reducción como PCA en la Fase 3.
2.  **Calidad de los Datos:** Presenta desafíos técnicos reales (valores faltantes en `Income` y valores atípicos en `Year_Birth`) que permiten demostrar habilidades en preprocesamiento.
3.  **Potencial de Análisis:** Facilita la creación de múltiples hipótesis sobre el comportamiento del consumidor y su relación con variables demográficas.

---

## 5. Fase 2: Análisis Exploratorio de Datos (EDA)

El análisis se estructura en el notebook `02_EDA.ipynb` y aborda los siguientes puntos críticos:

*   **Revisión de Valores Faltantes:** Identificación y cuantificación de datos ausentes, proponiendo estrategias de imputación o eliminación fundamentadas.
*   **Detección de Valores Atípicos:** Uso de métodos estadísticos (IQR y Z-score) y gráficos (Boxplots) para identificar anomalías.
*   **Análisis de Distribuciones:** Evaluación de sesgos en variables numéricas y necesidad de transformaciones logarítmicas o estandarización.
*   **Análisis Multivariado:** Construcción de matrices de correlación y diagramas de dispersión para identificar dependencias entre variables de consumo y demografía.
*   **Hipótesis Iniciales:** Planteamiento de preguntas de investigación verificables con los datos (ej. Relación entre nivel educativo y gasto en productos de lujo).

---

## 6. Fase 3: Preprocesamiento y Reducción de Dimensionalidad

En el notebook `03_Reduccion.ipynb`, se ejecutan las técnicas necesarias para preparar los datos para modelos futuros:

1.  **Codificación:** Transformación de variables categóricas (como nivel educativo o estado civil) mediante técnicas de One-Hot Encoding o Label Encoding.
2.  **Escalado:** Normalización o estandarización de variables numéricas para asegurar que todas contribuyan equitativamente al análisis.
3.  **PCA (Análisis de Componentes Principales):** Reducción de los 29 atributos originales a un conjunto menor de componentes que expliquen la mayor parte de la varianza, facilitando la visualización y eficiencia del modelo.

---

## 7. Estructura del Repositorio

El proyecto mantiene la siguiente organización de archivos para cumplir con el requisito de modularidad:

```text
/
├── data/                       # Archivos fuente en formato CSV
├── notebooks/                  #
│   ├── 01_exploracion.ipynb    # 
│   ├── 02_eda.ipynb            # Análisis exploratorio profundo y visualizaciones
│   └── 03_reduccion.ipynb      # Preprocesamiento y aplicación de PCA
├── .gitignore                  #
└── README.md                   # Documentación técnica principal