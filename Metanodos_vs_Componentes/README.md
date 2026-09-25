# KNIME - Metanodos vs Componentes

Este directorio está pensado para contener el workflow de KNIME que explica:

- **Metanodos**: Agrupa y organiza tu flujo.
- **Componentes**: Reutilización de subflujos.
- **Diferencias** entre metanodos y componentes.

## Sugerencia de estructura del workflow

Crea un workflow de KNIME (archivo `.knwf`) en esta carpeta con el nombre:

- `Metanodos_vs_Componentes.knwf`

Dentro del workflow, organiza tres secciones:

1. **Flujo base**
   - `File Reader` / `CSV Reader`
   - `Row Filter`
   - `Math Formula`
   - `GroupBy`

2. **Metanodo "Limpieza y Cálculo"**
   - Agrupa `Row Filter` + `Math Formula` en un metanodo.
   - Objetivo: mostrar cómo organizar y ocultar complejidad visual.

3. **Componente "Limpieza y Cálculo (Reusable)"**
   - Convierte el metanodo en componente, o crea el componente directamente.
   - Añade nodos de configuración para que el usuario pueda elegir columnas (precio, cantidad, etc.).
   - Guarda el componente en una carpeta compartida de tu `KNIME Explorer` para mostrar reutilización.

## Puntos clave para explicar

- **Metanodos**
  - Sirven para agrupar nodos y mejorar la legibilidad del flujo.
  - No tienen diálogo de configuración propio.
  - Uso principal: organización interna del workflow.

- **Componentes**
  - Permiten crear bloques reutilizables con su propio diálogo de configuración.
  - Se pueden guardar y reutilizar en otros workflows.
  - Ideales para estandarizar lógicas recurrentes (limpieza, transformaciones comunes, etc.).

- **Diferencias**
  - Metanodo = organización.
  - Componente = reutilización + parametrización.
  - Los componentes se comportan como nodos personalizados con documentación y configuración exposable.

> Nota: El archivo `.knwf` debe crearse y editarse desde KNIME Analytics Platform; esta carpeta solo actúa como ubicación destino del workflow y documentación de apoyo.
