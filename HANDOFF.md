# HANDOFF — euforia (euforia.cosmart.com.ar)

## 22/10 — Hosting migrado de GitHub Pages a Cloudflare Pages
- **Motivo:** los términos de GitHub Pages no permiten usarlo como hosting de un negocio/e-commerce. Pedido de Vaneh.
- **Ahora:** proyecto **Cloudflare Pages `euforia`** (preview `euforia-9dl.pages.dev`) conectado a `AquiVane/euforia`, rama `main`, sin build, salida = raíz. Dominio personalizado: `euforia.cosmart.com.ar`. Cada push a `main` se publica solo. GitHub Pages **despublicado**; se borró `CNAME`.
- **Backend:** no cambió. Formulario UNIRME, pagos y referidos van contra `euforia-worker` (repo `cosmart-workers`), que acepta cualquier origen.
- **Comportamiento:** `/x.html` redirige (308) a `/x`; una URL inexistente devuelve el `index.html` con 200. Verificado en desktop y mobile: inicio, `/unirme`, `/suscripcion` (Mercado Pago + PayPal cargan) y `/base`.
- **Pendiente detectado, no tocado:** el sitio carga `www.cosmart.com.ar/hm.js` (mapa de calor) y esa dirección devuelve 404.
