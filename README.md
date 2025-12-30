# Inventario Rápido

Script que filtra y contabiliza materiales de distintas ubicaciones para entregar inventario diario

## Características principales

* Lee archivo en Excel y construye un DataFrame.
* Elimina filas que contienen ubicaciones que no pertenecen a la bodega.
* Filtra el código de los materiales considerados dentro del inventario.
* Contabiliza las cantidades de todas las ubicaciones existentes y las suma por cada código.
* Devuelve un archivo Excel con el código y su cantidad total

## Tecnologías utilizadas
* Python
    - Pandas
