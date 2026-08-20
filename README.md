# EasyETL

<p align="center">
  <strong>Prepará, compará y entendé archivos de datos sin subir información a internet.</strong>
</p>

<p align="center">
  <a href="https://github.com/AgusPalombo/ETL-APP-CV/releases/download/v0.5.0.2/EasyETL-Setup.exe"><strong>Descargar EasyETL para Windows</strong></a>
</p>

## Qué permite hacer

EasyETL es una aplicación local para trabajar con archivos CSV, XLSX, JSON y XML desde una interfaz sencilla:

- Cargar uno o varios archivos de hasta 500 MB.
- Elegir la hoja correcta de un Excel.
- Revisar columnas, tipos de datos y filas de muestra.
- Corregir tipos numéricos y fechas sin modificar el archivo original.
- Renombrar columnas y reutilizar esos nombres en filtros, gráficos, dashboards y exportaciones.
- Filtrar valores mediante listas, búsquedas, vacíos y condiciones combinables.
- Detectar y excluir duplicados con claves elegidas por el usuario.
- Crear indicadores, gráficos y tablas dinámicas con filas, columnas y valores calculados.
- Incorporarlos al Dashboard y reorganizarlos en un mosaico adaptable.
- Comparar totales entre dos archivos.
- Comparar registros y distinguir nuevos, eliminados, modificados, sin cambios y filas sin clave válida.
- Exportar resultados en CSV separado por punto y coma.
- Preparar datos con filtros, cambios de nombre y tipo, columnas calculadas y eliminación reversible de columnas.
- Guardar e importar recetas de preparación reutilizables.
- Activar una licencia local vinculada al equipo, sin enviar datos por Internet.

## Privacidad

Todo el procesamiento se realiza en la computadora donde está instalada la aplicación. Los archivos y resultados no se envían a servidores públicos. EasyETL trabaja sobre copias locales derivadas y nunca modifica el archivo original.

## Instalación

1. Descargá [EasyETL-Setup.exe](https://github.com/AgusPalombo/ETL-APP-CV/releases/download/v0.5.0.2/EasyETL-Setup.exe).
2. Abrí el instalador.
3. Elegí si querés crear el acceso directo en el escritorio.
4. Finalizá la instalación y abrí **EasyETL**.

Windows puede mostrar una advertencia mientras el instalador no tenga una firma digital comercial. Verificá que la descarga provenga de este repositorio.

## Actualizaciones

EasyETL puede buscar nuevas versiones al iniciarse. La actualización es opcional: si la aceptás, descarga el instalador publicado, valida su integridad y reemplaza la versión anterior conservando los datos locales.

La versión actual es **0.5.0.2 para Windows de 64 bits**.

### Corrección 0.5.0.2

- `Número entero` detecta el formato original, redondea explícitamente y avisa cuántos valores cambiarán.
- El formato regional se elige únicamente para `Número decimal`, con ejemplos claros de coma y punto decimal.
- El editor de nombres y tipos presenta mejor el origen, el tipo detectado y el estado de cada columna.
- Los desplegables son compactos, buscables y desplazables, y permanecen dentro de la pantalla.
- Las preparaciones existentes siguen siendo compatibles y los archivos originales nunca se modifican.

### Corrección 0.5.0.1

- `Preparar datos` mantiene sus acciones y el progreso dentro del espacio disponible en escritorio, tablet y móvil.
- El cambio de nombre y tipo se concentra en una tarjeta clara para la columna seleccionada, con búsqueda y validaciones previas.
- Las columnas quitadas pueden restablecerse juntas sin afectar los demás cambios preparados.
- Volver al tipo `Automático` funciona correctamente y evita conversiones innecesarias.

### Novedades de la versión 0.5.0

- Nueva sección **Preparar datos** para concentrar filtros y cambios estructurales sin modificar el archivo original.
- Creación de columnas mediante texto fijo, combinación, cálculos, diferencias entre fechas y reglas de clasificación.
- Renombrado, conversión de tipos y eliminación reversible de columnas con vista previa y aplicación segura.
- **Explorar datos** queda como una tabla limpia y de sólo lectura sobre el resultado preparado.
- Recetas versión 3 para reutilizar la preparación completa sin incluir registros ni información sensible.
- Licencia offline vinculada al equipo, con 30 días de gracia y activación mediante archivo local.

### Novedades de la versión 0.4.14

- Los indicadores muestran únicamente columnas compatibles con el cálculo seleccionado, evitando opciones confusas.
- Si un cálculo necesita números, EasyETL elige una columna numérica válida y explica el cambio.
- Los menús de Gráficos y Tablas mantienen sus acciones visibles y permiten desplazarse por configuraciones extensas.
- Los constructores se adaptan a escritorio, tablet y móvil sin desbordar la pantalla.

### Novedades de la versión 0.4.13

- Dos gráficos dentro de un mismo cuadrante se muestran lado a lado desde 601 px y se apilan únicamente en móvil.
- Los gráficos y los indicadores pueden compartir un cuadrante mediante una distribución por columnas.
- Los controles para ubicar, ordenar, editar y quitar aparecen juntos en una fila superior más clara.
- Los títulos, valores y gráficos se adaptan a tarjetas estrechas sin producir superposiciones ni desplazamiento lateral.
- Los dashboards existentes conservan sus páginas, cuadrantes y orden.

### Novedades de la versión 0.4.12

- El Dashboard reemplaza el arrastre por una ubicación precisa mediante páginas y seis cuadrantes visuales.
- Antes de confirmar, EasyETL muestra una vista previa de los componentes que cambiarán de lugar.
- Los elementos que no entran se reacomodan automáticamente en los siguientes cuadrantes o páginas.
- Cada componente puede adelantarse o retrasarse dentro de su cuadrante mediante controles claros y accesibles.
- Los dashboards anteriores se actualizan automáticamente sin perder indicadores, gráficos, tablas ni su orden.

### Novedades de la versión 0.4.11

- El Dashboard aprovecha todo el ancho disponible sin invadir menús ni generar desplazamiento horizontal global.
- EasyETL calcula automáticamente el tamaño y la posición de indicadores, gráficos y tablas.
- Los componentes se compactan en páginas y se redistribuyen al reordenarlos mediante mouse, tacto o teclado.
- Los dashboards existentes se actualizan sin perder sus componentes ni su orden.
- Los títulos, valores y gráficos se adaptan mejor a pantallas grandes, tablets y móviles.

### Corrección 0.4.10.3

- Las tablas dinámicas pueden ordenarse por cualquiera de sus valores calculados.
- Se incorporó un Top N configurable entre 3 y 25 grupos, usando la medida elegida por el usuario.
- El resto puede consolidarse en `Otros` con cálculos exactos desde los registros originales.
- Las tablas guardadas en el Dashboard conservan esta configuración.

### Corrección 0.4.10.2

- El constructor de tablas conserva una distribución compacta después de generar resultados.
- La sección de valores puede plegarse y recuerda su estado por archivo.
- Las tablas pueden ordenarse por filas o por el valor calculado, en ambos sentidos.

### Corrección 0.4.10.1

- `Resultado Columna` conserva una tipografía legible al mostrar decimales.
- Los indicadores permiten un máximo de 2 decimales.
- Las configuraciones anteriores con mayor precisión se ajustan de forma segura a 2 decimales.

### Novedades de la versión 0.4.10

- Los gráficos temporales reducen y abrevian automáticamente sus etiquetas para evitar superposiciones.
- Los filtros de comparación se adaptan mejor a dispositivos móviles y recuerdan su estado de forma independiente.
- El constructor de tablas y las opciones de exportación ganan claridad y legibilidad.
- El Dashboard conserva sus componentes en páginas y tamaños predefinidos sin perder configuraciones anteriores.

## Desinstalación

Podés desinstalar EasyETL desde **Configuración → Aplicaciones → Aplicaciones instaladas**. Durante la desinstalación se consulta si también querés borrar los archivos procesados y configuraciones locales.

## Mantenimiento de este README

Para una versión futura:

1. Cambiá el número de versión visible.
2. Actualizá las dos direcciones de descarga con la nueva etiqueta de versión.
3. Conservá el nombre público EasyETL-Setup.exe.
4. Agregá o quitá funciones únicamente cuando estén disponibles en el instalador publicado.
5. Evitá incluir estructura interna, código fuente, pendientes técnicos o información sensible.
