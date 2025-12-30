# páginaWebFundamentos - Álvaro Henche Redondo - DDD

## Descripción del proyecto

Este repositorio contiene una página web estática multipágina desarrollada como entrega para la asignatura "Fundamentos de Ingeniería Informática" (UFV). El objetivo es presentar un portfolio académico y profesional con información sobre el grado, el curriculum vitae, contacto y una sección que muestra previews de sitios de compañeros.

El sitio está diseñado para ser ligero, accesible y fácilmente desplegable en GitHub Pages sin necesidad de procesamiento en servidor.

## Características principales

- Sitio multipágina HTML estático (sin JavaScript necesario).
- Estilos centralizados en `docs/css/styles.css` con variables CSS, Grid y Flexbox.
- Previews de sitios de compañeros en `net.html`, implementadas mediante iframes con overlay para evitar interacción accidental.
- Enfoque en accesibilidad: atributos `alt`, estados de foco visibles y carga diferida donde procede.

## Estructura del repositorio

Raíz del proyecto:

- `readme.md` — este documento.
- `docs/` — carpeta con los recursos públicos que sirven la web.
	- `index.html` — página principal (si existe en `docs/`).
	- `css/styles.css` — estilos globales.
	- `images/` — imágenes y recursos gráficos.
- `public/` — páginas finales (about.html, contact.html, degree.html, fii.html, net.html, navbar.html, topic.html).


## Tecnologías y convenciones

- HTML5 semántico.
- CSS moderno: variables, Grid, Flexbox, media queries.
- Recursos optimizados (SVG cuando es posible, imágenes comprimidas).

## Ver el proyecto 

Haga click en el siguente enlace para ver el proyecto desplegado en GitHub Pages:
[Ver página web](https://alvaro-henche-redondo.github.io/paginaWebFundamentos/)

## Despliegue en GitHub Pages

Pasos básicos:

1. Crear un repositorio en GitHub y subir el contenido.
2. En las settings del repositorio, en la sección "Pages", seleccionar la rama y la carpeta (`/docs` o `/root`) según dónde esté el `index.html` que quiere servir.
3. Esperar a que GitHub procese el sitio y visitar la URL proporcionada.

Consejos:

- Si el sitio se sirve desde `/docs`, mantenga rutas relativas en los enlaces y recursos.
- Para dominios personalizados, configurar el `CNAME` en la rama correspondiente.

## Decisiones de diseño y accesibilidad

- Un único archivo CSS facilita la coherencia visual y el mantenimiento.
- Uso de Grid y Flexbox para layouts adaptativos y control fino de la rejilla de tarjetas.
- Se priorizó HTML semántico para mejorar la accesibilidad y el SEO básico.
- Estados de foco y contraste revisados para navegación por teclado.

Previews (iframes):

- Los iframes fueron escalados mediante `transform: scale()` para mantener proporciones visuales y una altura fija.
- Se añadió una capa overlay transparente para bloquear interacciones directas con el iframe, evitando arrastres y selecciones; debajo queda un enlace "Visitar sitio →" que abre la página original.

## Problemas encontrados y soluciones

1. Responsive de iframes: se mitigó con un contenedor que aplica `transform: scale()` y `overflow: hidden` para evitar desbordes.
2. Interacción no deseada: overlay bloqueando clicks; único punto activable es el enlace externo.
3. Optimización de imágenes: uso de SVGs y compresión para reducir peso sin perder calidad.
4. Ajuste de breakpoints: pruebas en móviles (320–480px) y tabletas para asegurar legibilidad y accesibilidad.
5. Coherencia sin JS: uso cuidadoso de variables CSS y reglas de especificidad para evitar conflictos.

## Conclusión

- A pesar de las limitaciones de un sitio estático sin JavaScript, se logró una experiencia visual atractiva y funcional, se ha conseguido superar los retos técnicos y así logrando un proyecto sólido y bien estructurado que cumple con los objetivos académicos y personales planteados.
