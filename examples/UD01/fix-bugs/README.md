# fix-bugs: arregla las rutas

La web de TecnoClick tiene dos páginas, la portada y la ficha de un producto, y casi nada carga: faltan estilos, imágenes y scripts, y algún enlace no lleva a ningún sitio. El HTML, el CSS y el JavaScript están bien escritos. Lo que falla son las **rutas**.

```
fix-bugs/
├── index.html
├── css/
│   └── estilos.css
├── img/
│   ├── cabecera.svg
│   └── raton-inalambrico.png
├── productos/
│   └── producto.html
└── scripts/
    ├── script1.js
    └── script2.js
```

## 1. Antes de abrir el navegador, predice

Lee `index.html`, `productos/producto.html` y `css/estilos.css`. Por cada `<link>`, `<script>`, `<img>`, `<a>` y `url(...)`, anota en una tabla qué dirección va a pedir el navegador y si crees que llegará bien (200) o no (404).

| Archivo | Ruta escrita | Dirección que pedirá | ¿200 o 404? |
|---|---|---|---|
| `index.html` | `estilos.css` | | |
| … | … | | |

## 2. Comprueba tu predicción

Abre en VSCodium la carpeta del repositorio **entero**, no solo `fix-bugs`, y lanza `index.html` con Live Preview. Con la pestaña **Red** y la **Consola** abiertas, recarga y compara lo que sale con tu tabla. Haz lo mismo con la ficha del producto.

## 3. Arréglalo

Tres reglas:

- No se renombra ni se mueve ningún archivo.
- Solo se tocan las rutas.
- Ninguna ruta puede empezar por `/`.

Está terminado cuando se cumple todo esto:

- Las dos páginas se ven con estilos, y la cabecera de la portada tiene su imagen de fondo.
- La foto del ratón aparece en la ficha.
- El enlace de la portada lleva a la ficha, y el de la ficha vuelve a la portada, **también en un equipo con Linux**.
- La pestaña Red no tiene ningún 404 en ninguna de las dos páginas.
- Cada mensaje sale **una sola vez** en la consola.

## 4. Para pensar

1. Una de las rutas funcionaba si abrías solo la carpeta `fix-bugs` y fallaba al abrir el repositorio entero. ¿Cuál, y por qué?
2. Uno de los enlaces funciona en Windows y falla en Linux. ¿Qué tiene de distinto?
3. Mira la columna **Tamaño** de la pestaña Red en la ficha del producto. ¿Cuánto pesa la foto del ratón, y a qué ancho se muestra? ¿Qué harías con ella antes de publicar la web?
