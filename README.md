# InnovationTech — Sitio web

Servicios digitales con IA para negocios locales: páginas web, chatbots de
WhatsApp y presencia digital.

## Páginas

| Archivo | Descripción |
|---------|-------------|
| `index.html` | Página principal (servicios, precios, FAQ, contacto) |
| `demo.html` | Demo: tortería "Tortas Tortuga" con chatbot de WhatsApp |
| `showroom.html` | Showroom interactivo de los 3 servicios |

Contacto: WhatsApp **+1 210-990-0532**

## Publicar con GitHub Pages

1. En este repo: **Settings → Pages**
2. **Source:** Deploy from a branch → **Branch:** `main` → **/(root)** → **Save**
3. En 1–2 min el sitio queda en:
   `https://innovationtech1.github.io/webpage/`

## Dominio personalizado (innovationtech1.com)

1. Compra el dominio (Namecheap / Cloudflare, ~$12/año).
2. En **Settings → Pages → Custom domain** escribe `innovationtech1.com`.
3. En el DNS del dominio agrega los registros A de GitHub Pages
   (`185.199.108.153`, `.109.153`, `.110.153`, `.111.153`) y un CNAME de `www`
   hacia `innovationtech1.github.io`. Activa **Enforce HTTPS**.
