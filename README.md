# 🐾 Cuaderno de cumpleaños para Annie

Sitio estático (HTML + CSS + JS) para GitHub Pages. Todo se configura **dentro de `index.html`**,
en el bloque `CONFIG` (está al inicio del `<script>`). No hay nada que se edite desde la página.

## Estructura del repositorio

```
index.html
fotos/    tus fotos
videos/   tus videos
musica/   tus 2 canciones
```

## Cómo agregar fotos y videos

Cada recuadro es **una línea** dentro de `CONFIG.paginas`:

```js
{ tipo:'foto',  archivo:'foto1.jpg',  texto:'Annie 🐾' },
{ tipo:'video', archivo:'video1.mp4', texto:'Feliz cumple 🎂' },
```

- `tipo`: `'foto'` (busca en `fotos/`) o `'video'` (busca en `videos/`).
- `archivo`: el nombre **exacto** del archivo con su extensión. GitHub distingue mayúsculas: `Foto1.JPG` no es `foto1.jpg`.
- `texto`: lo que aparece junto a la foto.
- Con `archivo:''` el recuadro muestra un gatito con "Foto N" (útil para probar).
- Si un archivo no se encuentra, el recuadro muestra su ruta para que veas qué falta.

La foto se muestra **completa** (vertical, horizontal o cuadrada): el marco se adapta a su forma, sin recortes. Al tocarla se ve en grande.

## Cómo agregar páginas

Al final de la lista `paginas` hay una **plantilla comentada**. Cópiala, pégala justo arriba y borra los `//` del inicio.
Cada página lleva hasta 3 recuadros. Con 30 fotos necesitas 10 páginas. No hay límite.
Si pones más de 3 recuadros en una página, el resto pasa solo a una página nueva.
Si el número de páginas de fotos queda impar, el cuaderno agrega una página de relleno antes de la carta para que las hojas cuadren.

## Música

Escribe los nombres de tus dos canciones en `canciones` (carpeta `musica/`). Suenan una tras otra en bucle, sin botón para apagarlas.
Los navegadores en celular bloquean el sonido hasta el primer toque, así que si no arranca sola, empieza con el primer toque o deslizamiento.

## Recomendaciones

- Fotos de menos de 500 KB. Las de iPhone en HEIC hay que pasarlas a JPG.
- Videos cortos en MP4 (H.264), de menos de 10 MB. Se reproducen solos, sin sonido y en bucle, mientras su página está visible. Al tocarlos se abren en grande con sonido (la música se pausa y vuelve al cerrar).

## Publicar en GitHub Pages

1. Crea el repositorio y sube `index.html` y las tres carpetas.
2. Settings → Pages → Source: rama `main`, carpeta `/ (root)`.
3. Abre el enlace que te da GitHub.

## Que nadie pueda modificarlo

En GitHub, solo tú (el dueño) y quienes invites como *collaborators* pueden cambiar un repositorio. Otras personas pueden verlo y copiarlo (*fork*), pero su copia es aparte: no altera la tuya.
Para más seguridad: Settings → Branches → protege `main`, y cuando termines puedes archivar el repositorio (Settings → *Archive this repository*) para dejarlo de solo lectura. Después de archivar, revisa que el enlace siga funcionando.

## Cómo se usa

- **Arrastrar:** la hoja sigue el dedo (o el mouse) y se suelta hacia adelante o hacia atrás.
- **Celular:** una página a la vez. **Computadora:** cuaderno abierto con dos páginas.
- También funcionan los botones ‹ ›, el clic en la página y las flechas del teclado.
