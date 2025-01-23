# Proyecto de Análisis de Ventas de Dirty Cafe

Este repositorio contiene un proyecto completo de Ciencia de Datos cuyo objetivo es limpiar, analizar y modelar un conjunto de datos sucio que simula las ventas de un café. El conjunto de datos está intencionadamente desordenado, con valores faltantes, inconsistencias y errores, lo que ofrece un escenario realista para la limpieza de datos y el aprendizaje automático.

---

## 📂 Estructura del Proyecto

```
├── data/
│   └── dirty_cafe_sales.csv    # Conjunto de datos utilizado en el proyecto
├── src/
│   └── cafesales.ipynb         # Cuaderno original de exploración de datos
│   ├──requirements.txt            # Dependencias de Python
└──    README.md                   # Documentación del proyecto
```

---

## 📝 Descripción General del Proyecto

El conjunto de datos **Dirty Cafe Sales** contiene 10,000 filas de transacciones de ventas sintéticas. Incluye desafíos como:
- **Valores faltantes**: Columnas como `Item`, `Quantity`, `Price Per Unit` y `Transaction Date` contienen `NaN`, `ERROR` o `UNKNOWN`.
- **Datos inconsistentes**: Errores en columnas numéricas y categóricas.
- **Problemas del mundo real**: Requiere ingeniería de características y limpieza de datos.

### Objetivos Clave
1. Realizar limpieza de datos y transformación para hacer que el conjunto de datos sea utilizable.
2. Realizar un análisis exploratorio de datos (EDA) para descubrir tendencias e información relevante.
3. Entrenar y evaluar modelos de aprendizaje automático para predecir `Total Spent`.

---

## 📊 Análisis y Resultados

### Limpieza de Datos
- Los valores faltantes y los valores inválidos (`ERROR`, `UNKNOWN`) fueron reemplazados por `NaN`.
- Se utilizó imputación por KNN para las columnas numéricas, y las columnas categóricas se rellenaron con la moda.
- `Transaction Date` fue convertida a `datetime`, y se crearon nuevas características (`Year`, `Month`, `Day`, `DayOfWeek`).

### Modelos de Aprendizaje Automático
Se evaluaron tres modelos para predecir `Total Spent`:
1. **Regresión Lineal**:
   - MSE: 3.3176099
   - R²: 0.9055234
2. **K-Nearest Neighbors (KNN)**:
   - MSE: 1.60175
   - R²: 0.9543864
3. **XGBoost**:
   - MSE: 0.267172
   - R²: 0.992391

**Conclusión**: XGBoost superó a los otros modelos y se recomienda para futuras predicciones.

---

## 📈 Principales Insights
1. Los productos más populares fueron **Café** y **Sándwich**.
2. Existe una fuerte relación lineal entre `Quantity` y `Total Spent`.
3. Los datos limpiados permitieron una predicción más precisa de los totales de las transacciones.

---

## 🚀 Cómo Ejecutar el Proyecto

### Requisitos Previos
1. Instalar Python 3.8 o superior.
2. Clonar el repositorio:
   ```bash
   git clone https://github.com/your-username/dirty-cafe-sales.git
   cd dirty-cafe-sales
   ```
3. Instalar las dependencias:
   ```bash
   pip install -r requirements.txt
   ```

### Ejecutando el Proyecto
Para ejecutar el análisis y el modelado de datos, abre y ejecuta el archivo Jupyter Notebook `notebooks/cafesales.ipynb`:

```bash
jupyter notebook notebooks/cafesales.ipynb
```

---

## 📂 Descripción del Conjunto de Datos

| Nombre de la Columna   | Descripción                                               | Ejemplos de Valores   |
|------------------------|-----------------------------------------------------------|-----------------------|
| `Transaction ID`        | Identificador único de cada transacción                   | `TXN_1234567`         |
| `Item`                  | Artículo comprado (puede contener valores faltantes/inválidos) | `Café`, `ERROR`       |
| `Quantity`              | Cantidad del artículo comprado                            | `1`, `3`, `UNKNOWN`   |
| `Price Per Unit`        | Precio de un solo artículo                                | `2.00`, `4.00`        |
| `Total Spent`           | Monto total gastado (`Quantity` × `Price Per Unit`)       | `8.00`, `12.00`       |
| `Payment Method`        | Método de pago utilizado                                  | `Efectivo`, `UNKNOWN` |
| `Location`              | Ubicación de la transacción                               | `En tienda`, `ERROR`  |
| `Transaction Date`      | Fecha de la transacción                                   | `2023-01-01`          |

---

## 🌟 Características

- **Limpieza de Datos**: Maneja valores faltantes, entradas inválidas e inconsistencias en los formatos de datos.
- **Análisis Exploratorio**: Identifica patrones, tendencias e información relevante.
- **Modelos de Aprendizaje Automático**: Predice `Total Spent` utilizando Regresión Lineal, KNN y XGBoost.

---

## 🛠️ Tecnologías Utilizadas

- **Python**: Lenguaje de programación principal.
- **Pandas**: Manipulación y limpieza de datos.
- **Seaborn & Matplotlib**: Visualización de datos.
- **Scikit-learn**: Modelos de aprendizaje automático y evaluación.
- **XGBoost**: Modelado predictivo avanzado.
- **Jupyter Notebook**: Plataforma para el análisis interactivo de datos.

---

## 🤝 Contribución

¡Las contribuciones son bienvenidas! Siéntete libre de bifurcar este repositorio, crear una nueva rama y enviar un pull request.

---

## 📄 Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

---

## 📬 Contacto

Para cualquier pregunta o sugerencia, por favor contacta:
- Correo electrónico: izanfabrica2022@gmail.com
- GitHub: 0xfabrica (https://github.com/0xfabrica)
```
