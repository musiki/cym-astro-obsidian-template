# Template de Astro-Obsidian para blogs de Ciencia y Música 

Esta es una plantilla para convertir tu bóveda de Obsidian en un sitio web público con Astro. 



## Primeros pasos

### 1. El método más fácil: Deploy en Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/musiki/cym-astro-obsidian-template)

### 2. Pullea el repo en tu computadora local

```bash
git clone https://github.com/musiki/cym-astro-obsidian-template.git
cd cym-astro-obsidian-template
```

### 3. Instala las dependencias

```bash
npm install
```

### 4. Corre el servidor de desarrollo

```bash
npm run dev
```

El sitio estará en `http://localhost:4321`.

### 5. Agrega tus notas en la carpeta src/content/

Abre la carpeta `src/content/` como vault en Obsidian y agrega tus notas en formato Markdown.

> [!TIP]
> Chequea el frontmatter de tus notas. Ver sección [Frontmatter](#Frontmatter) más abajo.

---

## ¿Qué hace esto?

Esta plantilla convierte tus notas de Obsidian en un sitio web público y navegable para Ciencia y Música. Soporta `[[wikilinks]]`, callouts `[!NOTE]`, búsqueda integrada, y más.

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
git clone https://github.com/musiki/cym-astro-obsidian-template.git
cd cym-astro-obsidian-template
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
- 💬 Reportar issues: [GitHub Issues](https://github.com/musiki/cym-astro-obsidian-template/issues)

---
desarrollado por @zztt @musiki para cym UNTREF
Licencia: MIT
