# TelecomX_LATAM-02-Machine-learning
# Predicción de Clientes (Churn/Comportamiento)

Este proyecto utiliza **Machine Learning** para predecir la probabilidad de que un cliente realice determinada acción (ej. churn, conversión, comportamiento financiero).  

Se probaron dos modelos principales:
- **Regresión Logística**
- **Random Forest**

El flujo del proyecto fue:

1. **Carga de datos**: Se cargó la base de datos original y se trató con limpieza de valores nulos y codificación de variables categóricas.  
2. **Análisis exploratorio (EDA)**: Se analizaron distribuciones, correlaciones y balance de clases.  
3. **Tratamiento de datos**: Normalización de las variables numéricas para la Regresión Logística.  
4. **Entrenamiento y validación**:
   - División en train/test con `train_test_split`.
   - Uso de métricas de evaluación: **accuracy**, **ROC AUC**, **precisión**, **recall**, **f1-score**, y **matriz de confusión**.
5. **Comparación de modelos**:
   - **Regresión Logística**: Exactitud 0.75, ROC AUC 0.84  
   - **Random Forest**: Exactitud 0.77, ROC AUC 0.82  

---

## Resultados

- **Regresión Logística**  
  - Ventajas: buen desempeño en **recall de la clase minoritaria**, interpretabilidad de coeficientes.  
  - Limitaciones: menor precisión global en la clase positiva.  

- **Random Forest**  
  - Ventajas: mejor **exactitud global** y balance en la predicción de ambas clases.  
  - Limitaciones: menos interpretable y ligeramente menor AUC que la regresión logística.  

En conclusión, ambos modelos son útiles:
- Si se requiere **maximizar la detección de casos positivos** (recall), la **Regresión Logística** es más adecuada.  
- Si se busca **un modelo más robusto en términos de exactitud general**, el **Random Forest** es preferible.  
