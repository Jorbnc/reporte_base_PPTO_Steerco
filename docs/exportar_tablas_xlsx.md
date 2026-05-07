# Exportar tablas oficiales a XLSX

Esta guía describe cómo exportar las tablas intermedias oficiales desde Power BI Desktop para compartirlas como archivos `.xlsx`.

## Tablas a exportar

Las tablas oficiales son:

- `cumplimiento_acumulado_2026_corte`
- `cumplimiento_acumulado_2026_corte_CL`
- `cumplimiento_acumulado_2026_corte_PE`
- `cumplimiento_anual_2026_Quantum`
- `cumplimiento_anual_2026_Quantum_CL`
- `cumplimiento_anual_2026_Quantum_PE`

No exportes las tablas que empiezan con `visual_`; esas son auxiliares para los diagramas.

## Antes de exportar

1. Abre el proyecto `.pbip` en Power BI Desktop.
2. Actualiza los datos desde `Inicio > Actualizar`.
3. Revisa el valor de `parametros_corte[Mes Corte]`.
4. Si necesitas cambiar el mes de corte, cambia ese valor y vuelve a actualizar el modelo.
5. Verifica visualmente que las tablas y los diagramas muestran los importes esperados.

## Opción recomendada: exportar desde una tabla visual

1. Crea una página temporal llamada `Export tablas`.
2. Inserta un visual de tipo `Tabla`.
3. Arrastra al visual las columnas de una sola tabla oficial.

   Para las tablas acumuladas:
   - `Categoría`
   - `PPTO 2026`
   - `REAL 2026`

   Para las tablas Quantum:
   - `Categoría`
   - `LB BC 26`
   - `FCST 2026`

4. En el menú del visual, abre `... > Exportar datos`.
5. Si Power BI Desktop permite elegir formato, selecciona `.xlsx`.
6. Si solo permite `.csv`, exporta como `.csv`, ábrelo en Excel y usa `Guardar como > Libro de Excel (*.xlsx)`.
7. Repite el proceso para cada tabla oficial.
8. Nombra los archivos con el mismo nombre de la tabla, por ejemplo:
   - `cumplimiento_acumulado_2026_corte.xlsx`
   - `cumplimiento_anual_2026_Quantum_CL.xlsx`

## Opción simple: copiar y pegar desde la vista de datos

Usa esta alternativa si los usuarios solo necesitan copiar las tablas manualmente.

1. Ve a la vista `Datos`.
2. Selecciona una tabla oficial en el panel de datos.
3. Selecciona las filas y columnas visibles.
4. Copia con `Ctrl+C`.
5. Pega en Excel.
6. Guarda el archivo como `.xlsx`.

## Recomendaciones operativas

- Mantén una carpeta de salida con fecha de exportación, por ejemplo `exports/2026-05-07/`.
- Exporta siempre las 6 tablas en la misma sesión después de actualizar el modelo.
- No edites manualmente los importes exportados; si hay que corregir algo, corrígelo en Power BI y vuelve a exportar.
- Incluye el mes de corte en el nombre de carpeta o archivo cuando aplique, por ejemplo `corte_mes_3`.
