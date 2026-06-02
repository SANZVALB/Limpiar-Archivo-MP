# Limpieza de Archivo Mercado Pago

Aplicación web para procesar, limpiar y analizar archivos CSV exportados desde Mercado Pago.

Permite separar automáticamente registros relevantes de operaciones internas o no deseadas, generando archivos listos para análisis financiero o conciliación.

---

## 🚀 Qué hace

La herramienta permite:

- Subir un archivo CSV
- Analizar automáticamente su contenido
- Filtrar registros según criterios definidos
- Separar en dos grupos:
  - ✅ Registros limpios (válidos)
  - ❌ Registros eliminados
- Calcular:
  - Cantidad de filas totales
  - Registros limpios
  - Registros eliminados
  - Monto limpio (ARS)
  - Monto eliminado (ARS)
- Descargar resultados en formato CSV

---

## 📁 Uso

1. Subir o arrastrar un archivo `.csv`
2. El sistema procesa automáticamente
3. Visualizar resultados en pantalla
4. Descargar:
   - `*_Limpio.csv`
   - `*_Eliminados.csv`

---

## 🧠 Lógica de limpieza

Se eliminan filas cuya **primera columna** coincide con alguno de los siguientes patrones:

- `88 xx`
- `200001460`
- `MP-Q`
- `Venta`
- `MELIPAYMENTS-COLLECTIONATTEMPT`
- `INSTORE-`

---

## 💰 Cálculo de montos

- Se usa la columna: `TRANSACTION_AMOUNT`
- Se soportan formatos:
  - `1234.56`
  - `1234,56`
  - `1.234,56`
- Se normaliza automáticamente antes de calcular

---

## ⚙️ Procesamiento del CSV

El sistema incluye un parser manual capaz de manejar:

- Filas completas entre comillas:
  `"col1,col2,col3,..."`
- Campos con comillas escapadas:
  `"texto ""interno"""`
- CSV estándar y CSV exportado por sistemas financieros

Todo el procesamiento se realiza en el navegador (sin servidor).

---

## 🖥️ Interfaz

- Drag & Drop de archivos
- Feedback visual del archivo cargado
- Visualización de métricas
- Descarga directa de resultados

---

## ⚠️ Limitaciones

- Solo soporta archivos separados por coma `,`
- No maneja saltos de línea dentro de celdas
- Requiere que exista la columna `TRANSACTION_AMOUNT`

---

## 🛠️ Tecnologías

- HTML
- CSS
- JavaScript (Vanilla)

---

## 📌 Autor

SANZVAL
## URL
https://sanzvalb.github.io/Limpiar-Archivo-MP/csv_cleaner_html.html
``
# https://sanzvalb.github.io/Limpiar-Archivo-MP/csv_cleaner_html.html
