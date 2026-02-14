# Curso de Terminal y Bash

Curso práctico de Terminal y Bash para principiantes, construido como una SPA (Single Page Application). Forma parte del programa de [Hazla con Datos](https://hazlacondatos.com/) y es complementario al [curso de configuración del entorno de desarrollo](https://paulovillarroel.github.io/configuracion-entorno/).

**[Ver el curso en vivo](https://paulovillarroel.github.io/curso-terminal-bash/)**

## Contenido

El curso está organizado en 9 módulos progresivos + ejercicios integradores:

| # | Módulo | Contenido |
|---|--------|-----------|
| 1 | Introducción | Qué es la terminal, shell, Bash vs Zsh, contexto para ciencia de datos |
| 2 | Primeros pasos | echo, whoami, date, pwd, ls, cd, rutas, Tab, historial |
| 3 | Archivos y directorios | mkdir, touch, cp, mv, rm, wildcards, tree, find |
| 4 | Visualización y búsqueda | cat, less, head, tail, grep, pipes, redirecciones |
| 5 | Editores de texto | Nano (completo), Vim (básico) |
| 6 | Permisos y administración | chmod (simbólico + octal), sudo, chown |
| 7 | Gestión de procesos | ps, top/htop, kill, segundo plano, Ctrl+C/Z |
| 8 | Bash scripting | Shebang, variables, read, if/else, for, while, funciones |
| 9 | Automatización con Cron | crontab, sintaxis, buenas prácticas |
| -- | Ejercicios finales | 7 ejercicios integradores con soluciones |

Cada módulo incluye explicaciones detalladas, advertencias para comandos peligrosos y ejercicios prácticos.

## Stack tecnológico

- [Astro 5](https://astro.build/) (template minimal, SPA)
- [Tailwind CSS v4](https://tailwindcss.com/) (via `@tailwindcss/vite`)
- [@tailwindcss/typography](https://github.com/tailwindlabs/tailwindcss-typography) (prose classes)
- [astro-expressive-code](https://expressive-code.com/) (code blocks con copy button y terminal frames)
- [@astrojs/mdx](https://docs.astro.build/en/guides/integrations-guide/mdx/) (contenido en MDX)
- Modo claro/oscuro con persistencia en localStorage
- Sin frameworks JS (React/Vue). Solo vanilla JS para intersection observer y menú móvil

## Desarrollo local

```bash
# Instalar dependencias
npm install

# Iniciar servidor de desarrollo
npm run dev

# Build de producción
npm run build

# Preview del build
npm run preview
```

## Estructura del proyecto

```
src/
├── styles/global.css            # Tailwind v4 + theme tokens + dark mode
├── layouts/Layout.astro         # HTML base (head, meta, fonts)
├── components/
│   ├── Sidebar.astro            # Nav fijo con intersection observer
│   ├── MobileNav.astro          # Hamburguesa + drawer
│   ├── ThemeToggle.astro        # Botón claro/oscuro
│   ├── ModuleSection.astro      # Wrapper por módulo
│   ├── Callout.astro            # Cajas info/warning/tip
│   ├── CommandTable.astro       # Tabla de referencia de comandos
│   ├── Hero.astro               # Sección de bienvenida
│   ├── ScrollToTop.astro        # Botón flotante
│   └── Footer.astro             # Pie de página
├── content/
│   ├── module-01.mdx … 09.mdx  # Contenido de los módulos
│   └── exercises.mdx            # Ejercicios finales
└── pages/
    └── index.astro              # Punto de entrada (importa todo)
```

## Deploy

El sitio está configurado para GitHub Pages con base path `/curso-terminal-bash`. Para deployar con GitHub Actions, crea el archivo `.github/workflows/deploy.yml` siguiendo la [guía de Astro para GitHub Pages](https://docs.astro.build/en/guides/deploy/github/).

## Licencia

Contenido bajo licencia libre. Comparte y aprende.

---

Creado por [Paulo Villarroel](https://github.com/paulovillarroel)
