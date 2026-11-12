# Mi trayectoria (stream graph)

Stream graph de la trayectoria de Javi Cantón-Correa, inspirado en el de Alli Torban. D3 v7, sin build.

## Publicar en GitHub Pages

1. Sube `index.html` a la raíz de un repositorio (`steamgraph-cv`).
2. En *Settings > Pages*, elige *Deploy from a branch*, rama `main`, carpeta `/ (root)`.
3. La página queda en `https://<usuario>.github.io/steamgraph-cv/` (versión inglesa: añade `#en`).

## Editar los datos

Todo lo editable está en el bloque `const DATA = {...}` de `index.html`:

- `capas`: cada franja. `valores` es el peso aproximado por año (0 a 10; 10 = jornada completa). Entre años se interpola y fuera de `desde`/`hasta` vale 0. El orden de la lista es el orden de abajo arriba.
- `titulos`: anotaciones bajo el gráfico. `hitos`: puntos sobre el gráfico.
- `centros`, `proyectos` y `competencias`: barras bajo el eje. `tipo` toma el color de una capa; `url` las hace clicables.
- Los textos llevan versión `{ es, en }`.

Las etiquetas se colocan solas: dentro de la franja si caben, al final si la capa sigue activa, y si no, quedan en la leyenda y el tooltip.
