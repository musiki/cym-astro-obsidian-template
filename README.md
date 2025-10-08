# Plantilla Astro para Publicar Bóvedas de Obsidian

¡Hola! Esta es una plantilla para que puedas convertir tu bóveda de notas de [Obsidian](https://obsidian.md/) en un sitio web público y navegable, usando [Astro](https://astro.build/).

El objetivo es que no necesites saber programar. Solo tenés que escribir tus notas en Markdown y este proyecto se encarga del resto.

---

## ¿Cómo se usa? (El Resumen Rápido)

1.  **Descargá el Proyecto:** Hacé clic en el botón verde "Use this template" en GitHub y luego en "Create a new repository". O si preferís, descargá el ZIP.
2.  **Abrí el Proyecto:** Descomprimí el archivo y abrí la carpeta con [Visual Studio Code](https://code.visualstudio.com/).
3.  **Instalá las dependencias:** Abrí una terminal en VS Code (`Terminal > New Terminal`) y escribí el comando: `npm install`.
4.  **Iniciá el servidor de desarrollo:** En la misma terminal, escribí: `npm run dev`.
5.  **¡Listo!** Abrí tu navegador en la dirección que te indica la terminal (usualmente `http://localhost:4321`). Ya podés ver tu sitio.

Ahora, simplemente editá o creá nuevas notas en la carpeta `src/content/vault` y vas a ver los cambios reflejados en tu sitio local al instante.

---

## Guía de Instalación Detallada

### Paso 1: Preparación del Entorno (si es tu primera vez)

Si no tenés las herramientas instaladas, seguí estos pasos. Solo tenés que hacerlo una vez.

#### **Para usuarios de Windows:**

Se recomienda fuertemente usar **WSL (Windows Subsystem for Linux)**, que ya sabés usar.

1.  **Abrí tu terminal de WSL** (como Ubuntu, Debian, etc.).
2.  **Instalá Node.js:** Escribí el siguiente comando para instalar `nvm` (Node Version Manager), que te facilita manejar las versiones de Node:
    ```bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
    ```
    Cerrá y volvé a abrir la terminal de WSL. Luego, instalá la versión LTS (la más estable) de Node.js con:
    ```bash
    nvm install --lts
    ```
3.  **Instalá VS Code:** Si todavía no lo tenés, [descargalo desde su web oficial](https://code.visualstudio.com/). Es importante que también instales la extensión **"WSL"** desde el panel de extensiones de VS Code para que se integre correctamente con tu subsistema de Linux.

#### **Para usuarios de macOS o Linux:**

1.  **Abrí la Terminal.**
2.  **Instalá Node.js:** El método con `nvm` también es el recomendado acá. Es el mismo comando que en WSL:
    ```bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
    ```
    Luego, reiniciá la terminal e instalá Node con `nvm install --lts`.
3.  **Instalá VS Code:** [Descargalo desde su web oficial](https://code.visualstudio.com/).

### Paso 2: Tu Bóveda de Obsidian (¡La parte importante!)

**Toda la "magia" ocurre en la carpeta `src/content/vault`.**

Podés abrir esta carpeta (`cym-astro-obsidian-template/src/content/vault`) directamente como una bóveda en Obsidian, o simplemente copiar y pegar tus archivos `.md` adentro.

#### El Frontmatter de YAML

Para que Astro entienda tus notas y pueda mostrarlas en la galería o darles un título bonito, cada archivo `.md` debe empezar con un bloque de "frontmatter" en formato YAML. Es muy simple, fijate:

```yaml
---
title: "Este es un Post de Ejemplo"
description: "Acá podés ver cómo usar el frontmatter para añadir metadatos."
pubDate: "2025-10-08"
heroImage: "/placeholder-post.jpg"
tags: ["ejemplo", "astro", "obsidian"]
---

El resto de tu nota en Markdown va acá abajo...
```

**Campos disponibles:**

*   `title` (obligatorio): El título de tu nota.
*   `description` (opcional): Una descripción corta que aparecerá en la tarjeta de la galería.
*   `pubDate` (opcional): La fecha de publicación. Usá el formato `AAAA-MM-DD`.
*   `heroImage` (opcional): La ruta a una imagen de portada. Las imágenes deben estar en la carpeta `public/`. Por ejemplo, si tenés una imagen en `public/fotos/mi-foto.png`, acá escribirías `heroImage: "/fotos/mi-foto.png"`.
*   `tags` (opcional): Una lista de etiquetas para tu nota.

Fijate en los archivos `about.md` y `example-post.md` que están en `src/content/vault` para ver cómo funcionan.

### Paso 3: Publicando tu Sitio

La forma más fácil de publicar tu sitio gratis es con **Vercel**.

1.  Subí tu proyecto a un repositorio de **GitHub**.
2.  Creá una cuenta en [Vercel](https://vercel.com/) usando tu cuenta de GitHub.
3.  Desde el panel de Vercel, importá el repositorio de tu proyecto.
4.  Vercel detectará automáticamente que es un proyecto de Astro y lo configurará por vos. ¡Con un par de clics, tu sitio estará online!