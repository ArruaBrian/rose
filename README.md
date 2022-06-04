# <center><span style="color:#978bda; font-family: 'Courier New';">:sparkles: **Rose Proyect** :sparkles:</span></center>

> :smiley: Proyecto final para la plataforma <a href="https://www.coderhouse.com/" target="__blank">CoderHouse</a>

<br>

* Puntos a tener en cuenta para el proyecto

    * Buenas practicas y estructura en HTML
    * Uso de snippets y estructura en CSS
    * CSS avanzado con SASS
    * Utilización del framework Bootstrap
    * Subida al servidor

---

## <span style="color:#ccc; font-family:'Courier New';">**Sass** :zap:</span>

---
<br>

El proyecto esta enteramente hecho en SASS, su archivo madre se encuentra en `./src/scss/main.scss`

Este archivo contiene solo el diseño de las paginas y las dependencias, pero lo que realmente importa se encuentra en `./src/scss/base/_base.scss`

El archivo `_base.scss` es el constructor de las paginas, donde se importan todas las dependencias (las cuales se encuentran por separado, para tener un control sobre estas, mayor facilidad y orden para editar) y a su vez el archivo base se importa dentro de la hoja de estilo de cada pagina y terminan en el archivo main.

<br>

<center><a href="https://imgur.com/Db20nsI"><img src="https://i.imgur.com/Db20nsI.png" title="source: imgur.com" /></a></center>

<br>

La razón por la cual esto se hizo asi fue para disminuir el tiempo que uno pasa importando cada vez que quiera crear una sección o componente nuevo (dependiente de los módulos scss).


<br>

---

## <span style="color:#ccc; font-family:'Courier New';">**Bootstrap** :rage:</span>

---

<br>

Bootsrap fue implementado en este proyecto a través de NPM, puesto que me daría acceso a los archivos .sccs los cuales precisaba para hacer cambios específicos dentro del código fuente del mismo. Sin embargo, el JS de bootstrap fue implementado de manera diferente, en especifico se uso el link CDN del mismo.

Este se encuentra en `./node_modules/bootstrap` pero fue importado desde el main en `./src/scss/main.scss`

<br>

``` scss

// ++++++++++++++++++++++++++++ Bootstrap ++++++++++++++++++++++++++++++++++++++

// Funciones

@import '../../node_modules/bootstrap/scss/functions';

// Variables

@import '../../node_modules/bootstrap/scss/variables';

// Dependencias importantes 

@import '../../node_modules/bootstrap/scss/maps';
@import '../../node_modules/bootstrap/scss/mixins';
@import '../../node_modules/bootstrap/scss/root';

// Bootstrap (modificaciones)

@import './componentes/boostrap--edit';


// Tooltip (estilos del elementos JS)

@import'../../node_modules/bootstrap/scss/tooltip';
@import'../../node_modules/bootstrap/scss/popover';

// Modal

@import'../../node_modules/bootstrap/scss/modal';


// Transiciones 

@import'../../node_modules/bootstrap/scss/transitions';

```

<br>

Por otra parte, las modificaciones de bootstrap se hicieron a través de las variables sccs dentro del archivo `./scr/scss/componentes/_bootstrap--edit.scss`

<br>

``` scss

// Boostrap MODAL =====================================================================

$modal-content-bg: linear-gradient(to right, white 0%, colors.$violeta 140%);
$modal-footer-border-color: transparent;
$modal-header-border-color: transparent;
$modal-header-padding: 15px 30px 15px 30px;
$modal-inner-padding: 15px 30px 15px 30px;
$modal-content-border-radius: 15px 60px 15px 60px;

// Boostrap TOOLTIP =====================================================================

$tooltip-bg: linear-gradient(to right, white 0%, colors.$violeta 140%);
$tooltip-color: colors.$azul__a;
$tooltip-arrow-color: colors.$violeta;
$tooltip-arrow-height: 1.2rem;

```

<br>

### <span style="color:#ccc; font-family:'Courier New';">**Componentes utilizados** :zap:</span>

<br>

* Modal en el "Home"

<br>

<center><a href="https://imgur.com/TaicKTI"><img src="https://i.imgur.com/TaicKTI.png" title="source: imgur.com" /></a></center>

<br>

* Collapse en "Precios"

<br>

<center><img src="https://i.imgur.com/bhcxGa6.png" title="source: imgur.com" /></center>

<br>

* Tooltip en "Contacto"

<center><img src="https://i.imgur.com/XoPb3AL.png" title="source: imgur.com" /></center>

---

## <span style="color:#ccc; font-family:'Courier New';">**Subida al servidor** :blush:</span>

---

<br>

Se utilizaron 2 host para este proyecto, para fines prácticos usando las distintas herramientas que se nos proporciono:

* <a href="https://roseproyect.netlify.app" target="__blank">Netlify</a>
* <a href="https://rosewd.000webhostapp.com/" target="__blank">000WebHost</a>








