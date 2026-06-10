<div align="center">

# KTitle Studio

**Generador de títulos animados para Kdenlive · Animated title generator for Kdenlive**

Una herramienta de un solo archivo HTML que genera archivos `.kdenlive` y `.kdenlivetitle` con títulos diseñados visualmente para Kdenlive 26.x.

A single-file HTML tool that generates `.kdenlive` and `.kdenlivetitle` files with visually designed titles for Kdenlive 26.x.

[Español](#español) · [English](#english)

</div>

---

## Español

### ¿Qué es?

KTitle Studio es un editor de títulos en el navegador que te permite diseñar títulos para tus videos de Kdenlive de forma visual, con vista previa en tiempo real. Está construido como un único archivo HTML sin dependencias externas (salvo Google Fonts), usando JavaScript puro y Canvas 2D.

El editor de títulos nativo de Kdenlive es funcional, pero diseñar tipografía, gradientes, sombras y composiciones con varias capas resulta incómodo. KTitle Studio te da una interfaz cómoda para hacer ese diseño, y exporta archivos que Kdenlive abre directamente.

### Características

- **Capas múltiples**: texto, rectángulos, elipses e imágenes
- **Texto avanzado**: fuente, tamaño, peso, itálica, subrayado, alineación, tracking, interlineado, color sólido o gradiente, contorno, sombra con desenfoque y desplazamiento, efecto máquina de escribir
- **Manipulación en canvas**: mover, escalar (proporcional desde esquinas), rotar
- **Línea de tiempo dinámica**: nodos arrastrables para controlar entrada, cuerpo y salida de cada capa
- **Animaciones**: fade, slide (con dirección arriba/abajo/izquierda/derecha) y scale, en entrada y salida
- **Reproducción**: play/pausa, bucle, navegación entre nodos, scrubbing
- **10 plantillas de diseño** listas para usar con vista previa
- **Aleatorizadores creativos**: fuentes, colores (con gradientes y sombras), animaciones
- **Detección de fuentes del sistema** (Windows, macOS, Linux)
- **Deshacer/Rehacer** (Ctrl+Z / Ctrl+Y)
- **Importar** títulos `.kdenlivetitle` o `.kdenlive` existentes para editarlos
- **Exportar** a `.kdenlive` (proyecto) o `.kdenlivetitle` (título importable)
- **Tema claro/oscuro** (automático + manual)
- **Diseño responsive** para escritorio y móvil
- **Paneles redimensionables**

### Uso

1. Abre `index.html` en tu navegador (o usa la versión publicada en GitHub Pages)
2. Diseña tu título: agrega capas, escribe texto, ajusta colores y animaciones
3. Exporta:
   - **Export Proyecto** descarga un `.kdenlive` que abres con *Archivo → Abrir* en Kdenlive
   - **`.kdenlivetitle`** descarga un título que importas desde el editor de títulos de Kdenlive (*Abrir documento*)

### Limitación conocida

Las animaciones (fade/slide/scale) **no** se guardan dentro del `.kdenlivetitle`. Esto es por diseño de Kdenlive: un título guarda solo el diseño visual, mientras que las animaciones son filtros MLT que viven en el clip de la línea de tiempo. Al exportar como `.kdenlive` (proyecto), las animaciones sí se incluyen como filtros del clip.

### Tecnología

- HTML + CSS + JavaScript puro (sin frameworks)
- Canvas 2D para renderizado
- Tailwind CSS compilado e incrustado (sin CDN)
- Cero dependencias de JavaScript externas

---

## English

### What is it?

KTitle Studio is a browser-based title editor that lets you visually design titles for your Kdenlive videos, with real-time preview. It is built as a single HTML file with no external dependencies (except Google Fonts), using pure JavaScript and Canvas 2D.

Kdenlive's native title editor works, but designing typography, gradients, shadows, and multi-layer compositions is cumbersome. KTitle Studio gives you a comfortable interface for that design work, and exports files that Kdenlive opens directly.

### Features

- **Multiple layers**: text, rectangles, ellipses, and images
- **Advanced text**: font, size, weight, italic, underline, alignment, tracking, line spacing, solid or gradient color, outline, shadow with blur and offset, typewriter effect
- **Canvas manipulation**: move, scale (proportional from corners), rotate
- **Dynamic timeline**: draggable nodes to control in / body / out of each layer
- **Animations**: fade, slide (with up/down/left/right direction), and scale, on entry and exit
- **Playback**: play/pause, loop, node navigation, scrubbing
- **10 ready-made design templates** with preview
- **Creative randomizers**: fonts, colors (with gradients and shadows), animations
- **System font detection** (Windows, macOS, Linux)
- **Undo/Redo** (Ctrl+Z / Ctrl+Y)
- **Import** existing `.kdenlivetitle` or `.kdenlive` titles to edit them
- **Export** to `.kdenlive` (project) or `.kdenlivetitle` (importable title)
- **Light/dark theme** (automatic + manual)
- **Responsive design** for desktop and mobile
- **Resizable panels**

### Usage

1. Open `index.html` in your browser (or use the published GitHub Pages version)
2. Design your title: add layers, type text, adjust colors and animations
3. Export:
   - **Export Proyecto** downloads a `.kdenlive` that you open via *File → Open* in Kdenlive
   - **`.kdenlivetitle`** downloads a title you import from Kdenlive's title editor (*Open Document*)

### Known limitation

Animations (fade/slide/scale) are **not** saved inside the `.kdenlivetitle`. This is by Kdenlive's design: a title stores only the visual layout, while animations are MLT filters that live on the timeline clip. When exporting as `.kdenlive` (project), the animations are included as clip filters.

### Technology

- Pure HTML + CSS + JavaScript (no frameworks)
- Canvas 2D for rendering
- Tailwind CSS compiled and inlined (no CDN)
- Zero external JavaScript dependencies

---

<div align="center">

**Copyright © 2026 Grafico Gabo** · Licensed under [GPL v3](LICENSE)

Hecho con ❤️ para la comunidad de Kdenlive · Made with ❤️ for the Kdenlive community

</div>
