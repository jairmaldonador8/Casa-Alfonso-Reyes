# Casa Alfonso Reyes · Montana Realty Co.

Landing page exclusiva para la propiedad **EB-VY7877** de Montana Realty Co., ubicada en Palo Blanco, San Pedro Garza García, sobre Av. Alfonso Reyes.

**Propiedad:** Casa de 350 m² sobre 158 m² · 4 recámaras + departamento independiente · 4.5 baños · 2 estacionamientos techados · paneles solares · cisterna 5,000 L · acceso a parque privado.

**Precio:** $13,500,000 MXN

**Pincali:** https://www.pincali.com/inmobiliarios/montanar_1/inmueble/se-vende-casa-av-alfonso-reyes

---

## Stack

Sin build, sin dependencias, sin framework. Todo en un solo archivo HTML con CSS y JS inline. Las imágenes se cargan directamente desde el CDN de EasyBroker (las mismas que ve Pincali).

- **HTML + CSS + JS vanilla** (un solo `index.html`)
- **Imágenes:** servidas vía `assets.easybroker.com` (siempre actualizadas si el broker las actualiza en EasyBroker)
- **Tipografías:** Playfair Display (display/serif) + Outfit (sans), vía Google Fonts
- **Mapa:** iframe de Google Maps centrado en Av. Alfonso Reyes, Palo Blanco
- **Deploy:** Vercel, GitHub Pages, Netlify, o cualquier servidor estático

---

## Secciones

1. **Hero** — Fachada de la casa + título + precio + CTAs
2. **Ribbon de stats** — 7 datos clave (recámaras, baños, m², paneles solares, etc.)
3. **Pieza arquitectónica** — Ubicación privilegiada sobre Alfonso Reyes
4. **Overview** — Vista interior + descripción narrativa
5. **Galería carrusel** — 9 imágenes con auto-scroll + lightbox al tocar
6. **Ficha técnica** — 4 bloques de datos + grid de 8 features con iconos
7. **Tour de espacios** — 6 espacios con auto-scroll vertical
8. **Ubicación** — Mapa Google + amenidades cercanas (UDEM, Prepa Tec, Muguerza)
9. **CTA / Formulario** — 3 pasos con scoring interno y dispatch a WhatsApp
10. **Footer**
11. **Sticky WhatsApp FAB** abajo a la derecha

---

## Formulario · filtrado de leads → WhatsApp

El formulario califica al lead en 3 pasos:

- **Paso 1 — Identidad:** nombre, WhatsApp, correo
- **Paso 2 — Intent:** intereses (chips), urgencia, forma de compra
- **Paso 3 — Budget:** rango de inversión ($10M-$13M, $13M-$16M, $16M+) + mensaje

Score interno (A · HOT / B · WARM / C · NURTURE) basado en urgencia + forma de compra + presupuesto. Al enviar, arma un mensaje formateado y abre `wa.me/528123532365` en nueva pestaña.

---

## Cómo modificar el número de WhatsApp

Buscar y reemplazar `528123532365` en el archivo. Aparece en:

- Sticky FAB
- Footer (`tel:` y `wa.me`)
- Función `submitLead()`

---

## Cómo intercambiar fotos

Las imágenes están servidas desde `assets.easybroker.com/property_images/5977877/...`. Si el broker sube nuevas fotos a EasyBroker, se reflejan automáticamente. Para usar otras fotos, busca el `src` en `index.html` y reemplázalo.

---

## Deploy

### Vercel (recomendado)
```
npx vercel --prod
```

### GitHub Pages
1. Push a GitHub
2. Settings → Pages → Branch: `main`, folder: `/`

### Netlify
Drag & drop en https://app.netlify.com/drop

---

## Créditos

- **Diseño & desarrollo:** VITA Studio
- **Cliente:** Montana Realty Co.
- **Propiedad:** EB-VY7877 · Casa Alfonso Reyes, Palo Blanco
- **Año:** 2026
