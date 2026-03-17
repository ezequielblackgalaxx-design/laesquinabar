---
name: web-rebuilder
description: "Usa esta skill cuando el usuario quiera reconstruir la web de un cliente a partir de su HTML original (por ejemplo: 'usa la skill web-rebuilder', 'reconstruye la web del cliente', 'construye la web a partir del HTML original')."
---

# Web Rebuilder

## Objetivo
Reconstruir la web de un cliente con diseño profesional y moderno, conservando el 100% del contenido real extraído del archivo `client-original.html`.

Reglas clave:
- Nunca inventar información.
- Nunca usar placeholders de texto.
- Si un dato no está claro, marcarlo en el HTML como `<!-- REVISAR -->`.

## Paso 1 - Leer y extraer contenido real
Leer `client-original.html` completo y extraer:
- Nombre de la empresa (exacto)
- Teléfono(s)
- Email(s)
- Dirección física (si existe)
- Servicios (lista exacta)
- Zonas/localidades de trabajo
- Años de experiencia (si aparece)
- Datos de confianza (si aparecen)
- Testimonios (si existen)
- Precios (si existen)
- Colores principales de marca (en hex si es posible)
- Tipografías relevantes
- Slogan o frase principal

## Paso 2 - Estructura de páginas
Generar siempre estas 4 páginas:
1. `index.html` - Página principal
2. `servicios.html` - Servicios detallados
3. `nosotros.html` - Historia, equipo, valores, confianza
4. `contacto.html` - Formulario, mapa, teléfono, email, dirección

## Paso 3 - Diseño y estructura de `index.html`

### Hero section
- Fondo oscuro semitransparente sobre vídeo
- Vídeo: `assets/hero.mp4` con `playsinline muted loop preload="auto"`
- Fallback: `assets/hero-poster.jpg`
- Incluir comentario exacto: `<!-- SCROLL-VIDEO-SECTION -->`
- Título principal: nombre de la empresa
- Subtítulo: slogan o frase principal
- CTA principal: "Solicitar presupuesto" → `contacto.html`
- CTA secundario: teléfono directo (`tel:`)

### Secciones obligatorias en `index.html`
1. Hero con vídeo
2. Por qué elegirnos (3-4 puntos reales)
3. Servicios principales (máximo 6)
4. Números de confianza (solo datos reales)
5. Testimonios (si existen)
6. CTA final (teléfono + botón de presupuesto)
7. Footer (logo, navegación, teléfono, email, copyright)

## Paso 4 - Reglas de diseño

### Debes usar
- CSS propio dentro de `<style>` en cada HTML (sin framework externo)
- Google Fonts por CDN (tipografía moderna)
- Variables CSS de marca (`--color-primary`, `--color-dark`, etc.)
- Responsive mobile-first
- Animaciones suaves con `transition` y `transform`
- Layout con Grid/Flexbox

### No debes usar
- Bootstrap, Tailwind CDN ni otros frameworks CSS
- Imágenes de stock o placeholders
- Contenido inventado
- Efectos de scroll custom en hero (se integran luego)

### Estilo visual
- Limpio y profesional
- Espacio en blanco amplio
- Secciones con padding generoso (mín. 80px vertical)
- Tarjetas con sombras suaves
- Botones redondeados con hover suave
- Color primario en CTAs, títulos y acentos
- Overlay del hero: negro al 60%

## Paso 5 - Assets
- Logo: `assets/logo.png` (header + footer)
- Vídeo hero: `assets/hero.mp4`
- Poster hero: `assets/hero-poster.jpg`
- Imágenes adicionales: usar URLs reales del sitio original

## Paso 6 - Navegación compartida
Todas las páginas deben incluir el mismo header/footer con:
- Logo enlazando a `index.html`
- Menú: Inicio | Servicios | Nosotros | Contacto
- Teléfono visible y clickeable en móvil
- Header sticky

## Paso 7 - Entrega final al usuario
Al terminar, confirmar:
- Los 4 HTML generados
- Qué contenido real fue extraído y usado
- Qué datos quedaron marcados con `<!-- REVISAR -->`
- Cómo previsualizar: "clic derecho en `index.html` → Open with Live Server"