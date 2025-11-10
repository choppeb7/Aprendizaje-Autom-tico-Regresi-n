## 🧾 Checklist para elaborar un modelo de regresión lineal

### 🔍 1. Exploración inicial de datos
- Revisar la estructura del dataset (`.info()`, `.describe()`).
- Analizar la distribución de las variables mediante **histogramas**.
- Calcular la **matriz de correlaciones** (y visualizar con un heatmap).
- Identificar posibles **relaciones lineales** entre predictores y la variable objetivo.

---

### 🧹 2. Limpieza y preparación de datos
- Detectar y tratar **valores atípicos (outliers)** con boxplots o z-scores.  
- Tratar los **valores faltantes** (imputar o eliminar según el caso).
- Verificar el **tipo de dato** de cada variable (numérica, categórica).
- Crear variables dummy para las **categóricas** (`pd.get_dummies()`).

---

### 🔄 3. Transformación de variables
- Aplicar **transformaciones** para corregir asimetrías (log, raíz cuadrada, Box-Cox).  
- Escalar o normalizar si las variables tienen **rangos muy diferentes**.  
- Considerar **interacciones** o **términos polinómicos** si hay relaciones no lineales leves.

---

### 📉 4. Construcción del modelo
- Dividir los datos en **entrenamiento y prueba** (train/test split).  
- Ajustar el modelo con `statsmodels` o `sklearn`.  
- Revisar los **coeficientes y significancia estadística** (p-valores, intervalos de confianza).  
- Evaluar la multicolinealidad (VIF).

---

### 📊 5. Evaluación del modelo
- Revisar métricas: **R², R² ajustado, RMSE, MAE**.  
- Analizar **residuos**: deben tener media ≈ 0, varianza constante y distribución aproximadamente normal.  
- Verificar que no haya **heterocedasticidad** ni **autocorrelación** (Durbin–Watson, Breusch–Pagan).

---

### ⚙️ 6. Refinamiento
- Eliminar variables irrelevantes o altamente correlacionadas.  
- Probar modelos alternativos (interacciones, transformaciones).  
- Validar con **cross-validation** si es posible.  
- Documentar las decisiones tomadas en limpieza y modelado.

---

✅ **Consejo final:** un buen modelo lineal no solo predice bien, sino que **cumple los supuestos estadísticos** y tiene **interpretabilidad**.

