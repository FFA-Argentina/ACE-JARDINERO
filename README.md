# 🌿 Ayudante de Jardinería

Una Progressive Web App (PWA) para gestionar tu jardín: inventario de plantas, tareas, calendario y más — instalable en cualquier dispositivo.

---

## ✨ Características

- **Inventario de plantas** con fotos, frecuencia de riego, sustrato, ubicación y notas
- **Identificación de plantas por foto** usando IA (Claude Vision)
- **Calendario de tareas** con alertas: riego, abono, poda, tratamientos
- **Clima + fase lunar** en tiempo real para planificación
- **Inventario de insumos** con lista de compras automática
- **Archivo de bajas** para plantas retiradas
- **Funciona offline** — instalable como app en Android, iOS, Windows y macOS

---

## 📱 Instalación como app

### Android (Chrome)
1. Abrí la URL en Chrome
2. Tocá los tres puntos → **"Agregar a pantalla de inicio"**
3. La app se instala como app nativa

### iPhone / iPad (Safari)
1. Abrí la URL en Safari
2. Tocá el botón **Compartir** → **"Añadir a pantalla de inicio"**

### Desktop (Chrome / Edge)
1. Abrí la URL
2. Hacé clic en el ícono de instalación en la barra de direcciones
3. Confirmá la instalación

---

## 🚀 Deploy en GitHub Pages

```bash
# 1. Cloná o forkear este repositorio
git clone https://github.com/TU_USUARIO/jardin-app.git
cd jardin-app

# 2. Activar GitHub Pages en Settings → Pages → Branch: main / root

# La app queda disponible en:
# https://TU_USUARIO.github.io/jardin-app/
```

### Alternativas gratuitas de hosting

| Plataforma | Comando / Pasos |
|---|---|
| **GitHub Pages** | Settings → Pages → Branch main |
| **Netlify** | Arrastrá la carpeta a [netlify.com/drop](https://app.netlify.com/drop) |
| **Vercel** | `npx vercel` en la carpeta del proyecto |
| **Cloudflare Pages** | Conectar repo en [pages.cloudflare.com](https://pages.cloudflare.com) |

---

## 🔑 Configuración de IA (identificación de plantas)

La función de identificación de plantas usa la API de Anthropic (Claude).  
El proyecto ya incluye la llamada a la API — **necesitás una API key** de [console.anthropic.com](https://console.anthropic.com).

> ⚠️ **Para producción:** No expongas tu API key en el frontend. Implementá un proxy backend simple (ver `docs/backend-proxy.md`).

---

## 🗂️ Estructura del proyecto

```
jardin-app/
├── index.html          # App principal (HTML + CSS + JS en un solo archivo)
├── manifest.json       # Web App Manifest (PWA)
├── sw.js               # Service Worker (offline + caché)
├── icons/              # Íconos en todos los tamaños requeridos
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── icon-128.png
│   ├── icon-144.png
│   ├── icon-152.png
│   ├── icon-192.png
│   ├── icon-384.png
│   └── icon-512.png
└── README.md
```

---

## 🛠️ Tecnologías

- **HTML5 / CSS3 / Vanilla JS** — sin frameworks, sin dependencias de build
- **Service Worker API** — caché offline y soporte de notificaciones push
- **Web App Manifest** — instalación nativa multiplataforma
- **Geolocation API** — clima basado en ubicación real
- **Notification API** — recordatorios de tareas de jardín
- **Claude AI (Anthropic)** — identificación de plantas por foto

---

## 📄 Licencia

MIT — libre para uso personal y comercial.
