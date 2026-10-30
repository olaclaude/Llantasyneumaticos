# MR Automoción

Aplicación web responsive para explorar vehículos, consultar sus fichas y gestionar anuncios desde un panel de demostración.

## Desarrollo local

Requisitos: Node.js 20 o superior y npm.

```bash
npm ci
npm run dev
```

## Build y despliegue en Vercel

El proyecto está preparado para Vercel con Vite. Configuración esperada:

- **Framework preset:** Vite
- **Install command:** `npm install` (también funciona `npm ci`)
- **Build command:** `npm run build`
- **Output directory:** `dist`
- **Root directory:** raíz del repositorio

Para validar el build localmente:

```bash
npm ci
npm run build
npm run preview
```

Vercel debe desplegar desde la raíz; no hace falta una carpeta de proyecto anidada ni subir los artefactos `dist/` o `node_modules/` al repositorio.

## Alcance y limitaciones

Este es un prototipo frontend. Los coches que se añaden, favoritos y cambios del panel se guardan en `localStorage` del navegador: no se sincronizan entre dispositivos ni usuarios. El panel de propietario no tiene autenticación, y las fotos cargadas se guardan como datos locales en el navegador. Por tanto, el despliegue en Vercel sirve la aplicación, pero **no proporciona por sí solo base de datos, almacenamiento compartido ni protección del panel**.

Antes de usarlo como servicio real, hay que implementar autenticación y autorización de propietario, persistencia y almacenamiento de imágenes (por ejemplo, con un backend), además de preparar los avisos legales y de privacidad aplicables. Los cuatro vehículos iniciales son ejemplos y los datos de contacto y stock deben revisarse antes de publicar.

## Personalización

- Perfil de Instagram: constante `IG` en `src/main.jsx`.
- Contenido y vehículos de ejemplo: `src/main.jsx`.
- Estilos: `src/style.css`.
- Imágenes: `public/`.
