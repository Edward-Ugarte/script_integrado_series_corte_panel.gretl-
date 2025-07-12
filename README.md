# script_integrado_series_corte_panel.gretl
README - Proyecto Econométrico Simulado en Gretl

Descripción general: Este proyecto contiene cuatro bloques econométricos ejecutados en Gretl con datos simulados. Cada bloque representa un tipo de análisis empírico clave: series de tiempo, corte transversal, panel de datos, y modelos de elección binaria. El objetivo principal es entender cómo variables económicas se relacionan, diagnostican y proyectan en distintos contextos de datos.

Bloque A: Series de Tiempo

Se simula el ingreso anual como una función del año con ruido aleatorio.

Modelo estimado: ingreso_st = β0 + β1·año + ε

Coeficiente temporal significativo (β1 ≈ 19.76)

R-cuadrado ≈ 0.993 (modelo explica casi toda la variación)

Se detecta autocorrelación en los residuos (Breusch-Godfrey), aunque los residuos son normales y la especificación es adecuada.

Bloque B: Corte Transversal

Se estudia cómo edad, educación y género explican el ingreso entre individuos.

Modelo: ingreso_ct = β0 + β1·edad + β2·educación + β3·género + ε

Coeficientes significativos, en especial educación (β2 ≈ 38.75) y género (β3 ≈ 403)

R-cuadrado ≈ 0.915

No hay colinealidad ni heterocedasticidad. La especificación es válida.

Bloque C: Panel de Datos

Se modela la producción logarítmica en función de capital y trabajo para distintas unidades a lo largo del tiempo.

Modelo: ln(output) = β0 + β1·ln(capital) + β2·ln(trabajo) + ε

Elasticidades estimadas ≈ 0.5 para ambos factores

R-cuadrado ≈ 0.999

Se ejecutan modelos combinados, efectos fijos y aleatorios

El test de Hausman sugiere que los efectos aleatorios son válidos (p ≈ 0.14)

Bonus: Modelos Probabilísticos

Se estima la probabilidad de que una persona trabaje según su edad y educación.

Modelos: MCO (referencial), Logit, y Probit

En Logit y Probit, educación tiene efecto positivo aunque no significativo

Clasificación correcta ≈ 68%

R-cuadrado de McFadden bajo (≈ 0.018)

Los residuos del modelo probit cumplen normalidad

Diagnósticos generales:

Multicolinealidad: no presente (VIFs bajos)

Heterocedasticidad: no significativa

Autocorrelación: presente solo en Bloque A

Normalidad: cumplida en series y modelos probabilísticos

Especificación: adecuada en todos los casos

Notas adicionales: Todos los bloques fueron construidos  y adecuados para cada estructura. Las variables fueron simuladas de forma controlada para reflejar relaciones teóricas conocidas, como la función Cobb-Douglas, la regresión salarial clásica, y decisiones de empleo.

