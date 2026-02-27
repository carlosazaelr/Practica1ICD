# Practica1ICD
Introducción a Ciencia de Datos
# 🔬 Análisis Exploratorio y Medidas de Similitud: Dataset Cáncer de Mama (WDBC)

Este repositorio contiene un cuaderno de Jupyter (Jupyter Notebook) con una práctica integral de ciencia de datos enfocada en el **Wisconsin Diagnostic Breast Cancer (WDBC) dataset**. 

El proyecto abarca desde la carga y limpieza inicial de los datos hasta la implementación desde cero de algoritmos de medición de similitud y disimilitud entre pacientes, pasando por un análisis estadístico y visual profundo.

## 📊 Sobre el Dataset
El dataset contiene características calculadas a partir de imágenes digitalizadas de punciones con aguja fina (FNA) de masas mamarias. Describe las características de los núcleos celulares presentes en la imagen.
* **Instancias:** 569
* **Atributos:** 32 (ID, Diagnóstico [M=Maligno, B=Benigno], y 30 características numéricas continuas como radio, textura, perímetro, área, etc.)

## 🚀 Contenido del Proyecto

El cuaderno está dividido en 5 partes principales:

### Parte I — Carga y Limpieza de Datos
* Importación de librerías esenciales (`numpy`, `pandas`, `matplotlib`).
* Asignación de nombres de columnas basados en la documentación oficial (`wdbc.names`).
* Identificación y tratamiento de valores nulos o faltantes para asegurar la integridad de los datos.

### Parte II — Identificación de Atributos
* Detección de tipos de datos computacionales usando `pandas` (`dtypes`, `nunique`).
* Clasificación teórica (Nominal, Binario, Numérico Continuo) y justificación estadística de la naturaleza de las variables médicas.

### Parte III — Estadística Descriptiva
* Cálculo de métricas de tendencia central (Media, Mediana, Moda) para características clave como el tamaño del tumor (`radius_mean`).
* Análisis de dispersión (Rango, Cuartiles, IQR, Varianza, Desviación Estándar) para entender la variabilidad celular.
* Análisis de frecuencias para variables categóricas (Diagnóstico).

### Parte IV — Visualización de Datos
* **Histogramas y KDE:** Para observar la distribución de características continuas.
* **Boxplots (Diagramas de Caja):** Para identificar valores atípicos (outliers) que clínicamente podrían representar anomalías celulares severas.
* **Scatter Plots:** Para explorar la relación bidimensional entre distintas métricas (ej. Radio vs. Textura).
* **Gráficos de Barras:** Para visualizar el balance de clases (Benigno vs. Maligno).

### Parte V — Medición de Similitud y Disimilitud
Implementación de diversas métricas matemáticas para comparar "perfiles" de pacientes en una submuestra aleatoria:
* **Distancias Numéricas:** Implementación de la función generalizada de Minkowski (Euclidiana $p=2$ y Manhattan $p=1$).
* **Distancias Binarias:** Cálculo de la distancia de Hamming y similitud de Jaccard basadas en la binarización de diagnósticos y tamaños tumorales.
* **Similitud Coseno:** Cálculo de ángulos entre vectores de pacientes estandarizados mediante Z-score.
* **Tipos Mixtos:** Implementación simplificada (tipo Gower) para calcular distancias combinando variables numéricas normalizadas y categóricas simultáneamente.

## 🛠️ Tecnologías y Librerías Utilizadas
* **Lenguaje:** Python 3.13.5
* **Entorno:** Jupyter Notebook
* **Análisis y manipulación de datos:** `pandas`, `numpy`
* **Visualización:** `matplotlib`

## ⚙️ Cómo ejecutar este proyecto

1. Clona este repositorio en tu máquina local:
   ```bash
   git clone [https://github.com/carlosazaelr/Practica1ICD.git](https://github.com/carlosazaelr/Practica1ICD.git)
2. Asegúrate de tener instalado Python y Jupyter Notebook.
3. Instala las dependencias necesarias:
   ```bash
   pip install pandas numpy matplotlib
4. Abre el entorno de Jupyter:
    ```bash
   jupyter notebook

5. Abre el archivo .ipynb y ejecuta las celdas secuencialmente. (Asegúrate de que los archivos wdbc.data y wdbc.names estén en el mismo directorio que el cuaderno).

✒️ Autor
[Carlos A. Ramirez/carlosazaelr] - Desarrollo de la práctica - [GitHub](https://github.com/carlosazaelr/Practica1ICD/tree/main/p1)
