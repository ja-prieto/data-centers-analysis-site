# Centros de datos en España — cuaderno de resultados

Página estática con los resultados del censo de expedientes administrativos de centros de
datos en España. Se sirve en GitHub Pages y **se ejecuta entera en el navegador**: es un
cuaderno de [marimo](https://marimo.io) compilado a WebAssembly, así que los deslizadores de
la cadena de conversión, el filtro del mapa y las tablas funcionan sin servidor detrás.

**Este repositorio es solo la salida compilada.** No es el código fuente del proyecto: es lo
que produce `marimo export html-wasm`, y se regenera entero. Todo lo que dibuja la página
está en `public/`, en CSV y JSON, y se puede abrir por separado.

## Qué contienen los datos

Expedientes administrativos nominativos —autorizaciones eléctricas, planes urbanísticos,
evaluaciones ambientales, contratación pública— localizados uno a uno en boletines oficiales
y portales autonómicos, transcritos con su cita y su URL. Son documentos públicos.

Los convenios que gobiernan la transcripción están explicados en la propia página: celda
vacía es dato no localizado y nunca un cero, sin cita oficial la fila no entra, y toda cifra
derivada va marcada como inferida.

## Cómo se regenera

Desde el repositorio del proyecto:

```bash
uv run marimo export html-wasm app/centros_datos.marimo.py -o app/dist --mode run
```

y se copia el contenido de `app/dist/` aquí.
