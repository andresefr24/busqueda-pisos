# Gotchas — Búsqueda de pisos (idealista + publicación)

## idealista

- **Slugs de zona:** no adivinarlos. Distritos = `/venta-viviendas/madrid/{distrito}/`; barrios = `/madrid/{distrito}/{barrio}/`. Los slugs de barrio se descubren en el **desplegable del breadcrumb** de una página válida del distrito (devuelve nombre→href). Si el slug es erróneo, idealista sirve una página genérica (título "Viviendas venta…", sin H1 de resultados).
- **Ciudad Pegaso no es zona** en idealista — solo aparece como nombre de calle (Calle Dos / Plaza Mayor de Ciudad Pegaso). La colonia cae en barrio **Arcos** (San Blas-Canillejas).
- **Filtro de situación:** "Disponible, sin ninguna de las restricciones anteriores" añade `sin-inquilinos` a la URL y excluye nuda propiedad / alquilado / ocupado de una vez.
- **Filtros por URL** (slug): `con-precio-desde_200000,precio-hasta_300000,de-tres-dormitorios,de-cuatro-cinco-habitaciones-o-mas,ascensor,sin-inquilinos`.
- **Verificación DataDome** al entrar (~3 s, se pasa sola). Tras navegar, esperar antes de extraer.
- **Metro vs Cercanías:** Valdemoro, Alcalá de Henares, Torrejón, Parla, Navalcarnero NO tienen metro (solo Cercanías/tranvía) → se excluyen por el criterio de metro.
- **Anunciante:** `article.item .logo-branding img[alt]` da el nombre de la agencia; si no hay logo = vendedor **particular**.

## Publicación / GitHub Pages

- **Pages requiere repo público** en cuenta gratuita (privado → solo con plan de pago / Enterprise trial).
- Deploy desde rama `main` / carpeta `/ (root)`. Primer build ~1–2 min antes de servir (404 mientras tanto).
- URL de proyecto: `https://{usuario}.github.io/{repo}/`.
