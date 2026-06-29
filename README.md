# Figuras de Colección 3D — Tienda Online

**Proyecto de Parcial 2 — Interacción con Dispositivos Móviles**  
Profesor: Jorge Pérez  
Alumno: Rafael Amaya (rafa.amaya82@email.com)

---

## Descripción del Proyecto

Sitio web de una tienda online ficticia especializados en figuras de colección impresas en 3D y pintadas a mano. El proyecto implementa una solución responsiva y moderna utilizando **Bootstrap 5**, HTML5 semántico y CSS personalizado, adaptándose a diferentes dispositivos (móviles, tablets, desktop).

**Características principales:**
- Catálogo de 8 productos (figuras temáticas de películas, anime y videojuegos)
- Página de detalle de producto con galería, opciones de pago y características
- Formulario de contacto responsivo
- Navegación collapsible (hamburguesa en móvil)
- Carousel (carrusel) con banners promocionales
- Maquetación basada en grid Bootstrap y componentes personalizados

---

## Estructura del Proyecto

```
Tp_Final/
├── index.html                    # Página principal con 7 secciones
├── producto-detalle.html         # Página de detalle de producto
├── css/
│   ├── index.css                 # Estilos personalizados para index.html
│   ├── detalle.css               # Estilos personalizados para producto-detalle.html
│   └── estilos.css               # Estilos originales (conservado para referencia)
├── img/
│   ├── carousel/                 # Imágenes de banners del carousel
│   │   ├── banner-robocop.jpg
│   │   ├── banner-mazinger.jpg
│   │   └── banner-heman.jpg
│   ├── productos/                # Imágenes de las 8 figuras en venta
│   │   ├── tortuga-ninja.jpg
│   │   ├── robocop.jpg
│   │   ├── espadachin-azul.jpg
│   │   ├── mazinger.jpg
│   │   ├── he-man.jpg
│   │   ├── maestro-artes-marciales.jpg
│   │   ├── depredador.jpg
│   │   └── mago.jpg
│   ├── detalle/                  # Imágenes de galería para detalle de producto
│   │   ├── robocop-detalle-1.jpg
│   │   └── robocop-detalle-2.jpg
│   └── foto-perfil.jpg           # Foto del alumno en footer
├── .gitignore                    # Archivo de configuración git
└── README.md                     # Este archivo

```

---

## Secciones de la Página Principal

### 1. **Navbar (Navegación)**
- Componente Bootstrap navbar con collapse automático en breakpoints menores a `lg`
- Brand "Figuras 3D" con logo/texto
- Menú de navegación: Inicio, Productos, Nuestro Proceso, Contacto
- Personalización: fondo oscuro (#241a1d), borde dorado (#b4882f), hover en oro

### 2. **Carousel (Carrusel)**
- 3 imágenes de banners promocionales (He-Man, Mazinger Z, RoboCop)
- Aspect ratio 16:7, controles y indicadores
- Captions con descripción, borde traslúcido personalizado
- Responsivo: mantiene proporciones en todos los breakpoints

### 3. **Introducción a la Empresa**
- Sección "Sobre nosotros" con 2 párrafos de descripción
- Incluye card con lista de valores (List Group personalizado)
- Semántica: `<section>`, `<article>`, `<h2>`, `<p>` con refuerzo semántico (`<strong>`, `<em>`)

### 4. **Productos (Catálogo)**
- Grid responsivo con 8 figuras de colección
- Breakpoints: 
  - **xs (< 576px)**: 1 columna
  - **md (≥ 768px)**: 2 columnas
  - **lg (≥ 992px)**: 3 columnas
  - **xl (≥ 1200px)**: 4 columnas
- Cada pastilla incluye: título, imagen, descripción, precio y botón "Comprar"
- Efecto hover desktop: overlay transparente con información; en móvil info siempre visible
- Botones enlazan a `producto-detalle.html`

### 5. **Sección Libre — "Nuestro Proceso de Impresión 3D"**
- 2 párrafos descriptivos sobre el proceso de producción
- 1 imagen ilustrativa
- **Implementa Flexbox**: layout horizontal en `md+` (flex-md-row), apilado en móvil
- Semántica: `<section>`, `<article>`, `<figure>`, `<figcaption>`

### 6. **Contacto**
- Formulario con campos: Nombre, Email, Teléfono, Comentario
- Labels explícitos y campos requeridos
- **Responsive**: 
  - **xs/sm**: 1 columna (inputs apilados)
  - **md+**: 2 columnas (Nombre/Email en fila, Teléfono/Comentario en fila)
- Card lateral con información de contacto (dirección, teléfono, email)
- Semántica: `<form>`, `<label>`, `<input>`, `<textarea>`

### 7. **Footer**
- Información de la empresa
- Datos del alumno (nombre, edad, email, redes sociales)
- Foto de perfil (250px de ancho)
- Enlaces a redes sociales (Instagram, LinkedIn, X/Twitter)

---

## Página de Detalle de Producto

**Archivo**: `producto-detalle.html`

**Contenido:**
- Navbar idéntica a index.html con enlaces de navegación
- Galería de imágenes (1 imagen principal + 2 detalles en grid)
- Card de producto con precio, descripción y características
- **Accordion personalizado** con "Opciones de pago":
  - Pago único con tarjeta
  - Financiación en cuotas (3 cuotas sin interés, 6 cuotas con interés)
  - Envío y retiro
- Descripción extendida con semántica `<article>`
- Sidebar con características (List Group con iconos)
- Footer idéntico al de index.html

---

## Componentes Bootstrap Utilizados

1. ✅ **Navbar** — collapsible en breakpoints menores a lg
2. ✅ **Carousel** — 3 imágenes, indicadores, controles
3. ✅ **Card** — producto, información, características
4. ✅ **Badge** — etiquetas "Nuevo" y "Oferta" en pastillas
5. ✅ **List Group** — valores de empresa, características de producto
6. ✅ **Accordion** — opciones de pago en detalle de producto
7. ✅ **Form Controls** — campos de formulario con labels
8. ✅ **Grid System** — layout responsivo con clases col-*

**Todos los componentes están personalizados** mediante CSS propio (colores, espaciados, efectos) para diferenciarse de la documentación oficial de Bootstrap.

---

## Diseño Responsivo — Breakpoints

El sitio se adapta a **5 breakpoints** de Bootstrap 5:

| Breakpoint | Ancho | Cambios principales |
|-----------|-------|-------------------|
| **xs** | < 576px | Navbar collapsed, grid 1 col, formulario vertical, Flexbox apilado |
| **sm** | ≥ 576px | Idem xs |
| **md** | ≥ 768px | Grid 2 cols (productos), formulario 2 cols, Flexbox horizontal |
| **lg** | ≥ 992px | Grid 3 cols (productos), navbar expandido, hover en pastillas |
| **xl** | ≥ 1200px | Grid 4 cols (productos), layout completo desktop |

**Prueba en navegador:**
- Desktop 1680px: layout en 4 columnas, navbar expandido, sin scroll horizontal ✓
- Tablet 768px: layout en 2 columnas, navbar collapsa en sm ✓
- Móvil 375px: layout 1 columna, formulario apilado, Flexbox apilado ✓

---

## Personalización CSS

### **Paleta de colores:**
- **Oscuro primario**: #241a1d (navbar, footer)
- **Dorado/Acento**: #b4882f (bordes, hover, componentes activos)
- **Blanco**: #ffffff (texto en fondos oscuros)
- **Grises**: para textos secundarios

### **Efectos personalizados:**
- **Navbar**: borde inferior dorado, hover en enlaces con color oro
- **Carousel**: aspect-ratio 16/7, caption con borde traslúcido
- **Pastillas producto**: border-radius, shadow, overlay hover con transition
- **Accordion**: botón activo con fondo dorado, focus con shadow oro
- **List Group**: bordes removidos, separadores finos en dorado
- **Flexbox (sección libre)**: ancho limitado de imagen (320px), apilamiento responsivo

### **Archivos CSS:**
- `css/index.css` (127 líneas) — estilos específicos para index.html
- `css/detalle.css` (73 líneas) — estilos específicos para producto-detalle.html
- `css/estilos.css` (original, conservado)

---

## Características Técnicas

✅ **HTML5 semántico** — uso correcto de `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`  
✅ **Accesibilidad** — `alt` en imágenes, `labels` en formulario, `aria-label` en iconos  
✅ **Responsivo** — sin scroll horizontal en ningún viewport  
✅ **Flexbox** — sección libre implementa layout flexible responsivo  
✅ **Imágenes optimizadas** — todas locales, pesos 10–197 KB, aspect-ratio controlados  
✅ **CDN Bootstrap 5.3.8** — carga desde jsDelivr con integridad  
✅ **Validación HTML** — estructura válida y bien indentada

---

## Cómo Ejecutar Localmente

### **Opción 1: Abrir en navegador (más simple)**
1. Descomprime el archivo `IDM-AMAYA-PARCIAL_2.zip`
2. Abre `index.html` en tu navegador (Chrome, Firefox, etc.)
3. La navegación y enlaces funcionan sin necesidad de servidor

### **Opción 2: Servir con Python (recomendado para probar mejor)**
1. Descomprime el archivo
2. Abre terminal/cmd en la carpeta del proyecto
3. Ejecuta:
   ```bash
   python -m http.server 8000
   ```
   o (Python 2):
   ```bash
   python -m SimpleHTTPServer 8000
   ```
4. Abre en navegador: `http://localhost:8000`

### **Opción 3: Servir con Node.js (http-server)**
1. Instala globalmente:
   ```bash
   npm install -g http-server
   ```
2. En la carpeta del proyecto:
   ```bash
   http-server -p 8000
   ```
3. Abre: `http://localhost:8000`

---

## Navegación y Enlaces

**Desde index.html:**
- Navbar → Inicio (reload a index.html)
- Navbar → Productos (anchor a #productos)
- Navbar → Nuestro Proceso (anchor a #libre)
- Navbar → Contacto (anchor a #contacto)
- Botones "Comprar" en pastillas → `producto-detalle.html`

**Desde producto-detalle.html:**
- Logo "Figuras 3D" → vuelve a `index.html`
- Navbar → Inicio, Productos, Nuestro Proceso, Contacto (todos anchorean en index.html)
- Botón "Comprar ahora" → salta a #productos en index.html
- Botón "Seguir viendo productos" → vuelve a `index.html`

---

## Decisiones de Diseño Justificadas

1. **Paleta de colores (oscuro + dorado)**
   - Evoca un ambiente premium y artesanal
   - Contraste alto para legibilidad
   - Coherencia con temática de figuras coleccionistas

2. **Navbar con collapse**
   - Óptimo para móviles (ahorra espacio)
   - Expande en desktop para fácil acceso
   - Animación suave (Bootstrap por defecto)

3. **Carousel como encabezado**
   - Captura atención inmediata
   - Muestra productos destacados (He-Man, Mazinger, RoboCop)
   - Aspect ratio 16:7 óptimo para banners en desktop

4. **Grid 4-3-2-1 columnas**
   - Desktop: visualiza múltiples productos sin scroll excesivo
   - Tablet: balance entre espacio y legibilidad
   - Móvil: 1 columna para facilitar tap (accesibilidad)

5. **Efecto hover (overlay) en pastillas**
   - Desktop: info aparece al pasar mouse (interactivo)
   - Móvil: info siempre visible (no hay hover)
   - Flexbox para centrado perfecto

6. **Flexbox en sección "Nuestro Proceso"**
   - Imagen + texto lado a lado en desktop
   - Apilado en móvil para mejor lectura
   - Ancho limitado de imagen (320px) para control visual

7. **Accordion para opciones de pago**
   - Agrupa información extensa sin saturar la página
   - Interactividad dinámica (Bootstrap)
   - Fácil lectura (despliego a demanda)

8. **Formulario con 2 columnas (md+)**
   - Aprovecha espacio horizontal en desktop
   - Se adapta a 1 columna en móvil (optimal para inputs)

---

## Validación y Pruebas Realizadas

- ✅ HTML válido (estructura semántica, sin errores de sintaxis)
- ✅ CSS personalizado aplicado correctamente (sin errores de herencia)
- ✅ Responsive en 3+ breakpoints (xs, md, lg, xl)
- ✅ Imágenes optimizadas y locales (no hay URLs externas)
- ✅ Enlaces internos funcionales (navbar, botones, anchors)
- ✅ Formulario con labels y atributos requeridos
- ✅ Sin scroll horizontal en viewport 1680px (Chrome, Firefox)
- ✅ Componentes Bootstrap personalizados (no son idénticos a la doc)

---

## Tecnologías Utilizadas

- **HTML5** — estructura semántica
- **CSS3** — estilos personalizados, media queries, Flexbox
- **Bootstrap 5.3.8** — framework responsive via CDN
- **Bootstrap Icons 1.11.3** — íconos (Instagram, LinkedIn, X)
- **No JavaScript** — excepto el bundle de Bootstrap (interactividad navbar, carousel, accordion)

---

## Archivos Incluidos en el ZIP

```
IDM-AMAYA-PARCIAL_2.zip
└── Tp_Final/
    ├── index.html
    ├── producto-detalle.html
    ├── css/
    │   ├── index.css
    │   ├── detalle.css
    │   └── estilos.css
    ├── img/
    │   ├── carousel/ (3 banners)
    │   ├── productos/ (8 figuras)
    │   ├── detalle/ (2 detalles de RoboCop)
    │   └── foto-perfil.jpg
    ├── .gitignore
    └── README.md
```

**Peso total aproximado**: ~ 1.5 MB (imágenes incluidas)

---

## Contacto y Créditos

**Alumno**: Rafael Amaya  
**Email**: rafa.amaya82@email.com  
**Materia**: Interacción con Dispositivos Móviles  
**Profesor**: Jorge Pérez  
**Institución**: Instituto de Desarrollo Multimedia (IDM)  

**Redes sociales**:
- [Instagram](https://www.instagram.com/rafi.amaya/)
- [LinkedIn](https://www.linkedin.com/in/rafael-amaya/)
- [X / Twitter](https://x.com/RafaAmaya82)

---

## Notas Finales

- Este proyecto fue creado con fines educativos para demostrar habilidades en maquetación responsiva con Bootstrap 5
- No incluye backend ni funcionalidades de carrito/pago (solo mockups visuales)
- El formulario de contacto es estático (no procesa datos)
- Todos los productos y descripciones son ficticios

**Fecha de entrega**: 29 de junio de 2026  
**Estado**: Completado ✅

