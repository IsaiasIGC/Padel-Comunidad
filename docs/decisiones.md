# Documento de decisiones de diseño

> Cada decisión: **qué** elegiste, **por qué**, y **qué alternativa descartaste**.
> Se evalúa la justificación, no la longitud. Máximo 2 páginas en la Fase 1.

## Ruta de trabajo

- [ ] Ruta A · Figma (enlace con permiso de lectura: …)
- [x] Ruta B · VS Code (diseño directamente en `guia.html`)

## 1. Color (RA1 · CE b)

- Tono de acento de la ficha y cómo has obtenido la escala (50 … 950):
  - Tono de 172°, establecido por la ficha del Caso 10. La escala se ha generado mediante OKLCH, manteniendo un croma de 0,12 y variando la luminosidad para obtener seis niveles (50, 300, 400, 700, 800 y 950). Los colores se han convertido a hexadecimal para incorporarlos a los tokens Sass.

- Por qué el acento de texto/fondo es el 700 en claro y el 400 en oscuro (o el que elijas):
  - Se utilizan los niveles 700 en tema claro y 400 en tema oscuro como color de acento principal. Ambos superan el mínimo WCAG de 4,5:1 sobre sus respectivas superficies.

- Tokens semánticos añadidos y para qué:
  - `error` y `error-tenue` para representar errores de validación y sus fondos asociados. Se ha creado una familia de cuatro colores mediante OKLCH.

- Pares de contraste añadidos a `$pares-contraste`:
  - `error` sobre `error-tenue` y `error` sobre `superficie`, ambos con un mínimo de 4,5:1.

## 2. Tipografía (RA1 · CE b)

- Familia elegida y por qué (rendimiento, legibilidad, licencia):
  - Se ha elegido `system-ui` como fuente principal porque utiliza la tipografía nativa del sistema operativo, ofrece buena legibilidad y no necesita descargar archivos externos ni gestionar licencias de fuentes web.
- Base y razón en móvil y escritorio. Por qué esas:
  - En móvil se utiliza una base de 16 px con una razón modular de 1,2, mientras que en escritorio se utiliza una base de 18 px con una razón de 1,25. Se ha elegido una escala más moderada en pantallas pequeñas y algo mayor en escritorio para mantener una jerarquía visual equilibrada.
- Medida de línea (`max-inline-size` del párrafo en `ch`):
  - Se establece un máximo de 65ch para limitar la longitud de los párrafos y facilitar su lectura.

## 3. Espaciado y forma

- Escala de espaciado y radios. Si cambias algo respecto a la plantilla, por qué:

## 4. Componentes (RA1 · CE f)

| Componente | Estados | Cómo se resuelve cada estado en CSS |
| --- | --- | --- |
| Botón | normal, hover, foco, desactivado, secundario | |
| Turno | disponible, seleccionado, ocupado, foco | |
| Contador de invitados | | |
| Aviso de pago | | |

## 5. Comparativa de tecnologías (RA1 · CE e · RA2 · CE i)

| Criterio | Figma | Penpot | Diseño en código |
| --- | --- | --- | --- |
| Coste / licencia | | | |
| Traslado a código (handoff) | | | |
| Mantenimiento del sistema | | | |

| Criterio | Sass + CSS propio | CSS nativo sin preprocesador | Bootstrap / Tailwind |
| --- | --- | --- | --- |
| Tokens y temas | | | |
| Peso del CSS final | | | |
| Control de la cascada | | | |

**Decisión y motivo:**
