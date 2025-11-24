# Análisis del Desempeño de Bilibili Gaming - Worlds 2024 🏆

Este proyecto presenta un análisis estadístico exhaustivo sobre el desempeño del equipo **Bilibili Gaming (BLG)** en el *League of Legends World Championship 2024*. El informe combina técnicas de estadística descriptiva e inferencial para identificar los factores claves que influyeron en sus resultados.

## 👥 Autores
*   **Valentina Fonseca**
*   **Cristian Pérez**
*   **Santiago Suarez**

## 📊 Metodología y Análisis
El informe fue generado utilizando **R** y **Knime/LaTeX** (`.Rnw`), integrando código y narrativa en un solo documento reproducible.

### Puntos Clave del Análisis:
1.  **Estadística Descriptiva**: Análisis exploratorio de KDA, Oro por Minuto y Tasas de Victoria por equipo y posición.
## Análisis Estadístico Avanzado
Se han incorporado nuevas técnicas para profundizar en el análisis:
- **ANOVA y Tukey HSD**: Para evaluar diferencias significativas en la obtención de oro entre posiciones.
- **Árboles de Decisión**:
  - **Regresión**: Para predecir el Win Rate basado en KDA, Oro y Eficiencia.
  - **Clasificación**: Para determinar las reglas que separan la victoria de la derrota.
- **Comparación de Modelos**: Evaluación del RMSE entre Regresión Lineal y Árboles.

## Conclusiones Principales
- **KDA es Rey**: Se confirmó que el KDA es el predictor más fuerte de la victoria. Un KDA > 6 asegura prácticamente la victoria.
- **Eficiencia Normal**: Contrario a hipótesis iniciales, la eficiencia de recursos de BLG (0.50) fue estadísticamente normal y consistente con el perfil de un equipo campeón.
- **Perfil de Campeón**: BLG no presentó debilidades estadísticas estructurales. Su derrota se atribuye a factores intangibles (estrategia, ejecución) más que a déficits numéricos.
2.  **Métrica Personalizada**: Desarrollo del indicador de **Eficiencia de Recursos ($E_R$)**, que mide el daño infligido por unidad de oro gastada.
3.  **Inferencia Estadística**:
    *   **Intervalos de Confianza (95%)**: Comparación del desempeño de BLG vs el promedio mundial.
    *   **Pruebas de Hipótesis**: T-tests para validar diferencias de rendimiento.
    *   **ANOVA**: Análisis de Varianza para demostrar cómo la posición (Top, Jungle, Mid, ADC, Support) determina estructuralmente la economía del juego.
4.  **Modelado Predictivo**:
    *   **Regresión Lineal Múltiple**: Modelo para explicar el *Win Rate* ($R^2_{adj} = 0.58$).
    *   **Diagnóstico de Residuos**: Validación de supuestos de linealidad y normalidad (Q-Q Plots).

## 🛠️ Tecnologías
*   **Lenguaje**: R
*   **Formato**: Rnw (R + LaTeX)
*   **Librerías Clave**: `ggplot2`, `dplyr`, `knitr`, `kableExtra`, `gridExtra`.

## 🚀 Cómo Reproducir
Para compilar el informe y generar el PDF:

1.  Asegúrate de tener instalado R y una distribución de LaTeX (como TinyTeX).
2.  Instala las dependencias en R:
    ```r
    install.packages(c("knitr", "dplyr", "ggplot2", "kableExtra", "gridExtra", "readr"))
    ```
3.  Compila el archivo `.Rnw`:
    ```r
    knitr::knit2pdf("informe_worldcup_lol-knitr.Rnw")
    ```
