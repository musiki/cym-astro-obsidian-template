# Digital Obsidian Garden

Esta es una plantilla para convertir tu bóveda de Obsidian en un sitio web público con Astro.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME)

---

## ¿Qué hace esto?

Esta plantilla convierte tus notas de Obsidian en un sitio web público y navegable. Soporta `[[wikilinks]]`, callouts `[!NOTE]`, búsqueda integrada, y más.

## Instalación rápida (Deploy to Vercel)

Haz clic en el botón "Deploy with Vercel" arriba. Esto:
1. Crea una copia del repositorio en tu GitHub
2. Lo publica automáticamente en Vercel
3. Te da una URL pública donde ver tu sitio

Luego solo necesitás añadir tus notas `.md` en la carpeta `src/content/`.

## Estructura de archivos y Frontmatter

### ¿Dónde pongo mis notas?

Pon tus archivos `.md` en la carpeta `src/content/`. Podés organizarlos en subcarpetas temáticas:
- `bibliografía/` - referencias bibliográficas
- `conceptos/` - términos y definiciones
- `personas/` - biografías y perfiles
- `etc.`

### Frontmatter

Cada nota debe tener un bloque de metadatos al inicio:

```yaml
---
title: "Título de la Nota"
description: "Descripción corta."
pubDate: "2025-10-08"
img: "/mi-imagen.jpg"
---
```

El campo `img` es opcional. Las imágenes van en la carpeta `public/`.

## Desarrollo local (Opcional)

Si quisieras editar el sitio localmente:

### Prerrequisitos

- Node.js (versión 18+)

### Instalación

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
cd YOUR_REPOSITORY_NAME
npm install
npm run dev
```

El sitio estará en `http://localhost:4321`.

### Publicar cambios

```bash
git add .
git commit -m "Mis cambios"
git push
```

Vercel actualiza automáticamente tu sitio.

## Plugins y Configuración

Esta plantilla incluye configuración especial para Obsidian:

- Soporte completo para `[[wikilinks]]`
- Callouts: `[!NOTE]`, `[!WARNING]`, `[!TIP]`, etc.
- Búsqueda integrada con índices
- RSS feed automático
- Syntax highlighting para código

## Personalización básica

### Cambiar título del sitio

Edita `src/consts.ts`:

```typescript
export const SITE_TITLE = 'Mi Digital Garden';
export const SITE_DESCRIPTION = 'Mis notas públicas de Obsidian';
```

### Añadir imágenes

Pon las imágenes en la carpeta `public/` y referencialas en el frontmatter:

```yaml
---
img: "/mi-imagen.jpg"
---
```

## Soporte

Si tenés problemas:
- 📚 Docs de Astro: [astro.build](https://astro.build)
- 💬 Reportar issues: [GitHub Issues](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME/issues)

---

Licencia: MIT
