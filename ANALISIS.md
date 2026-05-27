### Análisis integral del repositorio MCCPLN

Este documento presenta una lectura académica y argumentada de **todos los archivos versionados** del repositorio, con énfasis en su función dentro del pipeline de inteligencia científica (bibliometría + NLP + visualización + soporte estratégico).

### 1) Contexto y objetivo general del proyecto

El proyecto MCCPLN implementa un flujo de analítica aplicada para transformar una base bibliográfica exportada desde Scopus en insumos de decisión de negocio y educación. Su foco temático es la **IA generativa en contextos educativos y organizacionales**, y su propuesta metodológica combina:

- análisis bibliométrico descriptivo;
- análisis de sentimiento (VADER) sobre texto científico;
- visualización estática e interactiva;
- síntesis ejecutiva en dashboard y documento final.

Desde una perspectiva de curso universitario, el proyecto evidencia una cadena completa de valor analítico: **dato crudo → procesamiento reproducible → evidencia visual → narrativa estratégica**.

### 2) Inventario completo de archivos del repositorio

Archivos versionados (24):

1. `README.md`
2. `ANALISIS.md`
3. `scopus.csv`
4. `notebooks/Fase_4_Diseño_y_construcción_de_dashboard_de_inteligencia_de_negocios.ipynb`
5. `notebooks/cuaderno_final.ipynb`
6. `dashboard/Dashboard.html`
7. `documentos/Dashboard de Inteligencia Científica — IA Generativa.pdf`
8. `coauthorship_top.html`
9. `keyword_trends.html`
10. `pubs_per_year.html`
11. `outputs_train_series.csv`
12. `outputs_test_series.csv`
13. `outputs_pubs_time_series.png`
14. `outputs_forecast_comparison.png`
15. `outputs_forecast_report.pdf`
16. `sentiment_vader_per_doc.csv`
17. `sentiment_summary (1).csv`
18. `sentiment_distribution.png`
19. `representative_abstracts.csv`
20. `wordcloud_positive.png`
21. `wordcloud_positive (1).png`
22. `visualizaciones/Top HECHO por suma de EVENTOS.png`
23. `visualizaciones/Estimacion de densidad (KDE) de EVENTOS.png`
24. `visualizaciones/Eventos (suma) por VIGENCIA.png`

> Nota técnica: en el estado actual del repo se observan 24 entradas porque este documento (`ANALISIS.md`) se incorpora en esta actualización.

### 3) Análisis detallado por archivo (propósito, metodología, hallazgos y conclusión)

#### 3.1 Documentación base

##### `README.md`
- **Propósito:** portada técnica del repositorio y punto de acceso a artefactos.
- **Metodología implicada:** documentación estructurada por carpetas, enlaces relativos y contextualización del caso.
- **Hallazgos clave:** organiza notebooks, dashboard, visualizaciones y PDF ejecutivo en una arquitectura legible.
- **Conclusión:** mejora trazabilidad académica y permite reproducibilidad conceptual del proyecto.

##### `ANALISIS.md`
- **Propósito:** análisis argumentado integral de todos los componentes.
- **Metodología implicada:** revisión documental de código, datos, visuales y salidas narrativas.
- **Hallazgos clave:** explicita dependencias internas, coherencia metodológica y límites del pipeline.
- **Conclusión:** fortalece la calidad de entrega universitaria al transparentar cómo cada artefacto aporta al objetivo final.

#### 3.2 Fuente de datos principal

##### `scopus.csv` (119 filas, 45 columnas)
- **Propósito:** dataset maestro bibliográfico.
- **Metodología implicada:** ingestión de metadatos Scopus (autores, año, fuente, resumen, keywords, etc.) para análisis bibliométrico y NLP.
- **Hallazgos clave:**
  - ventana temporal 2023–2026;
  - producción anual: 2023 (7), 2024 (36), 2025 (57), 2026 (19);
  - predominio de keywords: *generative artificial intelligence* (106), *artificial intelligence* (26), *chatgpt* (23), *higher education* (23).
- **Conclusión:** sustenta empíricamente la hipótesis de aceleración del campo y habilita la totalidad de productos analíticos.

#### 3.3 Notebooks analíticos

##### `notebooks/Fase_4_Diseño_y_construcción_de_dashboard_de_inteligencia_de_negocios.ipynb`
- **Propósito:** notebook operativo principal para construir salidas de fase 4.
- **Metodología implicada:**
  - limpieza y normalización del dataset;
  - extracción de métricas bibliométricas;
  - generación de visualizaciones (Plotly, Matplotlib, PyVis/NetworkX);
  - análisis VADER sobre `search_text`;
  - exportación de artefactos (`.csv`, `.png`, `.html`, `.md`, `.txt`).
- **Hallazgos clave:** produce archivos nucleares del repositorio (`pubs_per_year.html`, `keyword_trends.html`, `sentiment_distribution.png`, `sentiment_vader_per_doc.csv`, etc.).
- **Conclusión:** constituye el núcleo de reproducibilidad técnica del proyecto.

##### `notebooks/cuaderno_final.ipynb`
- **Propósito:** consolidación final con enfoque comparativo y narrativo.
- **Metodología implicada:** combinación de serie temporal (ARIMA) y aprendizaje supervisado (RandomForest), más síntesis para reporte.
- **Hallazgos clave:** integra resultados de sentimiento y pronóstico en una narrativa de estrategia/KPI.
- **Conclusión:** funciona como puente entre análisis técnico y toma de decisiones.

#### 3.4 Dashboard y documento ejecutivo

##### `dashboard/Dashboard.html`
- **Propósito:** tablero ejecutivo interactivo final.
- **Metodología implicada:** front-end estático (HTML/CSS/JS + Chart.js) con KPIs, gráficos y secciones narrativas tipo LLM.
- **Hallazgos clave:**
  - 119 documentos (2023–2026);
  - pico 2025 (57 publicaciones);
  - keyword dominante: Generative AI (106/119);
  - componente estratégico con recomendaciones priorizadas.
- **Conclusión:** artefacto de comunicación ejecutiva que traduce resultados técnicos a lenguaje de decisión.

##### `documentos/Dashboard de Inteligencia Científica — IA Generativa.pdf`
- **Propósito:** versión portable y evaluable del dashboard.
- **Metodología implicada:** exportación a PDF del tablero, preservando KPIs y narrativa principal.
- **Hallazgos clave:** encapsula en 2 páginas los indicadores, contexto y lectura estratégica.
- **Conclusión:** útil para presentación formal y entrega académica.

#### 3.5 Visualizaciones interactivas complementarias

##### `coauthorship_top.html`
- **Propósito:** red de coautoría interactiva.
- **Metodología implicada:** grafo de colaboración con nodos y aristas ponderadas (vis-network/PyVis).
- **Hallazgos clave:** identifica núcleos de colaboración y autores puente.
- **Conclusión:** agrega dimensión estructural (red) al análisis meramente frecuencial.

##### `keyword_trends.html`
- **Propósito:** evolución temporal de keywords principales.
- **Metodología implicada:** gráfico interactivo Plotly con series por término.
- **Hallazgos clave:** persistencia de *generative artificial intelligence* y emergencia de términos asociados a educación y ética.
- **Conclusión:** permite vigilancia tecnológica temática de manera dinámica.

##### `pubs_per_year.html`
- **Propósito:** visualización interactiva de publicaciones por año.
- **Metodología implicada:** serie temporal Plotly generada desde agregación anual.
- **Hallazgos clave:** confirma crecimiento fuerte hasta 2025 y ajuste en 2026 (año en curso).
- **Conclusión:** soporta la tesis de aceleración reciente del campo.

#### 3.6 Series de apoyo para pronóstico

##### `outputs_train_series.csv`
- **Propósito:** segmento de entrenamiento para modelo de publicaciones.
- **Metodología implicada:** separación temporal de la serie (`2023: 7`).
- **Hallazgos clave:** tamaño extremadamente reducido.
- **Conclusión:** evidencia limitación de robustez estadística para modelado predictivo.

##### `outputs_test_series.csv`
- **Propósito:** segmento de validación (`2024: 36`, `2025: 57`, `2026: 19`).
- **Metodología implicada:** evaluación fuera de muestra.
- **Hallazgos clave:** patrón no lineal con caída 2026.
- **Conclusión:** sugiere prudencia al interpretar forecast con pocos puntos temporales.

#### 3.7 Gráficos de series y pronóstico

##### `outputs_pubs_time_series.png`
- **Propósito:** serie temporal estática de publicaciones/año.
- **Metodología implicada:** line plot (Matplotlib/Seaborn).
- **Hallazgos clave:** trayectoria ascendente 2023→2025 y descenso en 2026.
- **Conclusión:** visualmente consistente con agregaciones del dataset maestro.

##### `outputs_forecast_comparison.png`
- **Propósito:** comparación histórico vs test (y marco de forecast).
- **Metodología implicada:** superposición de series observadas/modeladas.
- **Hallazgos clave:** muestra comportamiento real y sirve como chequeo visual de ajuste.
- **Conclusión:** aporta validación cualitativa, aunque no sustituye métricas numéricas confiables.

##### `outputs_forecast_report.pdf`
- **Propósito:** reporte textual de pronóstico.
- **Metodología implicada:** generación automática (ReportLab) desde resultados del notebook final.
- **Hallazgos clave:** registra `MAE/RMSE/MAPE = NaN` para ARIMA y RF en el estado actual.
- **Conclusión:** identifica una brecha metodológica: falta robustecer evaluación por escasez de datos o pipeline incompleto.

#### 3.8 Salidas NLP y sentimiento

##### `sentiment_vader_per_doc.csv` (31 filas, 51 columnas)
- **Propósito:** resultados por documento del análisis VADER.
- **Metodología implicada:** construcción de `search_text` y cálculo de `neg`, `neu`, `pos`, `compound`, `compound_label`.
- **Hallazgos clave:** distribución actual 100% `positive` (31/31), con `compound` alto (media ≈ 0.93).
- **Conclusión:** evidencia sesgo hacia positividad en la muestra filtrada o en la configuración del proceso de clasificación.

##### `sentiment_summary (1).csv`
- **Propósito:** resumen agregado de etiquetas de sentimiento.
- **Metodología implicada:** conteo y porcentaje por clase.
- **Hallazgos clave:** solo aparece clase positiva (`31`, `100%`).
- **Conclusión:** consistente con el archivo por documento; requiere validación crítica para evitar sobreoptimismo interpretativo.

##### `sentiment_distribution.png`
- **Propósito:** gráfico de barras del resumen VADER.
- **Metodología implicada:** visualización categórica de frecuencias.
- **Hallazgos clave:** barra dominante positiva y ausencia de neutrales/negativas en este corte.
- **Conclusión:** comunica de forma inmediata el sesgo de distribución de la muestra procesada.

##### `representative_abstracts.csv`
- **Propósito:** selección de abstracts representativos para lectura cualitativa.
- **Metodología implicada:** muestreo por etiqueta desde salida VADER.
- **Hallazgos clave:** incluye ejemplos enfocados en adopción, ética, capacitación y práctica docente.
- **Conclusión:** complementa la métrica automática con evidencia textual interpretativa.

##### `wordcloud_positive.png` y `wordcloud_positive (1).png`
- **Propósito:** nube de términos de abstracts positivos.
- **Metodología implicada:** tokenización + remoción de stopwords + ponderación por frecuencia.
- **Hallazgos clave:** términos prominentes: *artificial intelligence*, *student*, *education*, *tools*, *integration*, *challenge*.
- **Conclusión:** corrobora semánticamente el foco temático del corpus y la centralidad de la dimensión educativa.

#### 3.9 Visualizaciones nuevas incorporadas

##### `visualizaciones/Top HECHO por suma de EVENTOS.png`
- **Propósito:** ranking de hecho por suma de eventos.
- **Metodología implicada:** agregación y gráfico de barras horizontal.
- **Hallazgos clave:** destaca un hecho dominante (`Desplazamiento forzado`) con magnitud muy superior.
- **Conclusión:** identifica concentración temática de alta intensidad en el conjunto de eventos.

##### `visualizaciones/Estimacion de densidad (KDE) de EVENTOS.png`
- **Propósito:** distribución de densidad de eventos.
- **Metodología implicada:** KDE para observar concentración y cola de la distribución.
- **Hallazgos clave:** fuerte concentración en valores bajos y cola larga a la derecha.
- **Conclusión:** sugiere asimetría y potencial presencia de valores extremos.

##### `visualizaciones/Eventos (suma) por VIGENCIA.png`
- **Propósito:** evolución temporal de eventos por vigencia.
- **Metodología implicada:** serie temporal anual con puntos y línea.
- **Hallazgos clave:** crecimiento, pico histórico y posterior desaceleración en años recientes.
- **Conclusión:** habilita lectura de ciclos temporales para priorización de políticas o monitoreo.

### 4) Relaciones entre componentes

La arquitectura del repositorio responde a una lógica de capas:

1. **Capa de datos:** `scopus.csv`.
2. **Capa de procesamiento:** notebooks (`Fase_4...ipynb`, `cuaderno_final.ipynb`).
3. **Capa de salidas analíticas:** CSVs, PNGs, HTML interactivos y PDF de resultados.
4. **Capa de comunicación:** `dashboard/Dashboard.html`, `documentos/*.pdf`, `README.md`, `ANALISIS.md`.

Relaciones críticas:
- `scopus.csv` alimenta bibliometría y NLP.
- El notebook de fase 4 exporta gran parte de outputs usados por dashboard y anexos.
- El notebook final integra pronóstico y narrativa estratégica.
- El dashboard sintetiza KPIs y lectura ejecutiva de todas las capas previas.

### 5) Flujo de trabajo del proyecto

#### 5.1 Flujo técnico reproducible

1. Ingesta de `scopus.csv`.
2. Limpieza/normalización de campos (`Year`, autores, keywords, resumen).
3. Agregaciones bibliométricas (por año, fuente, keyword, coautoría).
4. Análisis NLP con VADER sobre texto enriquecido.
5. Generación de artefactos:
   - tabulares (`*.csv`);
   - visuales (`*.png`, `*.html`);
   - reportes (`*.pdf`, narrativas).
6. Integración ejecutiva en dashboard y documentación final.

#### 5.2 Flujo analítico-interpretativo

- **Descriptivo:** cuantifica volumen y evolución de producción científica.
- **Estructural:** identifica nodos/relaciones en colaboración académica.
- **Semántico-afectivo:** caracteriza tono discursivo en abstracts.
- **Estratégico:** traduce hallazgos en recomendaciones y KPIs.

### 6) Hallazgos globales y conclusión académica

1. **Maduración acelerada del campo** (pico 2025) con fuerte centralidad de IA generativa aplicada a educación.
2. **Convergencia temática** en adopción, ética, privacidad y formación docente.
3. **Capacidad de comunicación ejecutiva** sólida vía dashboard y documento PDF.
4. **Limitación metodológica visible** en forecast (métricas NaN y serie muy corta), que debe tratarse como línea de mejora.
5. **Valor académico del repositorio:** integra ciencia de datos aplicada, NLP y diseño de tablero en un producto coherente de inteligencia de negocio.

En síntesis, el repositorio cumple con una estructura de proyecto universitario robusta en su dimensión descriptiva y de visualización estratégica, y deja explícita una agenda de mejora en validación predictiva para futuras iteraciones.
