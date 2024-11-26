---
title: "Markdown Syntax"
date: 2021-04-03T23:29:21+05:30
draft: false
github_link: "https://github.com/gurusabarish/hugo-profile"
author: "Gurusabarish"
tags:
  - Markdown syntax
  - Sample
  - example
image: /images/post.jpg
description: ""
toc:
---

### Cita en bloque sin atribución

> Don't communicate by sharing memory, share memory by communicating.</p>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## Tablas

Las tablas no forman parte del estándar principal de Markdown, pero Hugo las soporta de forma nativa.

| Nombre  | Edad |
|  -----  |  --- |
|  Bob    |  27  |
|  Alice  |  23  |

### Markdown sin tablas

| Inline&nbsp;&nbsp;&nbsp; | Markdown&nbsp;&nbsp;&nbsp; | In&nbsp;&nbsp;&nbsp;                | Table  |
| ------------------------ | -------------------------- | ----------------------------------- | ------ |
| _italics_                | **bold**                   | ~~strikethrough~~&nbsp;&nbsp;&nbsp; | `code` |

## Citas en bloque

El elemento `blockquote` representa contenido que es citado de otra fuente, opcionalmente con una cita que debe estar dentro de un elemento `footer` o `cite`, y opcionalmente con cambios en línea como anotaciones y abreviaturas.

> **Nota** que puedes usar _sintaxis Markdown_ dentro de una cita en bloque.

### Ejemplo

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Ejemplo de Documento HTML5</title>
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

### Code block indented with four spaces

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Ejemplo de Documento HTML5</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

### Code block with Hugo's internal highlight shortcode

{{< highlight html >}}

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Ejemplo de Documento HTML5</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
{{< /highlight >}}

## Tipos de Listas

### Lista Ordenada

1. Primer item
2. Segundo item
3. Tercer item

### Lista Desordenada

- Un item
- Otro item
- Y otro item

### Lista Anidada

- Items
  1. Primer Sub-item
  2. Segundo Sub-item

## Encabezados

los siguientes elementos HTML `<h1>`—`<h6>` representan 6 niveles de secciones de encabezados. `<h1>` es la mayor seccion `<h6>` es la menor.

# H1

## H2

### H3

#### H4

##### H5

###### H6

## Otros Elemntos — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> es una imagen de mapa de bits.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.
