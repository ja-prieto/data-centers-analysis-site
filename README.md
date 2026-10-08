# Centros de datos en España — base común de información

Página estática con los resultados del proyecto: el inventario de centros de datos en España
construido con expedientes administrativos oficiales, la capa del parque en servicio, la red
y los permisos. Es un cuaderno de [marimo](https://marimo.io) compilado a WebAssembly: **se
ejecuta entero en el navegador**, sin servidor detrás.

**Este repositorio es solo la salida compilada, y se sobrescribe entero en cada
publicación** (un único commit, empujado a la fuerza). No se edita aquí: lo genera
`herramientas/publicar_web.sh` en el repositorio del proyecto, que es donde vive también el
flujo de despliegue (`herramientas/pages/despliegue.yml`).

Todo lo que dibuja la página está en `public/`, en CSV y JSON, y se puede abrir por separado.
