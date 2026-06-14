# novasanchez-portfolio

Portfolio personal de Rodrigo Sánchez ([@rodrigoscz_](https://x.com/rodrigoscz_)) y casa de la suite open-source **«todo es lenguaje»**.

Vive en el apex `novasanchez.com`. Cada herramienta de la suite tiene su propio subdominio.

## Stack

Astro estático, cero backend. Reusa el sistema visual compartido de la suite (`src/styles/theme.css`): paleta tierra, tipografía mono y tema oscuro fijo para el portfolio.

## Estructura

```
src/
  pages/index.astro   one-pager: hero, sobre mi, la suite, contacto
  styles/theme.css    tokens compartidos de la suite
public/
  nova-mark.svg        marca transparente usada en favicon, hero y footer
  nova-mark-badge.svg  variante con tile oscuro para fondos claros cuando haga falta
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

El portfolio ya tiene copy base en hero, sobre mi, suite y contacto. Próximo paso: revisión visual fina y publicación.

## Suite

- [tres-lenguas](https://github.com/rodrigoscz/tres-lenguas) · un audit web, tres lentes
- [tropicaliza](https://github.com/rodrigoscz/tropicaliza) · linter de locale del español
- [nav-sense](https://github.com/rodrigoscz/nav-sense) · análisis de arquitectura de navegación
- [lang-forge](https://github.com/rodrigoscz/lang-forge) · laboratorio de la suite
- [lang-suite](https://github.com/rodrigoscz/lang-suite) · índice y manifiesto

## Licencia

MIT
