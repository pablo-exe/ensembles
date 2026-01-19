# Ensembles: Bagging y Boosting

Este proyecto estudia de forma **experimental y conceptual** el comportamiento de métodos *ensemble* en aprendizaje automático, concretamente **Bagging** y **Boosting**, comparándolos con un **modelo base** (árbol de decisión).

El objetivo principal no es únicamente obtener métricas, sino **entender cómo y por qué cambian** el rendimiento medio y la estabilidad de los modelos al aplicar distintas estrategias ensemble.

---

## Objetivos del proyecto

* Analizar el comportamiento de un **árbol de decisión** como modelo base.
* Estudiar el impacto de **Bagging** en:

  * Accuracy media
  * Variabilidad de los resultados (desviación típica)
* Analizar cómo influyen:

  * El número de estimadores
  * El tamaño de muestra por estimador
* Comprender el funcionamiento y las ventajas de **Boosting** (Gradient Boosting).
* Comparar Bagging y Boosting desde un punto de vista **conceptual y empírico**.

---

## Metodología

### Evaluación

Todos los modelos se evalúan mediante **validación cruzada estratificada y repetida**, manteniendo constantes las condiciones experimentales para permitir comparaciones justas.

Las métricas empleadas son:

* **Clasificación**:

  * Accuracy (media y desviación típica)
* **Regresión**:

  * R² (coeficiente de determinación)
  * MAE (error absoluto medio)

La evaluación se realiza siempre sobre **datos no vistos** para medir capacidad de generalización.

---

## Estructura del proyecto

* **Modelo base**

  * Árbol de decisión como referencia
  * Análisis de rendimiento y variabilidad

* **Bagging (Bootstrap Aggregation)**

  * Comparación con el modelo base
  * Estudio del efecto del número de estimadores
  * Análisis del impacto del submuestreo
  * Observación de la estabilidad del modelo

* **Boosting (Gradient Boosting)**

  * Aplicación en clasificación y regresión
  * Estudio del efecto del número de estimadores
  * Análisis de reducción de error y aumento de capacidad

---

## Principales conclusiones

* **Bagging** tiende a:

  * Mejorar el rendimiento medio del modelo base
  * Reducir la sensibilidad a decisiones accidentales del entrenamiento
  * Mostrar rendimientos decrecientes al aumentar el número de estimadores

* **Boosting**:

  * Aprende de forma secuencial corrigiendo errores previos
  * Reduce el sesgo de manera progresiva
  * Puede lograr mejoras sustanciales de rendimiento
  * Presenta riesgo de sobreajuste si no se controla la complejidad

* La **desviación típica** es tan importante como la media para interpretar resultados.

---

## Ideas clave

* Un ensemble no garantiza mejores métricas en todos los escenarios, pero sí **resultados más interpretables**.
* Bagging y Boosting atacan problemas distintos:

  * Bagging reduce varianza
  * Boosting reduce sesgo
* La reproducibilidad y la evaluación consistente son esenciales en experimentos de ML.

---

## Requisitos

* Python 3.x
* scikit-learn
* numpy

---

## Notas finales

Este proyecto prioriza la **comprensión profunda de los métodos ensemble** sobre la optimización directa de métricas. Todas las conclusiones se basan en experimentos reproducibles y en el análisis conjunto de rendimiento medio y variabilidad.
