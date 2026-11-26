# Lingua IOS V2 — RS App

PWA para iPhone (Safari) que transcribe un video con Whisper, traduce los subtítulos y graba un video nuevo con los subtítulos puestos. Todo en el teléfono: no usa servidor ni laptop.

V2 agrega **Google Translate** como motor predeterminado (Opus-MT sigue disponible como opción) y quita el bucle de reintento que bloqueaba la traducción en Safari.

## Idiomas y motores

- 13 idiomas: inglés, español, francés, alemán, italiano, portugués, ruso, chino, japonés, árabe, hindi, neerlandés y sueco.
- **Google Translate** (predeterminado): necesita internet, no descarga modelos de traducción; solo se envía el texto de los subtítulos.
- **Opus-MT** (opcional): traduce en el dispositivo, descarga modelos la primera vez.
- Transcripción: Whisper `whisper-base` en el navegador (descarga el modelo la primera vez).

## Subtítulos

Tamaño, altura, color de texto, color y opacidad del fondo. Se puede descargar el `.srt` y grabar el video con subtítulos; en iPhone se guarda desde *Compartir → Guardar en Archivos / Fotos*.

## Versión y acceso

Versión actual: **V2** — https://rserrano285-svg.github.io/Lingua-IOS/V2/

La URL raíz redirige a V2. Convención **RS App**: cada versión vive en su carpeta (`V1`, `V2`, ...). Las rutas antiguas `/V18/` y `/V19/` redirigen a V1.

Para instalarla: abre la URL en Safari → *Compartir → Agregar a pantalla de inicio*.

## Límites conocidos

- Videos cortos (hasta ~8 min); Safari en iPhone tiene poca memoria.
- La primera vez descarga modelos de Whisper (decenas de MB).
- iOS no permite guardar silenciosamente: se usa el menú Compartir.

## Apoyo

Gratuita y de código abierto. [PayPal (rene285serrano)](https://paypal.me/rene285serrano).
