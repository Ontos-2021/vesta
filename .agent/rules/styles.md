---
trigger: always_on
---


# Guía de Diseño – VESTA · La Llama Eterna

Documento de referencia para diseño de la tienda Vesta (e-commerce basado en Django templates).  
Objetivo: mantener una identidad visual consistente en todo el sitio, independientemente del framework CSS (Tailwind, Bootstrap, CSS plano).

---

## 1. Identidad de marca

**Personalidad:** cálida, etérea, mística, elegante y confiable.  
**Concepto:** “La llama eterna” → fuego suave + cosmos.  

Pilares visuales:
- Degradados suaves violeta–azul–durazno.
- Tipografías con mezcla de serif elegante + sans moderna.
- Mucho espacio en blanco, UI limpia, sin ruido visual.

---

## 2. Sistema de color

Todos los colores deben definirse como tokens (variables) y no usarse hex sueltos en el CSS.

### 2.1. Paleta principal

| Token            | Nombre          | Uso principal                                     | Hex      |
|-----------------|-----------------|---------------------------------------------------|----------|
| `primary`       | Vesta Purple    | Botones primarios, links, acentos fuertes         | `#6A40FF` |
| `primary-soft`  | Vesta Lilac     | Fondos suaves, hovers, badges                     | `#D7C4FF` |
| `secondary`     | Vesta Blue      | Elementos secundarios, tags, iconos               | `#2F7BFF` |
| `brand-light`   | Vesta Glow      | Fondo base cálido (body, secciones claras)        | `#FFF5EF` |
| `brand-pink`    | Vesta Blush     | Acentos cálidos, badges, chips                    | `#F4B7C5` |
| `brand-peach`   | Vesta Peach     | Bloques destacados, fondos suaves de secciones    | `#F7D3B8` |

### 2.2. Neutros

| Token         | Uso                                   | Hex      |
|---------------|----------------------------------------|----------|
| `neutral-900` | Texto principal, títulos oscuros       | `#1F1630` |
| `neutral-700` | Texto secundario                      | `#4D435F` |
| `neutral-500` | Placeholders, labels, meta información| `#8D869E` |
| `neutral-200` | Bordes, divisores                     | `#E4DFEC` |
| `neutral-50`  | Fondo de tarjetas, bloques sobre blanco | `#FAF7FF` |
| `white`       | Fondo blanco                          | `#FFFFFF` |

### 2.3. Estados (e-commerce)

| Token      | Uso                         | Hex      |
|------------|-----------------------------|----------|
| `success`  | Confirmaciones, “En stock”  | `#1EC98A` |
| `warning`  | Avisos, “Pocas unidades”    | `#FFB347` |
| `danger`   | Errores, “Sin stock”        | `#FF4F6D` |

### 2.4. Degradado “Aura Vesta”

Usar **solo** en hero, banners especiales y secciones de storytelling.

```css
/* Versión principal */
background: linear-gradient(90deg, #2F7BFF 0%, #F4B7C5 50%, #6A40FF 100%);

/* Versión más suave */
background: linear-gradient(90deg, #2F7BFF 0%, #F7D3B8 50%, #6A40FF 100%);
````

---

## 3. Tipografía

### 3.1. Jerarquía tipográfica

* **Display / Marca (Títulos, claims):**

  * `Playfair Display` o `Cormorant Garamond`
  * Uso: H1, H2, subtítulos importantes.
* **Texto UI / Cuerpo:**

  * `Inter`, `Nunito` o `Work Sans`
  * Uso: menús, botones, descripciones de producto, formularios.

### 3.2. Escalas sugeridas

Desktop (puede escalar en mobile):

* `H1` (hero): 42–48 px, `font-display`, `font-weight: 700`.
* `H2`: 30–34 px, `font-display`, `font-weight: 600`.
* `H3`: 22–26 px, `font-display` o `font-body` bold.
* `Body`: 16 px, `font-body`, `line-height: 1.6`.
* `Small / Meta`: 14 px, `font-body`, `line-height: 1.4`.

Evitar usar más de 3 tamaños distintos por bloque para mantener la limpieza visual.

---

## 4. Layout & espaciado

### 4.1. Fondo general

* Fondo base del sitio: `brand-light` (`#FFF5EF`) o blanco (`#FFFFFF`) con secciones sobre `neutral-50`.
* El degradado no debe usarse como fondo de toda la web, solo en bloques específicos.

### 4.2. Grid

* Contenedor principal: ancho máximo 1200–1280 px, centrado.
* Margen lateral: 16 px en mobile, 24–32 px en desktop.
* Sistema de columnas:

  * Desktop: 3–4 columnas para grilla de productos.
  * Tablet: 2–3 columnas.
  * Mobile: 1–2 columnas.

### 4.3. Espaciado

* Separación entre secciones verticales: 64–80 px desktop, 40–48 px mobile.
* Padding interno de cards y bloques: 16–24 px.
* No saturar: priorizar aire y legibilidad.

---

## 5. Componentes clave

### 5.1. Navbar

* Fondo: `white` con sombra suave (`box-shadow` muy ligero).
* Logo: versión en crema / claro sobre fondo transparente.
* Links:

  * Color base: `neutral-700`.
  * Hover: `primary` + subrayado fino o cambio de peso.
* CTA (“Ingresar”, “Carrito”):

  * Botón primary o outline.

### 5.2. Botones

**Primary button**

* Fondo: `primary`.
* Texto: `white`.
* Radio: 8–999 px (decidir un estilo y respetarlo).
* Hover: `primary` más oscuro o sombra suave.
* Disabled: opacidad 0.5, sin sombra.

**Secondary button**

* Fondo: `white`.
* Borde: `primary`.
* Texto: `primary`.
* Hover: fondo `primary-soft`.

**Ghost / text button**

* Fondo transparente.
* Texto `primary`.
* Uso: acciones secundarias (“Ver más”, “Editar dirección”).

### 5.3. Cards de producto

* Fondo: `white`.
* Borde: `neutral-200`.
* Radio: 12–16 px.
* Sombra: sutil, aumenta en `hover`.
* Estructura:

  * Imagen (60–70% superior).
  * Debajo:

    * Nombre: `neutral-900`.
    * Categoría: `neutral-500`, tamaño small.
    * Precio: `primary`, peso semibold.
    * Badges:

      * Descuento: fondo `brand-pink` o `danger` con texto blanco.
      * Stock: texto small `success` / `danger`.

### 5.4. Checkout y formularios

* Fondos lisos (blanco / `brand-light`), sin degradados.
* Inputs:

  * Fondo: `white`.
  * Borde: `neutral-200`.
  * Radio: 8 px.
  * Focus: borde `primary` + halo suave.
* Mensajes:

  * Éxito: texto `success`.
  * Error: texto `danger`, mensaje corto y claro.

---

## 6. Uso de imágenes, iconos e ilustraciones

* Estilo fotográfico:

  * Iluminación suave, tonos cálidos/rosados.
  * Nada de contraste extremo; mantener la estética etérea.
* Iconografía:

  * Líneas simples, stroke fino, preferiblemente outline.
  * Color base: `neutral-700`; acentos en `primary` o `secondary`.
* Ilustraciones:

  * Opcionales; si se usan, mantener paleta de la marca y evitar estilos demasiado caricaturescos.

---

## 7. Responsividad

* Mobile-first: diseñar primero en mobile, escalar hacia tablet/desktop.
* Quebrar layout de 3–4 columnas a 1–2 en mobile.
* Menú:

  * Desktop: navbar horizontal.
  * Mobile: menú tipo drawer o dropdown desde botón “hamburguesa”.

---

## 8. Accesibilidad básica

* Contraste mínimo recomendado:

  * Texto vs fondo ≥ 4.5:1 para texto normal.
* Tamaños mínimos:

  * Texto body ≥ 14 px (ideal 16 px).
  * Área clicable de botones y links ≥ 40 × 40 px.
* No depender solo del color para estados (ej. error + ícono o texto).

---

## 9. Implementación en Tailwind (ejemplo)

```js
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: '#6A40FF',
        'primary-soft': '#D7C4FF',
        secondary: '#2F7BFF',
        'brand-light': '#FFF5EF',
        'brand-pink': '#F4B7C5',
        'brand-peach': '#F7D3B8',
        'neutral-900': '#1F1630',
        'neutral-700': '#4D435F',
        'neutral-500': '#8D869E',
        'neutral-200': '#E4DFEC',
        'neutral-50': '#FAF7FF',
        success: '#1EC98A',
        warning: '#FFB347',
        danger: '#FF4F6D',
      },
      fontFamily: {
        display: ['"Playfair Display"', 'serif'],
        body: ['Inter', 'system-ui', 'sans-serif'],
      },
    },
  },
};
```

Uso recomendado:

* Títulos: `class="font-display text-neutral-900"`.
* Texto: `class="font-body text-neutral-700"`.
* Botón primario: `class="font-body bg-primary text-white rounded-lg px-4 py-2 hover:bg-primary/90"`.

---

## 10. Implementación en Bootstrap (SCSS)

```scss
// _vesta-theme.scss
$primary:   #6A40FF;
$secondary: #2F7BFF;
$success:   #1EC98A;
$danger:    #FF4F6D;
$warning:   #FFB347;

$body-bg:    #FFF5EF;
$body-color: #1F1630;

$font-family-sans-serif: 'Inter', system-ui, -apple-system, sans-serif;
$headings-font-family:   'Playfair Display', serif;
```

Compilar este SCSS antes de importar Bootstrap o usando el mecanismo de theming del proyecto.

---

## 11. Do & Don’t

**Do**

* Usar el degradado solo en secciones hero / especiales.
* Mantener mucho espacio en blanco.
* Limitar la cantidad de colores en cada vista (máx. 3–4 simultáneos).

**Don’t**

* Usar fondos muy oscuros o saturados para secciones completas.
* Llenar la UI de sombras fuertes o bordes gruesos.
* Mezclar tipografías adicionales fuera de las definidas.

---

```
