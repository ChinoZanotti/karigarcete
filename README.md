# Sitio de Karina Garcete

Sitio estático de una sola página con cuatro vistas: Inicio, Tienda, Sobre mí y Contacto.

## Publicar en GitHub Pages

1. Creá un repositorio nuevo en GitHub (por ejemplo `karinagarcete`).
2. Subí **todo el contenido de esta carpeta** a la raíz del repositorio (incluyendo el archivo oculto `.nojekyll`, que es necesario para que se carguen los archivos de la carpeta `_ds`).
3. En el repositorio: **Settings → Pages → Source: Deploy from a branch → Branch: main / (root)** y guardá.
4. En unos minutos el sitio queda en `https://<usuario>.github.io/<repositorio>/`.

Para un dominio propio (por ejemplo `karinagarcete.com`), agregalo en **Settings → Pages → Custom domain** y apuntá el DNS a GitHub Pages.

## Qué hay que completar antes de publicar

En `index.html`, dentro del bloque `class Component extends DCLogic`, están los datos de contacto de relleno. Buscá y reemplazá:

| Buscar | Reemplazar por |
| --- | --- |
| `595981123456` | número de WhatsApp real, con código de país y sin espacios |
| `hola@karinagarcete.com` | email real |
| `@losdibujosdekari` | usuario de Instagram |
| `Asunción, Paraguay` | dirección del taller |

Faltan también las fotos de: calendario 2026, block de pintura, tote bag, "Somos Naturaleza", "Serie Tierra I" y "Serie Tierra II". Guardalas en `assets/` y en la lista `PRODUCTS` de `index.html` cambiá `slotHint: '...'` por `img: 'assets/nombre-del-archivo.jpg'`.

## Estructura

- `index.html` — el sitio completo (marcado + lógica).
- `assets/` — logo vectorial y fotografías.
- `_ds/` — hoja de estilos y tokens del sistema visual.
- `support.js`, `image-slot.js` — runtime del sitio. No hace falta editarlos.

Requiere conexión a internet: React y las tipografías (Caprasimo y Figtree) se cargan desde CDN.
