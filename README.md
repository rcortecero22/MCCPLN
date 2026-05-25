# MCCPLN
Diseño y construcción de dashboard de inteligencia de negocios 
# Análisis Bibliométrico y NLP aplicado a una Problemática de Negocio

## Descripción del proyecto

Este proyecto desarrolla un análisis bibliométrico y de procesamiento de lenguaje natural, NLP, a partir de una base de datos exportada desde Scopus. El objetivo principal es identificar tendencias de investigación, autores relevantes, palabras clave dominantes, redes de colaboración y percepciones asociadas a una problemática de negocio mediante análisis de sentimientos.

El trabajo integra técnicas de análisis de datos, visualización, bibliometría, NLP y diseño estratégico para convertir información científica en insumos útiles para la toma de decisiones empresariales.

## Objetivo general

Analizar una base bibliográfica obtenida desde Scopus para identificar patrones de conocimiento, tendencias temáticas y oportunidades estratégicas relacionadas con una problemática de negocio.

## Objetivos específicos

- Importar y preparar datos bibliográficos en un entorno Jupyter Notebook / Google Colab.
- Realizar un análisis exploratorio de los documentos científicos.
- Identificar autores, fuentes, años y palabras clave más relevantes.
- Construir visualizaciones bibliométricas.
- Analizar resúmenes mediante NLP para extraer sentimientos asociados a la problemática de negocio.
- Diseñar estrategias basadas en los hallazgos del análisis.
- Definir KPIs para evaluar dichas estrategias.
- Proponer un dashboard dinámico o reporte automático interpretado por un LLM.

## Fuente de datos

La base de datos utilizada corresponde a un archivo exportado desde Scopus:

- Archivo: `scopus.csv`
- Tipo de información: documentos académicos
- Campos principales:
  - Autores
  - Título
  - Año
  - Fuente
  - Resumen
  - Palabras clave
  - Citas
  - DOI
  - Afiliaciones

## Herramientas utilizadas

- Google Colab
- Jupyter Notebook
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- NetworkX
- VADER Sentiment Analysis
- GitHub

## Metodología

El proyecto se desarrolló en varias etapas:

### Paso 1. Recolección de datos

Se utilizó una base bibliográfica exportada desde Scopus en formato CSV.

### Paso 2. Alistamiento del entorno

Se configuró el entorno de trabajo en Google Colab y se creó el repositorio en GitHub.

### Paso 3. Importación de librerías

Se importaron librerías de análisis de datos, visualización, redes y NLP.

### Paso 4. Identificación de la problemática de negocio

Se definió una problemática relacionada con la adopción, privacidad, seguridad, costos y oportunidades estratégicas asociadas a las tendencias encontradas en la literatura científica.

### Paso 5. Análisis bibliométrico

Se analizaron publicaciones por año, autores principales, fuentes relevantes, palabras clave y redes de coocurrencia.

### Paso 6. Análisis NLP de resúmenes

Se aplicó análisis de sentimientos a los resúmenes usando VADER para identificar percepciones positivas, negativas y neutrales asociadas a la problemática de negocio.

### Paso 7. Visualización de resultados

Se generaron gráficos y visualizaciones interactivas para interpretar tendencias, frecuencias y relaciones entre conceptos.

### Paso 8. Interpretación de resultados

Se analizaron los gráficos y tablas generadas para extraer conclusiones sobre tendencias científicas, oportunidades de innovación y riesgos estratégicos.

### Paso 9. Diseño de estrategias

Se propusieron estrategias relacionadas con privacidad, adopción, innovación abierta y vigilancia tecnológica.

### Paso 10. Diseño de KPIs

Se definieron indicadores clave de rendimiento para medir la efectividad de las estrategias propuestas.

### Paso 11. Entrega en GitHub

Se publica el notebook final, el archivo README, los datos y los resultados generados en el repositorio.

## Principales análisis realizados

### 1. Análisis de publicaciones por año

Permite identificar la evolución temporal del tema y detectar años de mayor producción científica.

### 2. Análisis de autores

Permite reconocer autores influyentes y posibles referentes académicos o aliados estratégicos.

### 3. Análisis de fuentes

Permite identificar revistas, conferencias o medios donde se concentra la producción científica.

### 4. Análisis de palabras clave

Permite detectar los conceptos dominantes y las tendencias temáticas principales.

### 5. Redes de coautoría

Permiten visualizar relaciones de colaboración entre investigadores.

### 6. Redes de coocurrencia de palabras clave

Permiten identificar conexiones entre temas y posibles clústeres de investigación.

### 7. Análisis de sentimientos

Permite extraer señales positivas, negativas o neutrales en los resúmenes de los documentos analizados.

## Problemática de negocio

A partir del análisis bibliométrico y NLP, se plantea una problemática relacionada con cómo las organizaciones pueden adoptar tecnologías emergentes o enfoques innovadores minimizando barreras como:

- Costos de implementación.
- Riesgos de privacidad.
- Seguridad de la información.
- Dificultades de adopción.
- Falta de evidencia para la toma de decisiones.
- Necesidad de vigilancia tecnológica continua.

## Estrategias propuestas

### 1. Trust as a Service

Convertir la privacidad y seguridad en un diferencial competitivo.

### 2. Modelos de adopción y ROI

Reducir la fricción de adopción mediante modelos de prueba, pilotos y medición temprana de retorno.

### 3. Innovación abierta

Aprovechar autores, instituciones y documentos relevantes para identificar oportunidades de colaboración científica o transferencia tecnológica.

### 4. Vigilancia tecnológica

Actualizar periódicamente el análisis bibliométrico y NLP para monitorear nuevas tendencias.

## KPIs propuestos

| Pilar estratégico | KPI | Fórmula / Métrica | Meta sugerida |
|---|---|---|---|
| Privacidad y seguridad | Tasa de conversión por confianza | Clientes que compran por seguridad / total clientes nuevos | Mayor al 30% |
| Privacidad y seguridad | Incidentes de privacidad | Número de incidentes o brechas | 0 incidentes |
| Costo y adopción | Conversión trial a pago | Usuarios pagos / usuarios trial | Mayor al 5% |
| Costo y adopción | Time-to-Value | Días hasta primer valor percibido | Menor a 14 días |
| Innovación abierta | Transferencia tecnológica | Funcionalidades basadas en literatura científica | 2 por año |
| Vigilancia tecnológica | Actualización de datos | Días desde la última actualización | Menor a 90 días |

## Dashboard dinámico

El proyecto propone un dashboard dinámico que integra:

- KPIs principales.
- Gráficos de publicaciones por año.
- Distribución de sentimientos.
- Principales fuentes.
- Principales palabras clave.
- Interpretación automática tipo LLM de los gráficos.
- Recomendaciones estratégicas.

## Archivos del repositorio

| Archivo / carpeta | Descripción |
|---|---|
| `README.md` | Descripción general del proyecto |
| `scopus.csv` | Base de datos bibliográfica exportada desde Scopus |
| `notebook_final.ipynb` | Notebook principal del análisis |
| `outputs/` | Carpeta con gráficos, tablas y dashboard |
| `requirements.txt` | Librerías necesarias para reproducir el análisis |

## Resultados esperados

Este proyecto permite transformar una base bibliográfica en un sistema de inteligencia de negocio, integrando análisis académico, NLP, visualización y estrategia empresarial.

Los resultados permiten:

- Identificar tendencias científicas relevantes.
- Detectar oportunidades de innovación.
- Comprender barreras de adopción.
- Diseñar estrategias basadas en evidencia.
- Medir dichas estrategias mediante KPIs.
- Comunicar los hallazgos en un dashboard ejecutivo.

## Dashboard

El dashboard del proyecto se encuentra en:

dashboard.html`

Para visualizarlo, se puede descargar el archivo y abrirlo en un navegador web.

## Conclusiones

El análisis bibliométrico permitió reconocer patrones de producción científica, autores, fuentes y temas relevantes. El análisis NLP complementó estos hallazgos al identificar señales de sentimiento en los resúmenes, permitiendo conectar el conocimiento académico con una problemática de negocio.

La combinación de bibliometría, NLP, dashboards y KPIs demuestra cómo los datos científicos pueden convertirse en insumos estratégicos para la toma de decisiones organizacionales.

Cordial saludo,

Hago entrega del proyecto final desarrollado en Google Colab y publicado en GitHub. El proyecto contiene el análisis bibliométrico de una base exportada desde Scopus, el procesamiento de resúmenes mediante NLP, el diseño de estrategias, KPIs y una propuesta de dashboard dinámico para la interpretación de resultados.


Muchas gracias.

## Autor

Proyecto desarrollado por: RONNY CORTECERO CONTRERAS

Repositorio:

https://github.com/rcortecero22/MCCPLN
