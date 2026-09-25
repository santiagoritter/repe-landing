# repe-landing

Landing de marketing de [Repe](https://github.com/santiagoritter/GYM-tracker) (la app de entrenamiento). Copia standalone de `site/` del repo principal — mismo contenido, deploy independiente en GitHub Pages para no depender de la configuración de Vercel del otro repo.

- App real: https://santiagoritter.github.io/GYM-tracker/
- Esta landing: https://santiagoritter.github.io/repe-landing/

## Desarrollo

```bash
npm install
npm run dev
```

## Build

```bash
npm run build        # sirve desde la raíz del dominio (para Vercel)
VITE_BASE_PATH=/repe-landing/ npm run build   # para GitHub Pages (este repo)
```

Se publica solo en cada push a `main` (`.github/workflows/deploy.yml`).

## Páginas legales

`privacidad.html` y `terminos.html` se generan desde `src/lib/legalText.ts` en el repo principal (`scripts/gen-legal-site.mts`, `npm run docs:legal-site`) y se copian acá a mano cuando cambian — este repo no tiene acceso al código fuente de la app, así que no se pueden regenerar localmente.
