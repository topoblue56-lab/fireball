# Fireball — Roleplay con IA

Este ZIP contiene la app lista para publicarse como PWA y convertirse en APK de Android.

## Contenido
- `index.html` — la app completa (chat, personajes, ajustes, selector de modelos).
- `manifest.json` — metadatos de la PWA (nombre, iconos, colores).
- `sw.js` — Service Worker para funcionamiento offline básico.
- `icons/` — iconos de la app en los tamaños necesarios (192, 512, 512 maskable, apple-touch-icon).

## Pasos para generar la APK

1. **Sube estos archivos a un hosting HTTPS** (obligatorio). La opción más rápida y gratis es GitHub Pages:
   - Crea un repositorio nuevo en GitHub.
   - Sube todo el contenido de esta carpeta (manteniendo la estructura, incluida la carpeta `icons/`).
   - Ve a *Settings → Pages*, activa GitHub Pages sobre la rama principal.
   - Tu URL quedará algo así: `https://tuusuario.github.io/fireball-pwa/`

2. **Ve a [pwabuilder.com](https://www.pwabuilder.com)** y pega esa URL.
   - Detectará automáticamente el manifest y los iconos.
   - Pulsa "Package for stores" → **Android**.
   - Descarga el `.apk` (instalación directa) o el `.aab` (para subir a Google Play).

3. **Instala el APK en tu móvil**: pásalo por USB/Drive, activa "Instalar apps de orígenes desconocidos" en Ajustes y ábrelo.

## Notas

- La API Key de OpenRouter está embebida por defecto en el código (`DEFAULT_API_KEY` dentro de `index.html`). Recuerda que cualquiera que inspeccione el archivo puede verla — no publiques este repo como público si te preocupa que otros la usen.
- El modelo por defecto es `meta-llama/llama-3.1-8b-instruct:free`. Puedes cambiarlo desde el propio código (`DEFAULT_MODEL`) o, en el futuro, reactivando el panel de ajustes en la interfaz (actualmente está oculto con la clase `hidden`).
