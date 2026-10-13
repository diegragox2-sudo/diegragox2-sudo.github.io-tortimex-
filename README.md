# TortiMex: página de enlaces

Página web de una sola pantalla para TortiMex ("El maíz que te hace feliz"), venta de fritura en mostrador y fabricación y distribución de tortilla industrial. Muestra el nombre, el lema y los botones de contacto: WhatsApp, Instagram, TikTok y Facebook.

Estilo: minimalista con toque de comic y detalles mexicanos (papel picado, franja verde, blanca y roja). Funciona en computadora y en celular.

## Archivos

- `index.html`: la página completa. No necesita instalar nada ni otros archivos. Se abre con doble clic en cualquier navegador.

Si luego se agrega un logo, se guarda en la misma carpeta (por ejemplo `logo.png`).

## Cómo cambiar los datos

Abre `index.html` con el Bloc de notas o cualquier editor de texto y busca estas partes.

### WhatsApp

Busca `https://wa.me/50236746214`. El número va con código de país (502 es Guatemala), sin espacios, guiones ni el signo +. El texto `3674-6214` que se ve en el botón se cambia aparte, en la línea que dice `<span class="dato">3674-6214</span>`.

### Instagram

Busca `https://www.instagram.com/tortimex.xela`. Cambia el usuario al final si hace falta, y el texto visible `@tortimex.xela`.

### Facebook

Busca `https://www.facebook.com/profile.php?id=61564246979248`. Es el enlace de la página de TortiMex.

### TikTok (pendiente)

Ahora el botón abre una búsqueda de "tortimex". Busca `https://www.tiktok.com/search?q=tortimex` y reemplázalo por el enlace del perfil, por ejemplo `https://www.tiktok.com/@usuario`. Cambia también el texto `Ver perfil` por el usuario.

Si el negocio no tiene TikTok, borra el bloque completo de ese botón: desde el `<li>` que contiene `id="link-tiktok"` hasta su `</li>`.

### Textos

- Nombre: `<h1>TortiMex</h1>`
- Lema: `¡El maíz que te hace feliz!`
- Título de los botones: `¡Ándale, escríbenos!`
- Frase final: `Tortillas, nachos, tostadas, chalupas y mucho más.`

### Colores

Están al inicio del archivo, en el bloque `:root`:

- `--bg`: verde del fondo
- `--red`: rojo
- `--ink`: negro de los contornos
- `--paper`: blanco de los paneles

## Cómo agregar el logo (pendiente)

Todavía no hay logo en la página. Cuando se tenga el archivo (mejor PNG con fondo transparente):

1. Guárdalo como `logo.png` junto a `index.html`.
2. Dentro de `<header class="brand">`, antes del `<h1>`, agrega:
   `<img src="logo.png" alt="TortiMex" style="width:9rem;max-width:100%">`

Si el logo ya incluye el nombre, se puede quitar el `<h1>`.

No se recomienda usar el enlace de la imagen de Facebook directamente: esos enlaces caducan y el logo dejaría de verse.

## Cómo publicarla

Es un sitio estático, así que sirve cualquier hosting gratuito o barato:

- Netlify Drop (netlify.com/drop): arrastrar la carpeta con `index.html`.
- GitHub Pages.
- Cualquier hosting con cPanel: subir `index.html` a la carpeta `public_html`.

Para que tenga dominio propio (por ejemplo `tortimex.com`), se compra el dominio y se conecta al hosting elegido.

## Pendientes

- Enlace de TikTok.
- Logo en archivo original.
- Mascota del charro (opcional).
- Enlace de Google Maps para un botón de "Cómo llegar" (el QR de la tarjeta lleva a la ubicación).

## Notas técnicas

- Las letras se cargan de Google Fonts (Lilita One y Figtree). Sin internet se usa una letra de respaldo y la página sigue funcionando.
- Los íconos de las redes y los banderines están dentro del mismo archivo.
- Se adapta a celular: los márgenes se ajustan y no hay desplazamiento lateral.
