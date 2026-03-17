# Deploy de producción (sitio estático)

## Incluido en esta preparación
- `robots.txt`
- `sitemap.xml`
- `manifest.webmanifest`
- `404.html`
- `.htaccess` (Apache: compresión, caché, headers de seguridad, HTTPS)
- Meta de `theme-color`, favicon y manifest en páginas principales.

## Checklist antes de publicar
1. Subir todos los archivos al hosting.
2. Verificar que el dominio final sea `https://www.laesquinard.com`.
3. Si cambia el dominio, actualizar `robots.txt` y `sitemap.xml`.
4. Probar rutas:
   - `/`
   - `/menus.html`
   - `/servicios.html`
   - `/galeria.html`
   - `/nosotros.html`
   - `/contacto.html`
   - URL inexistente para validar `404.html`
5. Limpiar caché CDN/hosting tras publicar.

## Nota
`client-original.html` es un archivo histórico de extracción (no operativo) y no debe usarse como página pública.
