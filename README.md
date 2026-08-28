# EasyETL

<p align="center">
  <img src="packaging/assets/dashboard-icon.png" alt="Icono de EasyETL" width="150">
</p>

<p align="center">
  <strong>Prepará, compará y entendé archivos de datos sin subir información a internet.</strong>
</p>

<p align="center">
  <a href="https://github.com/AgusPalombo/ETL-APP-CV/releases/download/v0.6.0.1/EasyETL-Setup.exe"><strong>Descargar EasyETL para Windows</strong></a>
</p>

## Qué permite hacer

EasyETL es una aplicación local para trabajar con archivos CSV, XLSX, JSON y XML desde una interfaz sencilla:

- Cargar uno o varios archivos de hasta 500 MB.
- Elegir la hoja correcta de un Excel.
- Preparar los datos en un único lugar: filtros, nombres, tipos, columnas calculadas y columnas retiradas.
- Crear columnas mediante texto fijo, combinación, cálculos, diferencias de fechas o reglas de clasificación.
- Previsualizar y aplicar los cambios de forma atómica, siempre sin modificar el archivo original.
- Explorar en una tabla de sólo lectura el resultado final de la preparación y la deduplicación.
- Filtrar desde cada encabezado con búsqueda, selección, exclusión, condiciones tipadas y frecuencias contextuales.
- Filtrar valores mediante listas, búsquedas, vacíos y condiciones combinables.
- Detectar y excluir duplicados con claves elegidas por el usuario.
- Crear indicadores, gráficos y tablas dinámicas con filas, columnas y valores calculados.
- Incorporarlos al Dashboard y reorganizarlos en un mosaico adaptable.
- Exportar e importar plantillas de Dashboard sin transportar datos y generar informes HTML autocontenidos.
- Comparar totales entre dos archivos.
- Comparar registros y distinguir nuevos, eliminados, modificados, sin cambios y filas sin clave válida.
- Exportar resultados en CSV separado por punto y coma.
- Guardar e importar recetas de preparación.

## Privacidad

Todo el procesamiento se realiza en la computadora donde está instalada la aplicación. Los archivos y resultados no se envían a servidores públicos. EasyETL trabaja sobre copias locales derivadas y nunca modifica el archivo original.

## Instalación

1. Descargá [EasyETL-Setup.exe](https://github.com/AgusPalombo/ETL-APP-CV/releases/download/v0.6.0.1/EasyETL-Setup.exe).
2. Abrí el instalador.
3. Elegí si querés crear el acceso directo en el escritorio.
4. Finalizá la instalación y abrí **EasyETL**.

Windows puede mostrar una advertencia mientras el instalador no tenga una firma digital comercial. Verificá que la descarga provenga de este repositorio.

## Actualizaciones

EasyETL puede buscar nuevas versiones al iniciarse. La actualización es opcional: si la aceptás, descarga el instalador publicado, valida su integridad y reemplaza la versión anterior conservando los datos locales.

La versión publicada es **0.6.0.1 para Windows de 64 bits**.

## Calidad de desarrollo

Antes de iniciar 0.5.0.3 se incorporó un arnés de ingeniería obligatorio, sin cambiar la versión instalada. El arnés protege la privacidad local, la inmutabilidad de los archivos originales, la arquitectura, el tipado, las pruebas, la accesibilidad, el responsive y el empaquetado.

Para preparar una clonación y ejecutar los controles:

```powershell
.\scripts\install-dev-harness.ps1
.\scripts\quality-gate.ps1 -Mode Fast
.\scripts\quality-gate.ps1 -Mode Full
```

El modo `Release` es el único flujo autorizado para generar el instalador. La guía completa está en [docs/engineering/QUALITY_HARNESS.md](docs/engineering/QUALITY_HARNESS.md) y la deuda histórica controlada en [docs/engineering/TECHNICAL_DEBT_BASELINE.md](docs/engineering/TECHNICAL_DEBT_BASELINE.md).

### Corrección 0.6.0.1

- La revisión de importación se presenta como un popup centrado, con el contenido de EasyETL visible pero desenfocado y bloqueado detrás.
- La vista previa conserva desplazamiento vertical y horizontal dentro del diálogo, sin mover la página principal.
- La fila de encabezado y la opción Sin encabezado forman un único bloque claro, junto con separador y codificación.
- Se mantienen el foco por teclado, Escape, restauración del foco y una disposición adaptable desde 320 px.
### Novedades de la versión 0.6.0

- La importación asistida permite revisar y corregir hoja, fila de encabezado, separador y codificación antes de confirmar CSV y XLSX.
- Los archivos con detección confiable continúan automáticamente; los ambiguos se detienen para revisión sin bloquear el resto del lote.
- La cola muestra por archivo la transferencia, inspección, importación, error, reintento y cancelación real sin dejar temporales.
- La confirmación es atómica, conserva intacto el archivo original y registra la configuración efectiva para trazabilidad.
- EasyETL funciona sin Internet, mantiene los datos de versiones anteriores y conserva CSV como formato contractual de exportación del MVP.

### Novedades de la versión 0.5.7

- Cada indicador del Dashboard puede tener filtros propios sin modificar la vista general ni los demás componentes.
- Los filtros del indicador admiten varias reglas combinadas, selección o exclusión, condiciones tipadas y valores vacíos diferenciados.
- Los indicadores filtrados se conservan al guardar, recargar, exportar plantillas y generar el informe HTML.
- Los gráficos de dona del informe HTML completan ahora toda la circunferencia, sin el espacio vacío artificial.

### Novedades de la versión 0.5.6

- Los indicadores del informe HTML se agrupan al comienzo de cada página, con hasta cuatro tarjetas por fila.
- La grilla de indicadores se adapta a cuatro columnas en escritorio e impresión, dos en tablet y una en móvil.
- Los gráficos y las tablas ocupan todo el ancho disponible y se muestran uno por fila.
- Se mantienen intactos los cálculos, filtros, totales y el carácter autocontenido del informe.

### Novedades de la versión 0.5.5

- Acciones del Dashboard reúne la plantilla ejecutiva, exportación, importación e informe HTML.
- Las plantillas trasladan indicadores, gráficos, tablas, filtros propios y disposición sin incluir archivos, filas, resultados ni filtros generales.
- La importación valida compatibilidad y permite mapear columnas de forma asistida antes de confirmar el reemplazo.
- El informe HTML incluye todas las páginas, KPI, gráficos accesibles y hasta 100 filas agregadas por tabla.
- El informe es estático, autocontenido, imprimible y no utiliza JavaScript ni recursos externos.

### Novedades de la versión 0.5.4

- Los filtros de tablas dinámicas se administran exclusivamente desde el panel lateral; los encabezados quedan limpios y legibles.
- Los filtros generales y los propios se combinan y sólo se aplican al pulsar Generar tabla.
- Gráficos incorpora filtros propios de categoría y resultado agregado, también aplicados al pulsar Generar gráfico.
- La búsqueda de categorías contempla todo el universo elegible antes del Top N.
- Dashboard versión 10 conserva los filtros de cada gráfico y migra automáticamente las configuraciones anteriores.

### Novedades de la versión 0.5.3

- Cada columna visible de una tabla dinámica tiene su propio filtro, sin depender del nombre, la posición ni el contenido del campo.
- Las dimensiones adaptan selección, búsqueda y condiciones al tipo de dato; las medidas filtran el resultado numérico agregado.
- Las categorías de columnas dinámicas y cada medida asociada conservan objetivos tipados independientes.
- El menú mantiene un ancho legible fuera del scroll de la tabla y se reposiciona al desplazar o redimensionar la vista.
- Los valores se calculan sobre todo el universo elegible antes de Top N y paginación, y el resumen separa filtros generales, dimensiones y medidas.

### Novedades de la versión 0.5.2

- El constructor y la vista previa de tablas dinámicas comparten una altura contenida; el desplazamiento vertical y horizontal queda dentro de la grilla.
- Las dimensiones se filtran exclusivamente desde sus encabezados con búsqueda, selección y frecuencias contextuales sobre todo el resultado elegible.
- Los valores disponibles respetan los filtros generales, las demás dimensiones y las medidas, aunque estén fuera de la página visible.
- Los filtros de medidas se presentan fuera de la grilla como tarjetas compactas y actualizan el resultado sin ocultar la última vista válida.
- El resumen separa claramente filtros generales, filtros de columnas y filtros de medidas.

### Corrección 0.5.1.1

- Los filtros propios de tablas dinámicas se presentan como tarjetas verticales con nombres, condiciones y valores completos.
- Los filtros generales y los exclusivos de la tabla se muestran por separado y explican el orden en que se aplican.
- La interfaz distingue cambios pendientes de filtros ya aplicados al resultado.
- Los botones para quitar filtros conservan un tamaño compacto y accesible.

### Novedades de la versión 0.5.1

- Cada encabezado de `Explorar datos` reúne orden y filtros tipo Excel, con búsqueda paginada, selección o exclusión y condiciones según el tipo de columna.
- `Nulo`, `Texto vacío` y `Sólo espacios` se filtran por separado; las reglas y recetas anteriores continúan funcionando.
- Las frecuencias respetan los demás filtros activos y las consultas obsoletas se cancelan o ignoran al cambiar de dataset, columna o búsqueda.
- Las tablas dinámicas incorporan filtros propios de dimensiones y medidas, filtros desde sus encabezados y totales reconciliados después de los filtros.
- La exportación de tablas dinámicas incluye todas las páginas, separador `;`, UTF-8 BOM y fila de total general.
- Dashboard migra automáticamente a la versión 9 y conserva filtros independientes en cada tabla guardada.
- Se incluyen las mejoras visuales locales 0.5.0.3–0.5.0.6.

### Mejoras incorporadas desde 0.5.0.6

- Los botones para quitar fragmentos ya no se estiran: conservan un tamaño cuadrado compacto.
- Las filas mantienen una separación clara y una única acción compacta permite quitar la última regla cuando hay más de una.
- Esta corrección forma parte del release 0.5.1.

### Mejoras incorporadas desde 0.5.0.5

- Las tarjetas de Columnas nuevas tienen más aire entre el nombre resultante y la fila de controles.
- Los combobox e inputs de una misma fila conservan una separación uniforme, también en temas claro y oscuro.
- Esta mejora forma parte del release 0.5.1.

### Mejoras incorporadas desde 0.5.0.4

- Los desplegables quedan anclados al control aunque la sección tenga scroll y se cierran al salir de vista.
- Los inputs de columnas nuevas, las listas múltiples y los paneles de Deduplicar conservan una presentación contenida y coherente.
- Esta corrección forma parte del release 0.5.1.

### Mejoras incorporadas desde 0.5.0.3

- Todos los desplegables utilizan una familia compartida, accesible y adaptable.
- Las listas extensas permiten buscar; las breves admiten navegación y escritura incremental.
- Los menús respetan el viewport, los modales, las opciones deshabilitadas y la restauración del foco.
- Esta mejora forma parte del release 0.5.1.

### Corrección 0.5.0.2

- `Número entero` detecta automáticamente el formato original, redondea de manera explícita y avisa cuántos valores cambiarán.
- El separador regional se configura únicamente para `Número decimal` y ahora se presenta como formato del dato de origen con ejemplos claros.
- `Nombres y tipos` utiliza un editor más limpio con origen, tipo detectado, estado de modificación y ayuda contextual.
- Los desplegables del editor son compactos, buscables y desplazables; se mantienen dentro del viewport y pueden utilizarse con teclado o pantalla táctil.
- Las configuraciones antiguas que asociaban un formato decimal a números enteros se normalizan a detección automática sin modificar el archivo original.

### Corrección 0.5.0.1

- `Preparar datos` mantiene acciones, estado y progreso dentro de su contenedor en escritorio, tablet y móvil.
- El cambio de nombre y tipo utiliza un selector con búsqueda y una única tarjeta redondeada para la columna elegida.
- Las columnas modificadas quedan identificadas y los nombres vacíos o repetidos se bloquean antes de procesar.
- `Restablecer columnas quitadas` devuelve ese apartado a cero sin alterar otras operaciones del borrador.
- Volver a `Automático` elimina correctamente la conversión explícita y permite aplicar la preparación sin errores.

### Novedades de la versión 0.5.0

- La nueva sección `Preparar datos` concentra filtros, cambios de nombre y tipo, creación y retiro reversible de columnas.
- `Explorar datos` queda como tabla limpia de sólo lectura con búsqueda, orden, paginación, visibilidad y orden de columnas.
- Las columnas nuevas admiten texto fijo, combinación de fragmentos, cálculos, diferencias de fechas y clasificaciones por reglas.
- Las recetas versión 3 trasladan la preparación completa sin incluir registros, dashboards ni información sensible.
- Los cambios estructurales se construyen desde el original y se aplican sólo si la operación completa termina correctamente.
- EasyETL incorpora activación offline por equipo, firma Ed25519 y 30 días de uso completo inicial, sin enviar información a Internet.

### Novedades de la versión 0.4.14

- Los indicadores muestran todas las columnas para cantidad y valores únicos, y únicamente columnas numéricas para suma, promedio, mediana, mínimo y máximo.
- Al elegir un cálculo numérico desde una columna incompatible, EasyETL selecciona una alternativa válida y explica el cambio.
- Los constructores de Gráficos y Tablas mantienen fija su cabecera y desplazan sólo las opciones cuando realmente exceden el lienzo; la barra queda separada de los campos y próxima al borde del panel.
- El desplazamiento interno funciona con teclado, mouse y pantalla táctil en temas claro y oscuro, sin generar overflow global.

### Novedades de la versión 0.4.13

- Dos gráficos dentro de un mismo cuadrante se distribuyen lado a lado desde 601 px y se apilan únicamente en móvil.
- Las combinaciones de gráfico e indicadores aprovechan el ancho del cuadrante mediante columnas, sin perder el orden de los KPI.
- Ubicar, adelantar, retrasar, editar y quitar comparten una única fila superior, dejando el título completamente separado y legible.
- Los textos, cifras y visualizaciones se adaptan a tarjetas estrechas sin generar superposiciones ni desplazamiento horizontal global.
- El formato Dashboard v9 conserva la ubicación anterior y migra los tableros existentes sin perder componentes.

### Novedades de la versión 0.4.12

- El Dashboard reemplaza el arrastre por una ubicación precisa mediante páginas y seis cuadrantes visuales.
- Antes de confirmar un cambio, EasyETL muestra qué componentes se moverán y conserva el Dashboard intacto si se cancela.
- Los elementos que no entran avanzan automáticamente al siguiente cuadrante o página, sin superposiciones ni desplazamiento horizontal.
- Cada componente puede adelantarse o retrasarse dentro de su cuadrante mediante controles accesibles.
- Los dashboards anteriores se migran automáticamente conservando todos sus indicadores, gráficos, tablas y orden visual.

### Novedades de la versión 0.4.11

- El Dashboard aprovecha todo el ancho disponible sin invadir menús ni generar desplazamiento horizontal global.
- EasyETL calcula automáticamente el tamaño y la posición de indicadores, gráficos y tablas; ya no es necesario elegir un tamaño manual.
- Los componentes se compactan en páginas de seis cuadrantes y se redistribuyen al reordenarlos mediante mouse, tacto o teclado.
- Las configuraciones anteriores se migran conservando componentes y orden.
- Los títulos y valores se adaptan mejor a espacios reducidos, y los gráficos incluyen una alternativa textual accesible.

### Corrección 0.4.10.3

- Las tablas dinámicas pueden ordenarse por cualquiera de sus valores calculados, no solamente por el primero.
- Se incorporó un Top N configurable entre 3 y 25 grupos, con selección de la medida utilizada para el ranking.
- El resto puede consolidarse en `Otros`, recalculando correctamente sumas, promedios, medianas y valores únicos desde los registros originales.
- Las tablas guardadas en el Dashboard conservan el orden y el Top N elegidos; las configuraciones anteriores se migran sin activar límites nuevos.

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
