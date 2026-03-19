# NEXUS-AI
NEXUS AI — Interfaz de chat con inteligencia artificial construida sobre Claude Sonnet. Diseño oscuro premium con partículas animadas, renderizado de Markdown, historial de conversación y efecto typewriter en las respuestas. Una sola página HTML, sin dependencias.
[README.md](https://github.com/user-attachments/files/26125262/README.md)
# ⚡ NEXUS AI

> Interfaz de chat con inteligencia artificial de última generación, impulsada por Claude Sonnet de Anthropic.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Claude](https://img.shields.io/badge/Claude_Sonnet-CC785C?style=for-the-badge&logo=anthropic&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## 🌟 Vista previa

NEXUS AI es una aplicación web de chat con inteligencia artificial construida como **single-page application** en HTML, CSS y JavaScript puro — sin frameworks, sin dependencias, sin complicaciones.

Una interfaz oscura y premium inspirada en terminales futuristas, con partículas animadas en canvas, efectos de neón y respuestas renderizadas en tiempo real.

---

## ✨ Características

- 🤖 **IA real** — Conectada al modelo `claude-sonnet-4-20250514`, el más avanzado de Anthropic
- 💬 **Historial de conversación** — El contexto se mantiene durante toda la sesión
- ✍️ **Efecto typewriter** — Las respuestas aparecen como si se escribieran en tiempo real
- 📝 **Markdown completo** — Código, listas, encabezados, negritas, citas y bloques de código
- 🎨 **Diseño premium** — Fondo animado con partículas, efectos glow y glassmorphism
- 📋 **Copiar mensajes** — Botón para copiar cualquier respuesta al portapapeles
- 💾 **Exportar chat** — Descarga la conversación completa en `.txt`
- 🗂️ **Sidebar de sesiones** — Historial visual de conversaciones anteriores
- 🚀 **Sugerencias de inicio** — Accesos rápidos para empezar a chatear
- 📱 **Responsive** — Adaptado para móvil, tablet y escritorio
- ⚡ **Sin dependencias** — Solo una línea de Google Fonts, nada más

---

## 🚀 Inicio rápido

### Opción A — Abrir directamente en el navegador

```bash
# Descarga el archivo y ábrelo con doble clic
# Compatible con Chrome, Firefox, Edge, Safari
```

> ✅ Funciona sin instalación ni servidor

### Opción B — Servidor local (recomendado para desarrollo)

```bash
# Con Python
python -m http.server 8000

# Con Node.js
npx serve .

# Luego abre http://localhost:8000
```

---

## 🔑 Configuración de API Key

Para usar NEXUS AI fuera del entorno de Claude.ai necesitas una API Key de Anthropic.

### 1. Obtener tu API Key

1. Regístrate en [anthropic.com](https://www.anthropic.com)
2. Ve a **API Keys** en tu dashboard
3. Genera una nueva clave

### 2. Añadirla al código

Abre `index.html` y busca la función `callClaude`. Añade el header de autorización:

```javascript
const response = await fetch("https://api.anthropic.com/v1/messages", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
    "x-api-key": "TU_API_KEY_AQUÍ",          // ← Añade esta línea
    "anthropic-version": "2023-06-01",         // ← Y esta
    "anthropic-dangerous-direct-browser-calls": "true"  // ← Y esta
  },
  body: JSON.stringify({ ... })
});
```

> ⚠️ **Importante:** No subas tu API Key a repositorios públicos. Usa variables de entorno si despliegas en un servidor.

---

## 🌐 Despliegue

### GitHub Pages (gratis)

```bash
# 1. Crea un repositorio en GitHub
# 2. Sube index.html
git init
git add .
git commit -m "🚀 Initial commit — NEXUS AI"
git push origin main

# 3. Ve a Settings → Pages → Branch: main → Save
# URL: tuusuario.github.io/nexus-ai
```

### Netlify (gratis, 30 segundos)

1. Ve a [netlify.com](https://netlify.com)
2. Arrastra y suelta la carpeta del proyecto
3. ✅ URL pública instantánea

### Vercel (gratis)

```bash
npm i -g vercel
vercel
```

---

## 🗂️ Estructura del proyecto

```
nexus-ai/
│
├── index.html        # Aplicación completa (HTML + CSS + JS)
└── README.md         # Este archivo
```

Todo en un único archivo autocontenido. No hay build, no hay npm install, no hay configuración.

---

## 🛠️ Tecnologías

| Tecnología | Uso |
|---|---|
| HTML5 Canvas | Fondo animado con partículas y conexiones |
| CSS3 | Variables, animaciones, grid layout, glassmorphism |
| JavaScript ES6+ | Lógica de chat, llamadas a API, renderizado de Markdown |
| Google Fonts | Syne (display) + DM Mono (código) + DM Sans (texto) |
| Anthropic API | Motor de inteligencia artificial (Claude Sonnet) |

---

## 📄 Licencia

MIT License — libre para uso personal y comercial.

---

## 👤 Autor

Desarrollado con ⚡ y mucho café.

---

<div align="center">
  <strong>⚡ NEXUS AI — Inteligencia Sin Límites</strong>
</div>
