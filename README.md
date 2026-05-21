# CV Online — Nicolás Labbé

CV estático en HTML/CSS optimizado para GitHub Pages, ATS y exportación a PDF en tamaño A4.

## Estructura del proyecto

- `index.html`: contenido semántico del CV.
- `styles.css`: estilos responsive y reglas de impresión.
- `README.md`: guía de uso y despliegue.

## Cómo correr localmente

Opciones rápidas:

1. Abrir `index.html` directamente en el navegador.
2. Levantar un servidor local simple (recomendado):

```bash
python3 -m http.server 8080
```

Luego abre: `http://localhost:8080`.

## Cómo subir a GitHub Pages

1. Sube estos archivos al repositorio (rama `main` o la que uses para Pages).
2. En GitHub: **Settings → Pages**.
3. En **Build and deployment**:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` (root)
4. Guarda y espera el despliegue.
5. Tu CV quedará disponible en una URL tipo:
   - `https://TU-USUARIO.github.io/TU-REPO/`

## Imprimir o guardar como PDF

- Usa el botón **“Imprimir / Guardar como PDF”** en la parte superior del CV.
- O usa `Ctrl + P` / `Cmd + P`.
- En el diálogo de impresión:
  - Tamaño: **A4**
  - Márgenes: por defecto del navegador (el CSS ya define `@page`)
  - Activar/desactivar “Gráficos de fondo” es opcional (el diseño de impresión no depende de fondos)

## Decisiones de diseño (ATS, responsive, impresión)

### Optimización ATS

- HTML semántico con `header`, `nav`, `main`, `section`, `article`, `h1`, `h2`, `h3`.
- Texto real (sin imágenes para contenido de experiencia o habilidades).
- Fechas, cargos y empresas explícitos y fáciles de parsear.
- Skills y tecnologías en texto plano.
- Sin tablas para layout principal ni componentes visuales que reemplacen texto.

### Diseño responsive

- Diseño principal tipo CV ejecutivo con lectura lineal.
- Tipografía del sistema para máxima compatibilidad y rendimiento.
- Layout adaptable para desktop/tablet/mobile con media queries.
- Jerarquía visual clara, espaciado generoso y contraste alto.

### Impresión / PDF (A4)

- Reglas específicas en `@media print` para salida profesional.
- Botón interactivo oculto en impresión.
- Colores ajustados a texto oscuro y fondo blanco.
- `@page` configurado para tamaño A4 y márgenes controlados.
- Prevención de cortes incómodos con `break-inside: avoid` en bloques críticos.
- URLs de LinkedIn/GitHub visibles en versión impresa.

## Personalización rápida

- Edita datos personales y contenido en `index.html`.
- Ajusta paleta/espaciado/tipografía en `styles.css`.
- Si publicas en un dominio distinto, actualiza `og:url` en el `<head>` de `index.html`.
