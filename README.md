# Análisis de Observación de la Tierra (EO)
## Evolución del Espejo de Agua de la Laguna de Fúquene (1985–2024)

---

## Executive Summary

Este proyecto analiza la evolución del espejo de agua de la Laguna de Fúquene durante casi 40 años utilizando datos satelitales y Google Earth Engine.  
Más que replicar cifras oficiales, el enfoque del análisis está en evaluar cómo distintas decisiones metodológicas, limitaciones de los sensores y vacíos de datos influyen en los resultados obtenidos a partir de Observación de la Tierra (EO).

El proyecto demuestra capacidad para:
- Construir análisis reproducibles con datos reales
- Identificar y explicar discrepancias entre estimaciones satelitales y datos oficiales
- Tomar decisiones técnicas informadas frente a datos incompletos
- Reconocer los límites del dato y ajustar el enfoque analítico

---

## 1. Introducción

La Laguna de Fúquene es uno de los cuerpos de agua más importantes del altiplano cundiboyacense y ha experimentado cambios significativos en su extensión superficial a lo largo del tiempo.

Este proyecto busca analizar su evolución espacial y temporal utilizando datos satelitales históricos, priorizando la consistencia metodológica y la interpretación crítica de los resultados.

---

## 2. ¿Qué es Observación de la Tierra (EO)?

La Observación de la Tierra (Earth Observation, EO) consiste en el uso de sensores satelitales, aéreos o terrestres para monitorear fenómenos físicos del planeta.

En este proyecto, EO se utiliza para:
- Detectar agua superficial mediante información espectral
- Analizar cambios temporales a largo plazo
- Evaluar la calidad y confiabilidad de los datos satelitales

Es importante destacar que EO no proporciona valores exactos, sino estimaciones dependientes del sensor, la resolución espacial y las decisiones de procesamiento.

---

## 3. Área de estudio

El área de estudio corresponde a la Laguna de Fúquene, Colombia.  
Se definió un polígono (ROI) que cubre la extensión completa conocida del cuerpo lagunar.

Durante el desarrollo del proyecto se detectó que versiones iniciales del polígono solo cubrían parcialmente la laguna, lo que generaba subestimaciones importantes del área. La corrección de este aspecto fue clave para mejorar la calidad del análisis.

---

## 4. Selección de datos satelitales

### 4.1 ¿Por qué Landsat?

Aunque Sentinel-2 ofrece una mejor resolución espacial, el análisis principal se basa en Landsat debido a razones metodológicas fundamentales:

- Landsat ofrece una serie temporal continua desde 1984
- Permite analizar casi 40 años sin cambiar de sensor
- Reduce inconsistencias introducidas por diferencias instrumentales
- Sentinel-2 solo está disponible desde 2015

Para un análisis de largo plazo, la consistencia temporal es más importante que la resolución espacial.

Se utilizaron datos de Landsat 5, 7 y 8.

---

## 5. Metodología

### 5.1 Detección de agua superficial

El espejo de agua se estimó utilizando el Índice Normalizado de Diferencia de Agua (NDWI), calculado a partir de las bandas verde e infrarrojo cercano.

Este índice se basa en que:
- El agua refleja más radiación en el rango verde
- El agua absorbe fuertemente en el infrarrojo cercano

Se aplicó un umbral para clasificar píxeles como agua dentro del polígono de estudio.

---

### 5.2 Cálculo del área

El área de la laguna se calculó mediante:
1. Conteo de píxeles clasificados como agua
2. Multiplicación por el área de cada píxel
3. Conversión de metros cuadrados a kilómetros cuadrados

Este enfoque implica limitaciones importantes relacionadas con la resolución espacial y la nubosidad.

---

## 6. Datos faltantes y limitaciones

Durante el análisis se identificaron:
- Años completos sin observaciones válidas
- Meses sin datos debido a nubosidad
- Valores atípicos causados por fallas del sensor o ausencia de píxeles detectables

Estos datos faltantes no fueron interpolados, ya que forman parte del análisis y evidencian las limitaciones reales de la Observación de la Tierra.

---

## 7. Resultados principales

- Las áreas estimadas son menores que las reportadas por fuentes oficiales
- La tendencia temporal es coherente, pero el valor absoluto depende de la metodología
- El análisis mensual introduce demasiado ruido y vacíos de datos
- La visualización mediante mapas cada 5 años permite interpretar mejor los cambios espaciales

---

## 8. Decisiones metodológicas clave

- Priorizar consistencia temporal sobre resolución espacial
- Utilizar datos anuales en lugar de mensuales
- No forzar interpolaciones sobre datos faltantes
- Enfocar el análisis en el razonamiento y no en ajustar cifras

---

## 9. Aprendizajes

Este proyecto permitió comprender que:
- Más resolución no siempre implica mejores resultados
- Las discrepancias con datos oficiales son informativas
- Resolver un problema implica saber cuándo cambiar de enfoque
- La interpretación crítica del dato es tan importante como el código

---

## 10. Posibles extensiones

- Integración de datos de precipitación (CHIRPS)
- Análisis multiesensor para periodos recientes
- Comparación crítica con datos oficiales
- Clasificación basada en aprendizaje automático

---

## 11. Tecnologías utilizadas

- Google Earth Engine
- Python
- geemap
- pandas
- matplotlib
- Datos Landsat (USGS)

---

## Autor

Miguel Correa  
Proyecto académico y de portafolio enfocado en análisis geoespacial y Observación de la Tierra.

📧 Contact: bochicasimijaca@gmail.com

🔗 GitHub: https://github.com/Bochika
