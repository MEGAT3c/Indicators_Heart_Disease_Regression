# Indicators_Heart_Disease_Regression
### Hiperparámetros seleccionados 

- max_iter=1000



  - Justificación:
  - Por defecto, max_iter en la regresión logística es 100. Sin embargo, si el conjunto de datos es grande o si la convergencia del optimizador no se alcanza con facilidad, el número de iteraciones predeterminado puede no ser suficiente.
En este caso, el conjunto de datos es considerablemente grande (más de 300,000 registros). Por eso se aumenta a 1000, para asegurar que el modelo tenga suficiente tiempo para converger y optimizar los coeficientes sin detenerse prematuramente.


- random_state=42
  - Justificación:
  - Se utiliza un random_state fijo (42 en este caso) para garantizar la reproducibilidad de los resultados. Esto significa que cada vez que entrenamos el modelo, el conjunto de datos se dividirá de la misma manera, lo que permite obtener los mismos resultados al ejecutar el código varias veces.
- Hiperparámetros no ajustados (valores predeterminados)
solver:

  - Predeterminado: 'lbfgs' (Limited-memory BFGS)
   -El algoritmo 'lbfgs' es un buen punto de partida porque es eficiente en términos de memoria y adecuado para conjuntos de datos de tamaño medio a grande, como el de este caso. No se ha ajustado explícitamente ya que en este escenario no se espera que haya una mejora significativa con otros algoritmos (como 'saga' o 'liblinear').
  - C (Regularización inversa):
  - Predeterminado: C=1.0

   - No se ha modificado en esta implementación básica porque el valor predeterminado de C=1.0 ofrece un equilibrio razonable entre ajuste y generalización para muchos problemas. Sin embargo, en un entorno de producción, podría ser útil afinar este valor usando técnicas de validación cruzada.
- Validación cruzada
Aunque no se ha utilizado explícitamente en este código, ya que  los datos se dividieron en conjunto de entrenamiento, validación y prueba, lo cual permite evaluar el rendimiento y ajustar el modelo en el conjunto de validación antes de probarlo en el conjunto de prueba.
