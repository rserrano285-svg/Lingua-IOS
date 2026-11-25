# lingua · versión iPhone

Página web que transcribe un video con Whisper, lo traduce y le pone subtítulos, todo dentro del navegador del iPhone (Safari). No usa servidor ni laptop: el video no sale del teléfono.

La versión de escritorio (Windows, con Whisper y Argos) vive en **otro proyecto**, aparte de este.

## Qué hace
- Transcribe con Whisper (modelo `whisper-base`) usando Transformers.js.
- Traduce con modelos Opus-MT, frase por frase. Entre dos idiomas que no son inglés pasa por inglés.
- 13 idiomas: inglés, español, francés, alemán, italiano, portugués, ruso, chino, japonés, árabe, hindi, neerlandés y sueco.
- Subtítulos con tamaño, altura, color de texto, color y opacidad del fondo.
- Graba un video nuevo con los subtítulos puestos (en tiempo real) y lo guarda en Fotos o en Archivos desde el menú del iPhone.
- Baja los subtítulos en `.srt`.
- Si el iPhone cierra la página por falta de memoria, la página guarda el video en el teléfono (IndexedDB) y reintenta sola, hasta 4 veces.

## Estructura
- `index.html`: toda la app (HTML, CSS y JavaScript en un solo archivo).
- `README.md`: este archivo.

## Publicar (GitHub Pages)
1. Sube `index.html` a la raíz del repositorio.
2. En el repositorio: Settings, Pages, "Deploy from a branch", rama `main`, carpeta `/ (root)`.
3. Abre `https://<usuario>.github.io/<repositorio>/` en Safari.

Para ver un cambio nuevo sin que Safari use lo guardado, agrega `?v=NUMERO` al final de la liga. La versión aparece abajo a la izquierda de la página.

## Límites conocidos
- Mejor con videos cortos (hasta unos 8 minutos). El iPhone tiene poca memoria y Safari puede cerrar la página.
- La primera vez descarga los modelos (decenas de MB) y tarda más.
- iOS no deja que una página guarde directo en Fotos: se usa el menú de guardar del iPhone.
- Pendiente: que los subtítulos no se corten a la mitad en videos de más de un minuto (se revisa con el renglón "Details" que aparece al terminar).

## Versión
v18
