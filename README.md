# UOC Boilerplate

UOC Boilerplate is a starter template for the HTML and CSS Tools courses from the [Master's Program in Multimedia Applications](https://estudis.uoc.edu/ca/masters-universitaris/aplicacions-multimedia/presentacio) and the [Master's Program in Web App and Website Development](https://estudis.uoc.edu/ca/masters-universitaris/desenvolupament-llocs-aplicacions-web/presentacio) at the [Universitat Oberta de Catalunya](https://www.uoc.edu). It aims to provide a basic, modern frontend web development starter pack based on Parcel and including a Sass compiler, an ES6 transpiler, minifiers, an image transformer, and development tools.

This is the 3.x version of UOC Boilerplate, available since the UOC 2020-2 semester.

## Requirements

[Node.js](http://nodejs.org/) >= 14.15.x

## Getting started

Clone this repository with `git clone`, or download a .zip file using the top right green button.

Using the Terminal, navigate to the project folder and run `npm install`.

## Features

- Uses [Parcel v2](https://parceljs.org) module bundler.
- NPM scripts for fast development and production build (see Commands below).

### Stylesheets

- [Sass/SCSS](https://sass-lang.com) to CSS compilation.
- Minification and optimization of CSS files on production builds with [`cssnano`](https://github.com/cssnano/cssnano) (`@parcel/optimizer-cssnano`).
- [PostCSS](https://postcss.org/) features:
  - Transpile modern CSS with [`postcss-preset-env`](https://preset-env.cssdb.org/features).
  - Automatically add CSS prefix to unsupported properties with [`autoprefixer`](https://autoprefixer.github.io/).

### HTML

- Minification and optimization of CSS files on production builds [`htmlnano`](https://github.com/posthtml/htmlnano) (`@parcel/optimizer-htmlnano`).
- [PostHTML](https://github.com/posthtml/posthtml) features:
  - Include partial HTML files with [`posthtml-include`](https://github.com/posthtml/posthtml-include).

### Scripts

- Allow for modern JavaScript (ES201x/ES8/ES7/ES6…) which is automatically transpiled to ES5 and minifed in production builds, with [Babel](https://babeljs.io/).

### Images

- Image transformation with [`@parcel/transformer-image`](https://parceljs.org/recipes/image/) (based on [`sharp`](https://sharp.pixelplumbing.com/)).

### Development

- Development server launch and live reloading on file changes.
- Friendly error reporting.

## How to use this boilerplate

Content lives inside the `src/` folder. If you do not want to change the configuration or are unsure about what you are doing, do not edit files outside the `src/` folder.

Always run the following commands during the development stage and for production builds. Please note that it is expected that all projects built with this boilerplate are compiled using `npm run build` before they are published.

### Commands

| Command         | Description                                                                                                                                                                                                                                                                                                                                                         |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `npm run dev`   | Runs a local web server for development and opens the browser to display it. Automatically compiles styles and scripts whenever a file in `src/` is changed, and live reloads the browser. This is what _must be run_ on the development stage.                                                                                                                     |
| `npm run build` | Compiles and minifies and optimizes the files in the assets folder. The generated compiled and optimized files are located in the `dist/` folder. This is what _must be run_ before publishing the project. This is also the build command to be run by external deployment services such as Netlify. The publishable files are then located in the `dist/` folder. |
| `npm run clean` | Deletes the current `/dist` folder and cache folders.                                                                                                                                                                                                                                                                                                               |
| `npm run test`  | Displays a success message if everything is working as expected.                                                                                                                                                                                                                                                                                                    |

## Need help? / Want to help out?

Feel free to create a [new issue](https://github.com/uoc-advanced-html-css/uoc-boilerplate/issues/new/) or drop me a line at jorditarrida@uoc.edu.

Are you using this Boilerplate for your projects or for educational purposes? I would love to hear about it!

## Pasos realizados

Para comenzar he clonado [el proyecto](https://github.com/uoc-advanced-html-css/uoc-boilerplate/), instalado las dependencias y he probado que todo funcionaba correctamente levantando el proyecto.

Para clonar el proyecto

```js
git clone https://github.com/uoc-advanced-html-css/uoc-boilerplate.git
```

Para instalar las dependencias: `npm install`

Probar el proyecto: `npm run dev`

Para acelerar el comienzo de la aplicación, he partido de las modificaciones que había realizado en la PEC1 de esta asignatura,
para tener las configuraciones creadas.

### Bootstrap

Para la instalación de bootstrap, he seguido estos pasos que indican como configurarlo con Parcel: https://getbootstrap.com/docs/5.0/getting-started/parcel/

He importado en el css el móduilo de bootstrap, el apartado de Custom.css, para luego realizar modificaciones como se indicaba
en la teoría. He añadido el componente card, para comprobar que funcionaba correctamente el css y el componente del header,
para comprobar que los efectos de JS. también estaban importados correctamente.

------------------------------------
UTILIZAR FLEX Y GRID
Uso de Grid y @supports (15%)


### Imágenes

Obtenidas con licencia libre:

- https://www.wallpaperflare.com/search?wallpaper=chess+rook

Las imágenes de los avatares: https://avatoon.me/free-cartoon-avatars/

### Datos ajedrez

Los datos de los miembros del club, los he obtenido de la página: https://www.chess.com/es/players

En la sección de Club, ocultamos la descripción de los miembros, cuando se visualiza la pantalla en ancho muy pequeñ.

### Wiframe

Se ha procedido a utilizar el Wiframe que se facilita el enunciado, para diseñar y maquetar acorde a su estructura.

### Responsive

Para conseguir que la página sea responsive, inicialmente vamos a optar por el uso de css estándar con funcionalidades como Flex.

### Dependencias de terceros

Para las dependencias de terceros, vamos a hacer uso de la que se indica en el módulo 1, con [FontAwesome](https://fontawesome.com/docs/web/setup/host-yourself/webfonts#reference-font-awesome-in-your-project).

`npm install --save @fortawesome/fontawesome-free`

Con el comando indicado, se instalará en la carpeta node_modules y nos actualizará los ficheros de package.json y package-lock.json.

Luego vamos a nuestro main.scss e importamos la el all.min.css para hacer uso de la dependencia de css.

` @import "../../../node_modules/@fortawesome/fontawesome-free/css/all.min.css";`

Y luego en el index.html añadimos un icono, para comprobar que funciona correctamente.

### Metodologias CSS

De las metodologías CSS indicadas en el módulo 2, vamos a utilizar la de [BEM](https://getbem.com/).

### [Stylelint](https://stylelint.io/)

Instalamos la dependencia de stylelint y style-scss dado que estamos usando sass:

`npm install --save-dev stylelint-scss stylelint-config-recommended-scss`

Posteriomente creamos el archivo de configuración .stylelinttrc, y añadimos la configuración recomandada para scss.

```js
{
  "extends": ["stylelint-config-recommended-scss"],
  "rules": {}
}
```

Y dado que habíamos elegido la metodología BEM, para que nos valide los nombre creados, el fichero qyedaría así:

```js
{
  "extends": ["stylelint-config-recommended-scss"],
  "rules": {"selector-class-pattern": "^.[a-z]([a-z0-9-]+)?(__([a-z0-9]+-?)+)?(--([a-z0-9]+-?)+){0,2}$"}
}
```

Para finalizar, añadimos la configuración el package.json para que pueda lanzar el stylelint más fácilmente.

```js
"stylelint": "stylelint src/**/*.scss",
```

Además, lo añadiremos al comando de build, para que cuando lanzamos el comando de construcción de la carpeta dist, nos valide también el css.

```js
"build": "npm-run-all clean stylelint parcel:build",
```

### Sobre decisiones del diseño

He decidio realizar la maquetación *desktop first* para que el diseño se adapte a diferentes tamaños de monitor, pero sin llegar al formato móvil.
Esta decisión la he tomado, porque para las maquetaciones *mobile first* y que sea adaptativa, tendría que crear un diseño y un contenido adaptado a los dispositivos móviles.

## Github

A través de mi cuenta de Github, he creado un nuevo proyecto y lo he enlazado.

- [La URL de Gitub](https://github.com/)
- [URL de proyecto creado](https://github.com/jesuscuesta/PEC2-css2)

Una vez creado, he borrador la carpeta oculta de .git y he enlazado el proyecto con el creado, con este comando: `git remote add origin https://github.com/jesuscuesta/PEC2-css2`

## Netlify

Me he logado en la web de [Netlify]([Netlify](https://app.netlify.com/) con mi usuario de github.

## Completar la aplicación

### SASS

Para añadir más contenido con SASS hemos hecho uso de las variables y los mixing.

Hemos creado en el ficero _variables unas propiedades para que se adapte mejor a los diferentes tamaños, teniendo en cuenta
los Breakponts definidos en Material Design:
Breakpoints Material Design

- 600px: para pantallas de tamaño small.
- 1024px: para pantallas de tamaño medium.
- 1440px: para pantallas de tamaño large.

Posteriomente, hemos creado un Mixin para hacer la web más responsiva y que utilizase estos tamaños.

Todo el css validado con Stylelint.
