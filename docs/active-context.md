# Active context — Búsqueda de pisos

_Última actualización: 2026-06-23_

## Estado

- **Buscador publicado** en GitHub Pages: https://andresefr24.github.io/busqueda-pisos/
- Repo `andresefr24/busqueda-pisos` (rama `main`), ahora **público** (requisito de Pages en cuenta free).
- Datos: **48 propiedades en 8 zonas** capturadas de idealista (tanda 1 = 10 mixtas; tanda 2 = por zonas).
- `index.html` standalone (datos embebidos, mobile-first, filtros + orden). Vault en `docs/`.

## Criterios vigentes

3+ hab · ascensor si planta ≥2 · 200.000–300.000 € · no ocupados / no nuda propiedad / sin inquilinos · metro a <2 km · zona de buen aspecto (seguridad + poder adquisitivo). Detalle en [00-criterios.md](00-criterios.md).

## En curso

- **Búsqueda "todo Madrid con metro, excepto Línea 12"** (L12/MetroSur sur = muy lejos): Alcorcón, Móstoles, Getafe, Leganés, Fuenlabrada quedan **excluidos**.

## Hilos abiertos

- Cuantificar/cualificar la data juntos (pendiente sesión).
- Candidato a **skill `idealista-scan`** (pipeline búsqueda filtrada → extracción DOM → vault/HTML). 3ª repetición; pendiente de luz verde.
- Datos del HTML son estáticos: valorar separar a `data.json` si crece.
- No verificado en ficha: gastos de comunidad, año, estado, exterior/interior real.
