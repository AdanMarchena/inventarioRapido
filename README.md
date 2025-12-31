# Script de resumen de inventario por material
## Descripción
Script en Python que procesa un archivo de inventario en Excel para filtrar ubicaciones no relevantes, seleccionar materiales específicos y calcular el stock físico total por código de artículo.

El resultado se exporta a un nuevo archivo Excel

## Propósito
Este script se utiliza para obtener un resumen limpio y ordenado del inventario disponible, excluyendo ubicaciones específicas (packing, obsoletos, devolución, etc.) y enfocándose solo en una lista definida de materiales.

Es útil para:

Reportes de stock

Control de inventario

Cruce de información con otras áreas

## Requisitos
- Python 3.9+
- Pandas
- openpyxl (para lectura/escritura de Excel)

## Instalación

pip install pandas openpyxl

## Entrada de datos
- Archivo Excel de inventario
```
  Inventario disponible_639020281205524065.xlsx
```

## Columnas esperadas en el archivo:
- Ubicación
- Código de artículo
- Física disponible

 ## Ejecución
 Ejecutar el script directamente
```
python resumen_inventario_materiales.py
```
## Lógica del Script
1. Carga del archivo Excel en un DataFrame.
2. Exclusión de ubicaciones definidas en una lista (ubicaciones).
3. Eliminación de registros sin ubicación válida.
4. Filtrado por códigos de materiales específicos.
5. Agrupación por código de artículo y suma del stock físico.
6. Reordenamiento según la lista original de materiales.
7. Exportación del resultado a Excel.

## Salida
Archivo generado
```
resultado_materiales.xlsx
```
**Contenido:**
- Código de artículo
- Física disponible

## Limitaciones
- La ruta del archivo de entrada está definida en el código.
- Las listas de ubicaciones y materiales son estáticas.
- No se validan tipos de datos ni valores negativos.
- Asume que las columnas existen con los nombres exactos.

## Personalización
Para reutilizar el script en otros escenarios:
- Modifica la lista ubicaciones para excluir otras zonas.
- Cambia la lista materiales según los códigos requeridos.
- Ajusta el nombre del archivo de entrada y salida.

## Autor
Adán Marchena
Ingeniero en Informática
Chile
