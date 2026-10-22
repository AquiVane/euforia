# HANDOFF — euforia (euforia.cosmart.com.ar)

## 22/10 — Hosting migrado de GitHub Pages a Cloudflare Pages
- **Motivo:** los términos de GitHub Pages no permiten usarlo como hosting de un negocio/e-commerce. Pedido de Vaneh.
- **Ahora:** proyecto **Cloudflare Pages `euforia`** (preview `euforia-9dl.pages.dev`) conectado a `AquiVane/euforia`, rama `main`, sin build, salida = raíz. Dominio personalizado: `euforia.cosmart.com.ar`. Cada push a `main` se publica solo. GitHub Pages **despublicado**; se borró `CNAME`.
- **Backend:** no cambió. Formulario UNIRME, pagos y referidos van contra `euforia-worker` (repo `cosmart-workers`), que acepta cualquier origen.
- **Comportamiento:** `/x.html` redirige (308) a `/x`; una URL inexistente devuelve el `index.html` con 200. Verificado en desktop y mobile: inicio, `/unirme`, `/suscripcion` (Mercado Pago + PayPal cargan) y `/base`.
- **Pendiente detectado, no tocado:** el sitio carga `www.cosmart.com.ar/hm.js` (mapa de calor) y esa dirección devuelve 404.

## 22/10 — Rediseño mobile de la home (index.html)
- Bloques CSS `MOBILE v2` y `MOBILE v3` al final del `<style>` (≤900px): header mínimo (53px, logo sin achicar: se recorta el PNG con padding transparente), sin tarjetas (todo en listas con líneas finas), secciones con fondo y espaciado uniformes.
- **Paleta (regla de Vaneh):** celeste = marcas, naranja de marca `#e87c5a` = creadoras (y acentos de viajes). Se unificaron los naranjas/rojos/vino/dorado en un solo naranja. Botones de acción de marca (incl. "Quiero cobertura turística") en celeste; "Soy creadora" y "Me interesa sumarme" en naranja.
- Solo se tocó `index.html`. `unirme`, `suscripcion` y `base` quedan sin retocar (pendiente si Vaneh quiere el mismo estilo).
