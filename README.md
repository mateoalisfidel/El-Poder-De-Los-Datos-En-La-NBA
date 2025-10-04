# Análisis avanzado de la NBA

## Objetivo
El objetivo de este trabajo es analizar las estadísticas de jugadores de la NBA para **condensar decenas de métricas** (puntos, rebotes, asistencias, etc.) en unas pocas componentes principales que expliquen
la mayor parte de la variabilidad. Esto permite:  

- Visualizar perfiles de juego de los jugadores  
- Detectar jugadores atípicos  
- Segmentar jugadores en tipos como tiradores, interiores u organizadores  

Además, se realiza un **clustering** útil para los General Managers de las franquicias, para poder tener un recambio de un jugador que quisieran fichar pero al final no se diera a cabo. 

Por último, se aplica un modelo de **PLS-DA** para predecir qué jugadores tienen más probabilidades de ser **All-Star**, ayudando a entender el potencial de cada jugador en la liga.

---

## Datos
- Dataset completo: `nba_2022_2023.csv`, con estadísticas de cada jugador: puntos, rebotes, asistencias, tiros, porcentaje de tiro, triples, tiros libres, robos, tapones, pérdidas y faltas.  
- Para el **PCA**, se utilizaron variables ajustadas por partido 
---

## Metodología
1. **Limpieza de datos**: preparación y filtrado de los datasets (`Rmd/limpieza.Rmd`)  
2. **Análisis exploratorio de datos (EDA)**  
3. **Reducción de dimensionalidad**: PCA (`Rmd/pca.Rmd`)  
4. **Clustering de jugadores** (`Rmd/clustering.Rmd`)  
5. **Modelado predictivo**: PLS-DA (`Rmd/pls.Rmd`)  
6. **Visualización de resultados y conclusiones**: se genera en `Rmd/trabajo_nba.Rmd`, que **combina de forma resumida los tres análisis anteriores** y produce las visualizaciones y conclusiones,
    exportadas luego al PDF (`docs/proyecto-nba.pdf`)

---

## Resultados
- Identificación de patrones de rendimiento de jugadores  
- Jugadores con influencia en el juego y estilos similares para ayudar a los General Managers a tomar decisiones.
- Predicción de All-Stars con métricas de evaluación 
- PDF con el informe completo en `docs/proyecto-nba.pdf`

---

## Tecnologías
- **Lenguajes y herramientas**: R  
- **Librerías principales utilizadas en R**:  
  - **Análisis estadístico y PCA**: FactoMineR, factoextra, ropls  
  - **Manipulación de datos**: dplyr, tidyr  
  - **Clustering**: cluster, NbClust  
  - **Visualización**: ggplot2, ggrepel  
- **Áreas de interés y práctica**: Machine Learning, Análisis Predictivo, PCA, PLS, Clustering, Regresión y Visualización de datos

---

## Cómo ejecutar
1. Abrir los archivos `.Rmd` en RStudio  
2. Instalar las librerías necesarias (`requirements.txt`)  
3. Ejecutar cada R Markdown en orden: limpieza → PCA → Clustering → PLS-DA. O ejecutar el archivo final directamente.

---

## Contacto
- LinkedIn: https://www.linkedin.com/in/mateoalisfidel/ 
- Email: mateo.alisfidel.data@gmail.com
