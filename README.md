# HFoco — Organizador de estudio

App web instalable (PWA) para organizar materias, parciales y tiempos de estudio.
Funciona en PC y en Android, y también sin conexión.

## Archivos

```
index.html              la app completa
manifest.webmanifest    nombre, colores e íconos para instalarla
sw.js                   service worker (uso sin conexión)
icons/                  íconos de la app
```

No necesita servidor propio ni base de datos: es un sitio estático.

## Deploy

Cualquier hosting estático con **HTTPS** sirve (el HTTPS es obligatorio para poder instalarla).

**Netlify (lo más rápido):** entrá a app.netlify.com/drop y arrastrá la carpeta `hfoco` completa. Te da un enlace al instante.

**GitHub Pages:**
1. Creá un repositorio y subí todos los archivos a la raíz.
2. Settings → Pages → Source: rama `main`, carpeta `/ (root)`.
3. Queda en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

**Vercel:** `npx vercel` dentro de la carpeta, o importá el repositorio desde vercel.com.

Para probarla en tu PC antes del deploy: `python -m http.server 8000` dentro de la carpeta y abrí `http://localhost:8000`.

## Instalar como app

- **Android (Chrome):** abrí el enlace → menú ⋮ → *Instalar aplicación* (o *Agregar a la pantalla principal*).
- **PC (Chrome / Edge):** ícono de instalar en la barra de direcciones.

## Dónde se guardan los datos

Todo queda guardado en el navegador de cada dispositivo (tareas, fechas, notas y archivos subidos).
Para pasar los datos de un dispositivo a otro: **Progreso → Copia de seguridad → Descargar archivo**,
y en el otro dispositivo **Restaurar copia**. La copia no incluye los archivos subidos.

## Actualizar la app

Cuando cambies algo, subí los archivos de nuevo. Si modificás `sw.js`, cambiá también
`CACHE = 'hfoco-v1'` por `hfoco-v2` (y así) para que los dispositivos tomen la versión nueva.
# Hfoco
