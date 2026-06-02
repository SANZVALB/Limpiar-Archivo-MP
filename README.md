# Limpieza de Archivo Mercado Pago

Aplicación web simple para procesar archivos CSV de Mercado Pago, limpiando registros no relevantes y generando archivos separados.

## 🚀 Qué hace

Permite subir un archivo `.csv` y automáticamente:

- Filtra filas según criterios predefinidos
- Separa en:
  - ✅ Registros válidos (limpios)
  - ❌ Registros eliminados
- Calcula:
  - Cantidad de registros
  - Monto total limpio
  - Monto eliminado
- Genera dos archivos descargables:
  - `*_Limpio.csv`
  - `*_Eliminados.csv`

---

## 📁 Uso

1. Subir un archivo CSV
2. El sistema procesa automáticamente
3. Descargar los resultados

---

## 🧠 Lógica de limpieza

Se eliminan filas que comienzan con alguno de los siguientes valores en la primera columna:

- `88 xx`
- `200001460`
- `MP-Q`
- `Venta`
- `MELIPAYMENTS-COLLECTIONATTEMPT`
- `INSTORE-`

---

## 💰 Cálculo de montos

- Se utiliza la columna `TRANSACTION_AMOUNT`
- El valor se normaliza para soportar:
  - formato con punto (`1234.56`)
  - formato con coma (`1234,56`)
  - formatos mixtos (`1.234,56`)

---

## ⚠️ Consideraciones técnicas

- El procesamiento se realiza totalmente en el navegador (no hay backend)
- El CSV puede contener campos entre comillas y caracteres especiales
- Se utiliza un parser manual para interpretar las filas

---

## 🛠️ Tecnologías

- HTML
- CSS
- JavaScript (vanilla)

---

## 📌 Autor

Desarrollado por SANZVAL
``
# https://sanzvalb.github.io/Limpiar-Archivo-MP/csv_cleaner_html.html
