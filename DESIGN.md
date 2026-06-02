# DESIGN.md — Dra. Katherine Cuentas Pacheco

Estética: **editorial / nude / piel**. Cálido, natural, sofisticado. Nada clínico-frío.
Anclado en sus fotos reales: vestido vino, joyas doradas, bata blanca, mármol.

## Color (OKLCH)
Estrategia: cálida comprometida — marfil de fondo, terracota (clay) como acento que
carga la marca, vino como momento dramático (sección contacto), bronce en detalles.

- --bg        oklch(0.972 0.013 78)   marfil cálido
- --bg-2      oklch(0.948 0.020 72)   arena
- --bg-3      oklch(0.912 0.030 58)   blush-arena
- --ink       oklch(0.285 0.028 48)   espresso (texto)
- --ink-2     oklch(0.460 0.030 46)   marrón suave (secundario)
- --clay      oklch(0.605 0.125 46)   terracota (acento principal)
- --clay-600  oklch(0.530 0.130 42)   terracota botones/hover
- --wine      oklch(0.360 0.085 24)   vino (tags)
- --wine-deep oklch(0.250 0.050 27)   fondo sección contacto
- --cream     oklch(0.966 0.018 80)   texto sobre oscuro
- --blush     oklch(0.900 0.038 40)   relleno suave
- --bronze    oklch(0.700 0.065 78)   filetes finos
- --line      oklch(0.872 0.018 62)   hairlines

## Tipografía
- Display/títulos: **Gilda Display** (serif delicada, beauty). Usada grande.
- Cuerpo/UI/labels: **Hanken Grotesk** (300–700).
- Escala fluida con clamp(); jerarquía por tamaño + peso + color. Eyebrow en
  mayúsculas con tracking, usada con moderación (no sobre cada sección).

## Componentes
- Botón pill clay con sombra cálida; variante ghost con borde hairline.
- Foto hero en arco (border-radius 200px arriba) + ring de bronce + halo blush + chip.
- Servicios: índice editorial (número Gilda + título + descripción + flecha), no cards.
- FAQ: acordeón animando grid-template-rows (no height).
- Contacto: panel vino oscuro con texto crema; formulario → WhatsApp.
- WhatsApp flotante (clay, no verde neón para no romper la paleta).

## Motion
- Reveal on scroll (IntersectionObserver, stagger por data-delay), ease-out (cubic 0.22,1,0.36,1).
- Respeta prefers-reduced-motion.
- Nunca animar propiedades de layout.

## Servidor de preview
launch.json → "katherine" → http://localhost:8805
