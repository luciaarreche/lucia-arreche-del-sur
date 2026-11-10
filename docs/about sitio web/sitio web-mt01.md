<div style="position: relative; height: 0;">
  <img src="/lucia-arreche-del-sur/images/ia/mucha%20ia.png"
       alt="Sello de colaboración: Alta IA"
       style="position: absolute; width: 55px; height: auto; right: 75px; transform: translateY(-25px);">
</div>
# Sobre este sitio

*PHASIS — Procesos en estado crudo*

PHASIS es una bitácora digital desarrollada en el marco de la Especialización en Fabricación Digital e Innovación Abierta de UTEC.

Este sitio funciona como un espacio de documentación, experimentación y aprendizaje. Reúne procesos, ejercicios, herramientas y reflexiones que surgen durante el recorrido formativo.

Su construcción también forma parte de ese proceso. Diseñar la bitácora implica aprender a trabajar con nuevos lenguajes y herramientas, tomar decisiones sobre cómo organizar y presentar la información, experimentar con recursos visuales y resolver problemas que aparecen durante el desarrollo.

Más que un soporte terminado, PHASIS se plantea como un espacio en transformación, donde el contenido y la propia estructura del sitio se construyen simultáneamente.

## 01 / Pensar el sitio

La identidad de PHASIS se construye alrededor de tres ideas: pensar con las manos, explorar las relaciones entre lo sensible y lo técnico, y prestar atención a aquello que emerge durante los procesos.

Estas ideas orientan tanto la documentación de los ejercicios como las decisiones visuales y estructurales de la web.
## 02 / La arquitectura del sitio

PHASIS está organizada a partir de una estructura de carpetas y archivos que permite separar los contenidos, los recursos visuales y la configuración general de la web.

La carpeta `docs` reúne las páginas y los materiales que se muestran en el sitio. Cada módulo tiene su propio espacio, mientras que las imágenes, los archivos de fabricación y las hojas de estilo se organizan en carpetas específicas.

```text
PHASIS
│
├── docs/
│   ├── index.md
│   ├── about/
│   ├── about sitio web/
│   ├── tecnicos/
│   ├── diseno/
│   ├── innovacion/
│   ├── proyecto/
│   ├── images/
│   ├── files/
│   └── stylesheets/
│       └── extra.css
│
└── mkdocs.yml
```

Esta organización permite que los contenidos puedan crecer y modificarse sin tener que reconstruir el sitio completo.
## 03 / Los lenguajes de la web

Durante la construcción de PHASIS fui reconociendo tres lenguajes que intervienen en el funcionamiento del sitio: Markdown, CSS y YAML. Cada uno cumple una función diferente y, en conjunto, permiten organizar, configurar y diseñar la bitácora.

### Markdown / El contenido

Markdown es el lenguaje que utilizo para escribir y estructurar las páginas. Los archivos `.md` contienen los textos, títulos, imágenes y enlaces que forman parte de cada módulo.

Por ejemplo, para organizar los apartados de una página:

```markdown
# MT03 — Del modelo al material

## 01 / Aproximación

## 02 / El ejercicio: Ghast

## 03 / Del modelo al material
```

El símbolo `#` establece niveles de jerarquía. De esta manera, el contenido puede organizarse sin tener que definir manualmente su apariencia.

### CSS / La apariencia

CSS (*Cascading Style Sheets*) permite intervenir en la presentación visual del sitio: dimensiones, colores, márgenes, tipografías y efectos.

En PHASIS utilizo el archivo `extra.css` para desarrollar una identidad visual propia, más allá de la configuración inicial de MkDocs.

Por ejemplo, para que una imagen se desvanezca progresivamente:

```css
mask-image: linear-gradient(
  to bottom,
  transparent 0%,
  black 30%,
  black 65%,
  transparent 100%
);
```

Este recurso fue utilizado para integrar imágenes al fondo de las páginas, evitando que se perciban como elementos rectangulares independientes.

### YAML / La configuración

YAML es el lenguaje utilizado para configurar el sitio mediante el archivo `mkdocs.yml`.

Allí se define el nombre de la web, su estructura de navegación, el tema visual y las extensiones que permiten incorporar funcionalidades.

Por ejemplo:

```yaml
site_name: PHASIS

nav:
  - Inicio: index.md
  - Sobre mí: about/me.md
```

Mientras Markdown organiza el contenido y CSS define su apariencia, YAML establece cómo se configura y articula el sitio.

Los tres lenguajes se complementan: modificar uno puede transformar la manera en que se presenta o funciona el conjunto.
## 04 / Herramientas y flujo de trabajo

La construcción de PHASIS implicó familiarizarme con herramientas que hasta ahora no formaban parte de mi práctica habitual de diseño. El proceso combinó la escritura de contenidos, la edición de código, la organización de archivos y la visualización de resultados.

### VS Code / El espacio de trabajo

Visual Studio Code es el editor desde el que construyo y modifico la bitácora.

Desde allí puedo acceder a las carpetas del proyecto, editar los archivos Markdown, intervenir en las hojas de estilo CSS y modificar la configuración del sitio.

Una de las primeras cosas que aprendí fue a reconocer la relación entre los archivos y sus ubicaciones. Las rutas permiten vincular imágenes, documentos y otros recursos con las páginas donde aparecen.

### MkDocs / De los archivos a la web

MkDocs permite transformar los archivos Markdown en un sitio web navegable. Utilizo el tema Material for MkDocs como punto de partida para su presentación visual.

Durante el desarrollo, ejecuto desde la terminal de VS Code:

```bash
mkdocs serve
```

Este comando inicia un servidor local que permite visualizar PHASIS en el navegador y observar los cambios a medida que modifico los archivos.

Aprendí también a diferenciar la vista previa de Markdown en VS Code de la visualización real del sitio en Chrome. Algunos recursos gráficos y rutas de imágenes no se interpretan de la misma manera en ambos entornos.

### Git y GitHub / El registro de versiones

Git permite registrar los cambios realizados en los archivos del proyecto, mientras que GitHub funciona como repositorio remoto donde puede alojarse una copia del trabajo.

Durante el proceso comencé a reconocer algunos indicadores de VS Code:

- `M` (*Modified*): archivo modificado respecto de la versión registrada en Git.
- `U` (*Untracked*): archivo nuevo que todavía no fue incorporado al seguimiento de Git.

También aprendí que guardar un archivo en la computadora no equivale a registrar una versión en Git ni a subirla a GitHub.

### Un proceso de prueba y ajuste

El trabajo no siguió una secuencia completamente lineal. Muchas decisiones surgieron al visualizar resultados, identificar problemas y volver a intervenir los archivos.

El procedimiento habitual consiste en modificar el código, guardar los cambios, observar su resultado en el navegador y realizar nuevos ajustes cuando es necesario.

De esta manera, la construcción del sitio se convierte también en una práctica de experimentación y aprendizaje.
## 05 / Diseñar mientras se aprende

Construir PHASIS implicó abordar el diseño desde un territorio que no me resultaba familiar: la programación y la construcción de sitios web.

Al principio, las decisiones se concentraron en comprender la estructura del proyecto y lograr que los contenidos se visualizaran correctamente. A medida que fui reconociendo las herramientas, comenzaron a aparecer preguntas vinculadas con la identidad visual y la experiencia de navegación.

### De la imagen al espacio

Uno de los desafíos fue integrar los recursos visuales sin que funcionaran simplemente como imágenes rectangulares insertadas entre párrafos.

A través de intervenciones en CSS, experimenté con transparencias, degradados, escalas y posiciones para generar imágenes que parecen emerger del fondo, atravesar los márgenes o desvanecerse en la página.

Estas exploraciones aparecen en distintos sectores de PHASIS: el prisma iridiscente de la presentación personal, el personaje flotante del módulo MT03 y las texturas luminosas incorporadas en Innovación.

### El error como parte del proceso

Durante la construcción surgieron dificultades relacionadas con rutas de archivos, imágenes que no aparecían, diferencias entre las vistas previas y el navegador, y estilos CSS que no producían los resultados esperados.

Resolver estos problemas implicó revisar el código, identificar las relaciones entre archivos y comprender progresivamente cómo funciona el sitio.

En lugar de entenderlos únicamente como obstáculos, estos errores se convirtieron en oportunidades para reconocer la lógica de las herramientas.

### Una identidad en construcción

PHASIS no parte de una identidad visual completamente definida. Su lenguaje se desarrolla a través de pruebas, decisiones y ajustes sucesivos.

La luz, la refracción, las transparencias y los fragmentos visuales funcionan como recursos para expresar algo del propio proceso de aprendizaje: las relaciones entre lo sensible y lo técnico, entre las ideas y su materialización.

En ese sentido, diseñar el sitio y documentar los ejercicios no son actividades separadas. Ambas forman parte de una misma exploración.

La bitácora no solamente registra lo que aprendo: también permite observar cómo aprendo.
---
## 06 / Registro de colaboración con IA

Los sellos de colaboración permiten hacer visible cómo interviene la inteligencia artificial en los procesos documentados en PHASIS.

No representan el valor ni la autoría del trabajo, sino las modalidades de participación de la IA. En todos los casos, las decisiones de orientación, selección, curaduría y evaluación forman parte del proceso de diseño.

![Panel de referencia de los sellos de colaboración con IA](../images/ia/panel%20de%20referencia.png)

*Este sitio se encuentra en construcción.*

PHASIS es un espacio abierto y en permanente desarrollo. Sus contenidos, su estructura y su identidad visual continuarán transformándose a medida que avance el proceso de aprendizaje, incorporando nuevas experiencias, herramientas y formas de explorar.