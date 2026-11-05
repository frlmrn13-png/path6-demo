# Path 6 · Demo

Demo navegable de **Path 6**, la app que conecta a autores que empiezan con lectores beta, correctores e ilustradores de portada en formación, a **precios reducidos y justificados**.

👉 **Pruébala:** https://frlmrn13-png.github.io/path6-demo/

Es una sola página (`index.html`), sin servidor ni base de datos. Todo es inventado: no se cobra nada, no se sube ningún archivo y no se guarda ningún dato (salvo el tipo de usuario elegido, en tu propio navegador).

## Qué se puede probar

Al entrar eliges cómo ver la app. Desde el perfil puedes cambiarlo cuando quieras.

- **Autor/a (Ana):** el camino de su libro en 6 etapas, contratar con pago protegido, aprobar entregas, pedir pruebas gratis de un capítulo a varios profesionales y compararlas antes de pagar.
- **Lector/a beta (Lucía), corrector/a (Pablo) o ilustrador/a de portada (Irene):** su tramo dentro del camino del libro de Ana y un encargo simulado de principio a fin (Ana escribe, aceptas, entregas un PDF y cobras o te eligen). También su precio recomendado.

Además:

- **Niveles y precio justo:** cada perfil indica nivel (junior, intermedio o senior), formación y motivo. Path 6 recomienda un precio según el nivel y explica por qué.
- **Visor de documentos:** correcciones con control de cambios y comentarios, informes de lectura beta y bocetos.
- **Servicios de lanzamiento:** lectura beta, corrección e ilustración de portada. La promoción (redes, boletín de Path 6 a lectores y destacados) aparece como "Próximamente".
- **Compartir con amigos** y **"Quiero probarla"**, que abre el formulario de opinión sobre la demo.

## Sistema de diseño

Toda la interfaz sale de una sola hoja de estilos con tokens, al principio de `index.html`. Los componentes no usan colores sueltos, solo `var(--…)`. Hay una página de referencia en la propia demo: **Perfil → Sistema de diseño** (`#/sistema`).

| Grupo | Tokens |
|---|---|
| Marca (paleta Atardecer vivo, igual en claro y oscuro) | `--coral` `--apricot` `--green` `--pink` `--lilac` `--mint` `--star`, y `--on-color` para el texto sobre ellos |
| Superficies y texto (cambian en modo oscuro, gris grafito) | `--bg` `--surface` `--surface-2` `--line` `--text` `--muted` `--ink` `--on-ink` `--accent` |
| Estados | `--ok` `--warn` `--danger` |
| Forma | `--r-xs` 4 · `--r-sm` 8 · `--r-md` 12 · `--r-lg` 16 · `--r-xl` 22 · `--r-pill` |
| Sombras | `--sh-1` tarjetas · `--sh-2` elementos flotantes · `--sh-3` diálogos |
| Tipografía | `--font-ui` Plus Jakarta Sans · `--font-read` Literata · tamaños `--fs-xs` 11 a `--fs-xxl` 30 |
| Espacio | `--sp-1` 4 · `--sp-2` 8 · `--sp-3` 12 · `--sp-4` 16 · `--sp-5` 24 |
| Papel del visor (siempre claro) | `--paper` `--paper-ink` `--paper-muted` `--paper-line` |

Reglas: tarjetas en `xl`, campos en `md`, etiquetas en `sm`, botones y filtros en pastilla. Un solo bloque destacado (coral) por pantalla. Las etiquetas de rol, nivel y género son pastillas pastel con texto en tinta.

## Verla en local

```bash
npx --yes serve@14.2.4 . -l 3100
```

Después abre http://localhost:3100.
