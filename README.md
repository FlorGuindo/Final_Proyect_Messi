# Final_Proyect_Messi
# README: Análisis y Modelado de Goles de Messi en Clubes

## Tabla de Contenidos
1. [Introducción](#introducción)
2. [Declaración del Problema](#declaración-del-problema)
3. [Recolección de Datos](#recolección-de-datos)
4. [Limpieza y Preparación de los Datos](#limpieza-y-preparación-de-los-datos)
5. [Análisis Exploratorio de Datos](#análisis-exploratorio-de-datos)
6. [Ingeniería de Características](#ingeniería-de-características)
7. [Modelado y Evaluación](#modelado-y-evaluación)
8. [Visualización y Dashboard](#visualización-y-dashboard)
9. [Resultados y Discusión](#resultados-y-discusión)
10. [Conclusión](#conclusión)
11. [Trabajo Futuro](#trabajo-futuro)


---

## Introducción
Este proyecto analiza el rendimiento goleador de Lionel Messi a lo largo de su carrera en clubes. El objetivo principal fue construir un modelo predictivo capaz de estimar si Messi marcaría uno o más goles en un partido, así como identificar patrones clave que explican su éxito.

## Declaración del Problema
En el fútbol moderno, comprender el rendimiento de los jugadores es clave para optimizar decisiones deportivas y financieras. Este proyecto busca responder: ¿Cuáles son los factores determinantes para que Messi marque uno o más goles en un partido?

## Recolección de Datos
- **Fuente**: Dataset "Messi, Neymar, Ronaldo, Lewandowski All Goals" de Kaggle.

## Limpieza y Preparación de los Datos
- Conversión de fechas
- Clasificación de temporadas
- Regulizar el formato de los minutos
- Eliminación de columnas irrelevantes o duplicadas.
- Conversión de variables categóricas a ordinales (ej, nivel del oponente, matchday, venue).
- Transformación de la variable objetivo en binaria: 0 (1 gol) o 1 (más de 1 gol).

## Análisis Exploratorio de Datos
- Goles por temporada y lugar del partido.
- Relación entre días sin marcar y rendimiento goleador.
- Análisis del "días sin marcar óptimos" como métrica clave.

## Ingeniería de Características
- **Variables creadas**:
  - "Días sin marcar
  - Clasificación del oponente (preferido, normal, difícil).
  - Transformación de "Venue" a binario (local/visitante).
  - ¿Fue el gol del 1 a 0?
  - Conversión de "Season" a un valor numérico.

## Modelado y Evaluación
- **Modelos implementados**:
  1. OLS.
  2. Comparativa de Regression Tree, Linear Regression, KNN
  3. Comparativa de DecisionTreeClassifier, LogisticRegression, KNeighborsClassifier
  4. Random Forest Classifier (modelo final).
- **Evaluación**:
  - Random Forest obtuvo una accuracy del 0.74
  - "Season" resultó ser la variable más influyente seguida de "días sin marcar"

## Visualización y Dashboard
- **Dashboard en Power BI**: Incluye gráficos interactivos de goles por temporada, días sin marcar, calsificacion de instancias según competencias, clubes, momento del partido donde marcó, rivales favoritos y si fue el gol del 1 a 0
- **Gráfico destacado**: Relación entre goles totales y según días sin marcar.

## Resultados y Discusión
- Messi mantiene un rendimiento consistente a lo largo de los años.
- Los "días sin marcar" tienden a aumentar ligeramente con el tiempo.
- El modelo confirma que variables como la temporada, los dias sin marcar y las instancia del partido son claves.

## Conclusión
El proyecto demuestra cómo el análisis de datos puede ofrecer insights clave sobre el rendimiento de jugadores. Aunque los datos limitados restringieron el análisis completo, los resultados sientan una base para investigaciones futuras. Este mismo modelo y tipo de analisis podría aplicarse a más jugadores.

## Trabajo Futuro
- Incluir datos de partidos donde Messi no marcó para optimizar el modelo.
- Analizar partidos con la selección argentina.
- Investigar la evolución del rendimiento según la edad y contexto competitivo.


