# Dra. Katherine Cuentas Pacheco · Dermatología

Landing page de la Dra. Katherine Cuentas Pacheco, dermatóloga clínica y estética en
Barranquilla (Centro Médico Chicago).

**En vivo:** https://landing-katherine-cuentas.vercel.app

## Stack

Sitio estático autocontenido: HTML + CSS + JS vanilla. Sin build.

- Tipografías: Gilda Display + Hanken Grotesk + Allura (Google Fonts).
- Animación: GSAP 3.13 (core + ScrollTrigger + MorphSVGPlugin) vía CDN.
- Hosting: Vercel.
- Formulario de contacto: compone un mensaje de WhatsApp con los datos del paciente
  y abre `wa.me`.

## Estructura

```
index.html              # toda la página
assets/
  logo-katherine.png    # logo (fondo transparente)
  dra-katherine-retrato.jpeg
  dra-katherine-clinica.jpeg
robots.txt
sitemap.xml
PRODUCT.md  DESIGN.md   # contexto de marca
```

## Desarrollo local

Cualquier servidor estático sirve. Por ejemplo:

```bash
python3 -m http.server 8805
# abrir http://localhost:8805
```

## Despliegue

Conectado a Vercel: cada `git push` a `main` despliega a producción.

Si necesitas desplegar manualmente:

```bash
vercel deploy --prod
```

## Configuración rápida (`index.html`, bloque `CONFIG`)

```js
const CONFIG = {
  whatsapp: "573003226768",
  saludo: "Hola Dra. Katherine, vengo de su página web…",
  instagram: "https://www.instagram.com/drakatherine.dermatologa/",
  mapsUrl: "https://www.google.com/maps/search/?api=1&query=…"
};
```

## SEO

- Schema.org `Physician` + `MedicalBusiness` con dirección y especialidad.
- Open Graph + Twitter Card.
- `robots.txt` + `sitemap.xml`.
- Cuando actives Search Console, descomenta el `<meta name="google-site-verification">`
  en `index.html` y pega tu code.
