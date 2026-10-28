# Dabar · Hebreo I, Sesión 3

App de estudio para la Sesión 3 de Hebreo I: **estado constructo, pronombres y sufijos pronominales**.

- **Teoría** en cuatro bloques cortos: cadena constructa, pronombres (personales, demostrativos, interrogativos y relativo), sufijos en sustantivos y preposiciones, y un método paso a paso para traducir versículos.
- **Flashcards con repaso espaciado** (Otra vez / Bien / Fácil), cinco mazos y 86 tarjetas, cada una con transliteración (sistema de Page H. Kelley) y análisis de género, número y estado.
- **Práctica por niveles** (1 a 4, como en la pizarra), con la solución explicada en cada respuesta.
- **Simulacro de examen** de 14 preguntas al azar.
- **Progreso** guardado automáticamente en el navegador.

Sin dependencias ni compilación. Archivos:

```
index.html              la app completa
manifest.webmanifest    nombre e ícono para "Agregar a inicio"
icons/                  íconos (iPhone, Android y pestaña del navegador)
```

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `hebreo-sesion3`).
2. Sube `index.html`, `manifest.webmanifest`, `README.md` y la carpeta `icons/` a la rama `main` (botón **Add file → Upload files**; arrastra la carpeta completa).
3. Ve a **Settings → Pages**, en *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
4. En uno o dos minutos la app estará en `https://<tu-usuario>.github.io/hebreo-sesion3/`.

Desde la terminal:

```bash
git init
git add index.html manifest.webmanifest README.md icons
git commit -m "App de estudio: Hebreo I, Sesión 3"
git branch -M main
git remote add origin https://github.com/<tu-usuario>/hebreo-sesion3.git
git push -u origin main
```

## Instalar en el celular

Abre el enlace de GitHub Pages en el celular:

- **iPhone (Safari):** botón Compartir → **Agregar a inicio**.
- **Android (Chrome):** menú ⋮ → **Agregar a la pantalla principal** (o **Instalar app**).

Aparece el ícono "Dabar" y la app se abre a pantalla completa, sin la barra del navegador.

## Editar el contenido

Las tarjetas están en la constante `DECKS` y los ejercicios en `LEVELS`, al inicio del `<script>` de `index.html`. Cada tarjeta tiene:

```js
{ f: "דְּבַר יְהוָה",            // frente en hebreo
  tr: "dᵉḇar YHWH",               // transliteración
  es: "la palabra de Jehová",      // traducción
  an: ["דְּבַר — sust. masc. sg. constructo", "..."], // análisis
  tip: "..." }                     // opcional
```

## Diseño

Sistema visual *Dabar Padilla*: fondo crema, cielo y miel como colores de marca, texto en tinta granate, píldoras inclinadas. Tipografías: Poppins (títulos) y Noto Serif Hebrew (hebreo con niqqud), desde Google Fonts.

La experiencia de usuario toma como referencia un caso de estudio de rediseño de Anki: inicio con anillo de progreso y "último repaso", mazos con contadores de nuevas/aprendiendo/dominadas, botones de repaso con su intervalo visible, guía inicial que explica cada botón y guardado automático visible.
