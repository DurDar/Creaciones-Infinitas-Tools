# 🚀 Tiendanube Data Automator - Creaciones Infinitas
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DurDar/Creaciones-Infinitas-Tools/blob/main/Creaciones_Infinitas_Gestion_Tiendanube.ipynb)
Este repositorio contiene una solución profesional de ingeniería de datos desarrollada en **Python (Google Colab)** para la gestión, unificación y normalización de catálogos textiles masivos. Optimizada para la carga de datos en la plataforma **Tiendanube**.

## 🏗️ Arquitectura de Datos (Novedad)
El sistema ahora implementa una estructura de carpetas autogestionada para garantizar la integridad de la información:
- **/materia_prima**: Carpeta de entrada donde se alojan los fragmentos CSV originales (Lista N°77).
- **/resultados**: Carpeta de salida donde el sistema deposita la Lista Maestra limpia y el archivo final de carga.

## 🛠️ La Solución: Protocolo de Blindaje de Datos
Se implementó un cuaderno que sigue un manual de estilo estricto:
- **Aislamiento de Entradas:** El código solo procesa archivos dentro de `materia_prima`, evitando la duplicación de datos por procesamientos previos.
- **Normalización Automática:** Limpieza de headers, eliminación de espacios y mapeo de columnas críticas (`artículo` -> `Nombre`).
- **Control de Versiones:** Exportación automática con *timestamps* en la carpeta de resultados para auditoría de precios y stock.
- **Interfaz de Auditoría:** Uso de `tqdm` y `data_table` para validación visual antes de la exportación final.

## 🚀 Cómo usar este proyecto
1. Abre el archivo `.ipynb` en Google Colab.
2. Al ejecutar la primera celda, el sistema creará automáticamente las carpetas `materia_prima` y `resultados` en tu Google Drive (`/Creaciones_Infinitas`).
3. Sube tus 13 archivos CSV originales a la carpeta `materia_prima`.
4. Ejecuta el resto del cuaderno. El archivo listo para Tiendanube aparecerá en la carpeta `resultados`.

## 📦 Tecnologías
- `Pandas` (Procesamiento de datos)
- `Google Colab & Drive API` (Infraestructura)
- `Tqdm` (Feedback visual)
- 
## 📈 Próximos Pasos (Roadmap de Mejora)
Para escalar esta solución, se planean las siguientes implementaciones:
- **Validación Automática de Precios:** Alerta visual si un precio varía más de un 20% respecto a la versión anterior (Detección de outliers).
- **Dashboard en Streamlit:** Interfaz gráfica para visualizar la evolución del stock total sin entrar al código.
- **Integración API Mercado Pago:** Automatización de la conciliación de gastos para calcular el margen neto real por producto.
---
**Desarrollado por Darío Fernando Durán** *Impulsando la transformación digital en el sector textil.*
