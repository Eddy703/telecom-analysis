# telecom-analysis
Proyecto 6 - Análisis de una empresa de telecomunicaciones. 

# 📊 Análisis de Comportamiento de Clientes - ConnectaTel

## 🎯 Objetivo del Proyecto
El objetivo principal de este proyecto es analizar el comportamiento de uso de los clientes de **ConnectaTel**, una empresa de telecomunicaciones en Latinoamérica. A través del análisis de datos históricos (hasta 2024), se busca construir un perfil estadístico de los usuarios, detectar comportamientos atípicos (Heavy Users) y crear una segmentación conductual. 

Los hallazgos de este análisis están orientados a proporcionar recomendaciones estratégicas para optimizar la retención de clientes (reducción de Churn) y proponer mejoras en la oferta actual de planes tarifarios (Básico y Premium).

## 🗂️ Datasets Utilizados
El análisis se fundamenta en tres conjuntos de datos principales:
* **`plans.csv`**: Información de los planes tarifarios actuales (costo mensual, minutos incluidos, GB, costo por excedentes).
* **`users_latam.csv`**: Perfil demográfico de 4,000 clientes, incluyendo edad, ciudad de residencia, fecha de registro, plan contratado y fecha de abandono (churn).
* **`usage.csv`**: Registro transaccional detallado (40,000 filas) del uso real de los servicios, clasificando eventos en llamadas (`call`) y mensajes de texto (`text`), junto con su duración o longitud.

## 🛠️ Etapas del Análisis Realizadas
1. **Carga y Exploración Inicial:** Revisión de la estructura de los datos, tipos de variables y detección de inconsistencias.
2. **Saneamiento y Calidad de Datos:** * Tratamiento de valores centinela (ej. edades `-999` y ubicaciones `?`).
   * Manejo estratégico de valores nulos, identificando nulos condicionales (MAR) en la duración de llamadas y longitud de mensajes.
3. **Agregación de Datos:** Transformación de registros transaccionales individuales en un perfil de consumo consolidado por usuario (Total de mensajes, llamadas y minutos).
4. **Análisis Exploratorio de Datos (EDA):** Visualización de distribuciones mediante histogramas y Boxplots.
5. **Tratamiento de Outliers:** Identificación de valores atípicos usando el método de Rango Intercuartílico (IQR). Se tomó la decisión estratégica de *mantenerlos*, ya que representan el consumo máximo real de la red comercial.
6. **Segmentación de Clientes:** Clasificación de usuarios en grupos de uso (*Bajo, Medio, Alto, Crítico*) y grupos de edad (*Joven, Adulto, Adulto Mayor*).
7. **Reporte Ejecutivo:** Traducción de hallazgos estadísticos en insights de negocio accionables.

## 🚀 Cómo Ejecutar el Notebook

Este proyecto fue desarrollado en un entorno de Jupyter Notebook y puede ser ejecutado localmente o en la nube.

**Opción A: Google Colab (Recomendado)**
1. Descarga el archivo `S7 Version-Estudiante-Project-ConnectaTel.ipynb`.
2. Sube el archivo a [Google Colab](https://colab.research.google.com/).
3. Carga los archivos `.csv` en el entorno virtual de Colab o ajusta las rutas de lectura usando Google Drive.

**Opción B: Entorno Local (Jupyter/VS Code)**
1. Asegúrate de tener instalado Python 3.x.
2. Instala las dependencias necesarias.
3. Abre el archivo `.ipynb` en tu editor de preferencia.

## 📋 Guía de Reproducción
Para reproducir los resultados exactos de este análisis, sigue estos pasos:

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/TU_USUARIO/TU_REPOSITORIO.git](https://github.com/TU_USUARIO/TU_REPOSITORIO.git)
   cd TU_REPOSITORIO
