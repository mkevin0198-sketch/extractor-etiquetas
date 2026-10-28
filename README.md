# Extractor de etiquetas

Aplicación web de NovaPet para procesar etiquetas de MercadoLibre, consultar pedidos y preparar impresiones.

**Abrir la aplicación:** https://mkevin0198-sketch.github.io/extractor-etiquetas/

## Funciones

- Carga de etiquetas de MercadoLibre en archivos `.txt` o texto ZPL pegado.
- Clasificación de pedidos Flex y Colecta, búsqueda y selección de registros.
- Consulta de estados y rutas desde archivos Excel `.xlsx`.
- Exportación a `1 f.csv` (Flex) y `1 c.csv` (Colecta).
- Impresión Zebra/ZPL y gestión de etiquetas PDF de Bluexpress y Walmart.
- Historial local, HTML portable, usuarios, notificaciones y modo oscuro.
- Conexión opcional a Google Drive para detectar archivos.

## Uso

1. Abre la aplicación desde el enlace anterior.
2. Selecciona el usuario y carga un archivo de etiquetas, o pega su contenido.
3. Consulta los resultados y utiliza las opciones de exportación o impresión.
4. Para consultar estados, carga el Excel correspondiente.

La página publicada comienza sin pedidos: el historial incorporado es `{"version":2,"documents":[]}`. Los datos cargados y el historial se guardan en el navegador. Esta copia no incluye los archivos locales ni documentos de la cuenta de Google Drive.

La integración de Drive conserva la configuración del proyecto original y requiere autenticación y permisos de la cuenta correspondiente. Si Google rechaza el nuevo dominio, el propietario del cliente OAuth debe autorizar el origen `https://mkevin0198-sketch.github.io` en su configuración. La impresión depende de la instalación y configuración local de la impresora.

## Archivos

- `index.html`: página principal.
- `app.js`: procesamiento, consulta Excel, historial, exportación e impresión.
- `drive-sync.js`: integración de Google Drive.
- `styles.css`, `left-panel.css`, `order-lookup.css`, `drive-sync.css`: estilos.
- `xlsx.full.min.js`: biblioteca incluida para leer Excel.
- `assets/icons/`: iconos SVG.
- `index.github-standalone.html`: versión con los scripts principales incorporados.
- `build-standalone.js`: construcción de esa versión.
- `NovaPet-Downloads-Helper.ps1`: auxiliar original de Windows para detectar Excel de despacho.

## Procedencia

Copia mediante fork de [asistentebodega-jpg/aa](https://github.com/asistentebodega-jpg/aa), correspondiente al commit `d4886defce97aa2cb6d0f98456eeb0f2970a06d0`. Los 16 archivos originales se conservaron sin cambios. Publicación preparada el 28 de octubre de 2026.
