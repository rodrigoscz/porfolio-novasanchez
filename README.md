# novasanchez-portfolio

Portfolio personal de Rodrigo Sánchez ([@rodrigoscz_](https://x.com/rodrigoscz_)) y casa de la suite open-source **«todo es lenguaje»**.

Vive en el apex `novasanchez.com`. Cada herramienta de la suite tiene su propio subdominio.

## Stack

Astro estático, cero backend. Sistema visual en `src/styles/theme.css`: paleta tierra y tema oscuro fijo.

Tipografía (Fontshare, variables, auto-hospedadas en `public/fonts/`):

- **Rajdhani** 700: títulos (`h1`, `h2`, `h3`) y botones
- **Sentient**: cuerpo de texto
- Monoespaciada del sistema: chips de stack y el rol del hero

## Estructura

```
src/
  pages/index.astro   one-pager: hero, sobre mí, la suite, contacto
  styles/theme.css    tokens compartidos de la suite
public/
  nova-mark.svg        marca transparente usada en favicon, hero y footer
  nova-mark-badge.svg  variante con tile oscuro para fondos claros cuando haga falta
  fonts/               Rajdhani y Sentient en woff2 variable (un archivo por familia)
  og.png               tarjeta social 1200x630 (regenerar si cambia el copy del hero)
  robots.txt           apunta al sitemap
  sitemap.xml          estático: una sola URL, actualizar si se agregan páginas
```

## Desarrollo

```bash
pnpm install
pnpm dev      # servidor local
pnpm build    # build estático a dist/
pnpm preview  # previsualizar el build
```

## Deploy

Cloudflare Pages, dominio custom `novasanchez.com`. Build estático puro, sin base path.

## Estado

Copy base completo en hero, sobre mí, suite y contacto, con ortografía corregida. Resueltos: `h1` semántico, Open Graph + Twitter Card, canonical, JSON-LD `Person`, `robots.txt` y `sitemap.xml`.

Accesibilidad y pulido resueltos: skip link, anillo de foco `:focus-visible` unificado, `scroll-margin-top` en las secciones, contraste WCAG AA en toda la paleta, tipografía sin justificado y limpieza de CSS muerto.

### Contraste (verificado)

| Par | Ratio | AA (4.5) |
| --- | --- | --- |
| `--terra` sobre `--paper` | 5.85:1 | ✅ |
| `--terra` sobre `--arena` | 6.40:1 | ✅ |
| `--brown` sobre `--arena` | 8.50:1 | ✅ |
| `--ink` sobre `--arena` | 12.33:1 | ✅ |

Pendiente antes de publicar:

- Definir si entra una sección de trabajos o casos.
- Verificar que los subdominios de la suite estén activos: las cards enlazan a `*.novasanchez.com`.
- El repositorio todavía no está bajo git.
- Deploy a Cloudflare Pages con dominio custom `novasanchez.com`.

## Suite

- [tres-lenguas](https://github.com/rodrigoscz/tres-lenguas) · un audit web, tres lentes
- [tropicaliza](https://github.com/rodrigoscz/tropicaliza) · linter de locale del español
- [nav-sense](https://github.com/rodrigoscz/nav-sense) · análisis de arquitectura de navegación
- [lang-forge](https://github.com/rodrigoscz/lang-forge) · laboratorio de la suite
- [lang-suite](https://github.com/rodrigoscz/lang-suite) · índice y manifiesto

## Licencia

MIT
