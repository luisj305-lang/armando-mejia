# Armando Mejía — sitio del artista

Sitio web personal del pintor Armando Mejía. Página estática, sin dependencias ni build: se abre
directamente `index.html` o se publica tal cual en GitHub Pages.

## Estructura

```
index.html      todo el sitio (HTML + CSS + JS en un archivo)
obra/           46 imágenes de obra, JPEG, lado mayor 1100 px
```

## Secciones

| Sección | Obras |
|---|---|
| Paisajes | 16 |
| Figuras | 11 |
| Cuba | 5 |
| Música | 3 |
| Arquitectura | 4 |
| Devoción | 2 |
| Abstractos | 5 |

Además: Exposiciones, Estudio, Bio y Contacto.

## Publicar en GitHub Pages

En el repositorio: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)`**.
El sitio queda disponible en `https://<usuario>.github.io/<repo>/` en un par de minutos.

## Cómo editar el contenido

Todos los textos están directamente en `index.html`, en español y sin plantillas de por medio.

- **Fichas de obra** — busque `<figcaption>`. El formato es
  `"Título" - medidas - técnica - año`.
- **Bio, Estudio, Contacto y Exposiciones** — son secciones `<section class="page" id="...">`
  al final del archivo. Se editan como texto normal.
- **Portada** — los `div.slide` al principio toman su imagen de la galería mediante el atributo
  `data-from="wN"`, donde `N` es el número del archivo en `obra/`. Cambiando ese número se cambia
  la imagen de portada.
- **Añadir una obra** — coloque el JPEG en `obra/` y copie un bloque `<figure class="cell">`
  existente, ajustando `flex-grow`, `flex-basis` y el `padding-bottom` del `span.ratio` a la
  proporción de la nueva imagen.

## Pendiente de confirmar

Los siguientes datos son provisionales y deben reemplazarse por los reales:

- Año y lugar de nacimiento, y trayectoria de formación (sección **Bio**)
- Títulos, medidas y años de las 46 obras
- Listado de exposiciones
- Correo, teléfono y galerías de representación (sección **Contacto**)

## Tipografía

El sitio usa **Montserrat** desde Google Fonts, con reserva a Helvetica y Arial. Si se prefiere
trabajar sin conexión, descargue la fuente a una carpeta `fonts/` y sustituya el `<link>` del
`<head>` por una regla `@font-face`.
