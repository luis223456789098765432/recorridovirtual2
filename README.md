# Recorrido Virtual — Versión con Diagnóstico

Esta variante añade:
- **Chequeo de imágenes** (muestra cuáles rutas no cargan).
- Botón **“Importar imágenes…”** para cargar archivos locales y emparejarlos por **nombre** con lo declarado en `TOUR_CONFIG` (útil cuando no están en `images/`).

## Pasos recomendados
1. Coloca tus imágenes 360° en `images/` con los **nombres exactos**:
   - `vecteezy_majestic-peaks-and-serene-valleys-a-360-view-of-the-italian_20803205.jpg`
   - `vecteezy_tbilisi-sameba-cathedral-360_19828880.jpg`
2. Abre con un **servidor local** para evitar restricciones del navegador:
   ```bash
   cd virtual_tour_template_debug
   python -m http.server 8000
   # Visita http://localhost:8000
   ```
3. Si aún no cargan, usa el botón **Importar imágenes…** y selecciona los archivos desde tu PC. El sistema los empareja por nombre.

## Notas
- Las imágenes deben ser 360° equirectangulares (relación 2:1). Si no lo son, se verán distorsionadas.
- Puedes ajustar `yaw` y `pitch` de los hotspots en el bloque `TOUR_CONFIG` de `index.html`.
