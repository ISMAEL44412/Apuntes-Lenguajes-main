- [Introducción a HTML](#introducción-a-html)
- [Estructura Básica](#estructura-básica)
- [Elementos y Etiquetas](#elementos-y-etiquetas)
- [Atributos Globales](#atributos-globales)
- [Mejores Prácticas](#mejores-prácticas)

# Introducción a HTML

HTML (HyperText Markup Language) es el lenguaje de marcado estándar para crear páginas web. Es la base de toda la web moderna y funciona en conjunto con CSS para el estilo y JavaScript para la interactividad. HTML proporciona la estructura semántica del contenido, permitiendo a los navegadores renderizar páginas web de manera correcta y accesible.

## Estructura Básica

La estructura básica de un documento HTML es fundamental para que funcione correctamente:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Título de la Página</title>
  </head>
  <body>
    <h1>Contenido Principal</h1>
    <p>Este es un párrafo de texto.</p>
  </body>
</html>
```

- `<!DOCTYPE html>`: Declara que es un documento HTML5
- `<html>`: Elemento raíz que contiene todo el documento
- `<head>`: Contiene metadatos e información sobre la página
- `<body>`: Contiene el contenido visible de la página

## Elementos y Etiquetas

### Encabezados

Los encabezados se usan para estructurar jerárquicamente el contenido:

- `<h1>` a `<h6>`: Títulos del más importante al menos importante
- Solo debe haber un `<h1>` por página para SEO

### Párrafos y Texto

- `<p>`: Párrafo
- `<strong>`: Texto importante (negrita semántica)
- `<em>`: Texto enfatizado (itálica semántica)
- `<mark>`: Texto resaltado
- `<small>`: Texto pequeño
- `<del>`: Texto tachado
- `<ins>`: Texto insertado/subrayado

### Listas

```html
<!-- Lista ordenada -->
<ol>
  <li>Primer elemento</li>
  <li>Segundo elemento</li>
</ol>

<!-- Lista sin ordenar -->
<ul>
  <li>Elemento</li>
  <li>Elemento</li>
</ul>

<!-- Lista de definiciones -->
<dl>
  <dt>Término</dt>
  <dd>Definición</dd>
</dl>
```

### Enlaces e Imágenes

- `<a href="url">`: Enlace de navegación
- `<img src="ruta" alt="descripción">`: Insertar imagen
- `<figure>` y `<figcaption>`: Para imágenes con descripción

### Elementos Multimedia

- `<video>`: Para videos embebidos
- `<audio>`: Para archivos de audio
- `<iframe>`: Para incrustar contenido externo

## Atributos Globales

Los atributos globales se pueden usar en cualquier elemento HTML:

- `id`: Identificador único del elemento
- `class`: Clases CSS para estilizar
- `style`: Estilos CSS inline
- `title`: Tooltip al pasar el mouse
- `data-*`: Atributos de datos personalizados
- `aria-*`: Atributos de accesibilidad
- `lang`: Idioma del contenido

## Mejores Prácticas

1. **Semántica**: Usa elementos semánticos como `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>` y `<footer>`

2. **Accesibilidad**: Siempre proporciona texto alternativo en imágenes y usa etiquetas asociadas con formularios

3. **SEO**: Usa meta tags, encabezados estructurados y contenido descriptivo

4. **Validación**: Valida tu HTML usando validadores online para asegurar que sea correcto

5. **Performance**: Minimiza el HTML, optimiza las imágenes y usa atributos como `loading="lazy"`

6. **Responsive**: Usa `<meta name="viewport">` para hacer tu sitio responsive en dispositivos móviles

7. **Formularios accesibles**: Siempre asocia etiquetas `<label>` con campos `<input>` usando el atributo `for`
