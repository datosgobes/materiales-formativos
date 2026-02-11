# Guía y ejemplos de estructura, secciones y componentes reutilizables para cursos en LiaScript

Este documento recopila todos los componentes reutilizables (estructuras, secciones y elementos visuales) utilizados en las unidades formativas, para facilitar la creación de nuevos cursos manteniendo la coherencia visual, estructural y funcional.


<center>

**Ejemplo de unidad formativa**

| Unidad de ejemplo | CURSO.md completo | Ver en LiaScript |
|-------------------|-------------------|------------------|
| Unidad 01 - Conceptos básicos y beneficios | [`CURSO.md`](https://github.com/datosgobes/unidad-formativa-01/blob/main/CURSO.md) | [Abrir](https://liascript.github.io/course/?https://raw.githubusercontent.com/datosgobes/unidad-formativa-01/main/CURSO.md) |

</center>

---

## Índice

### Estructura del curso
- [Encabezado LiaScript (metadatos)](#encabezado-liascript)
- [Título y logos institucionales](#titulo-y-logos)
- [Bloque de inicio (preview y descargas)](#bloque-inicio)
- [Aviso legal](#aviso-legal)
- [Tutorial](#tutorial)
- [Información inicial](#informacion-inicial)
- [Objetivos didácticos](#objetivos-didacticos)
- [Contenidos (índice)](#contenidos)
- [Público objetivo](#publico-objetivo)
- [Conocimientos previos](#conocimientos-previos)
- [Introducción de contenido](#introduccion-contenido)
- [Bloque de contenido con subsecciones](#bloque-contenido)

### Componentes visuales pedagógicos
- [📖 Fuente](#fuente)
- [💡 Ejemplo](#ejemplo)
- [⚠️ Aviso](#aviso)
- [ℹ️ Más información](#mas-informacion)
- [🔍 Saber más](#saber-mas)
- [🧪 Caso de estudio](#caso-de-estudio)
- [✏️ Ejercicio](#ejercicio)
- [📋 Cuestionario final](#cuestionario-final)

---

## Estructura del curso

### <span id="encabezado-liascript">Encabezado LiaScript (metadatos)</span>

Este bloque se coloca al inicio del archivo CURSO.md y contiene todos los metadatos del curso.

> [!IMPORTANT]
> - El bloque de metadatos debe mantenerse al inicio del archivo y no debe contener ningún otro elemento antes que él.
> - Asegúrate de actualizar los campos `module_id`, `title`, `comment`, `long_description`, `repository` y `date` con la información específica de tu unidad formativa.
> - El campo `edit` se puede establecer en `true` para habilitar la edición en línea a través del LiveEditor de LiaScript, o en `false` para deshabilitarlo.

```markdown
<!--
module_id: unidad-formativa-XX
author: Equipo gestor de la plataforma datos.gob.es
email: contacto@datos.gob.es
date: DD/MM/YYYY
version: 1.0.0
language: es
narrator: Spanish Female
mode: Textbook
title: Unidad XX - Título de la unidad
comment: Descripción breve de la unidad formativa.
long_description: Descripción completa de la unidad formativa. Más información en [datos.gob.es](https://datos.gob.es/)

edit: true

repository: https://github.com/datosgobes/unidad-formativa-XX

logo:     https://cdn.jsdelivr.net/gh/datosgobes/materiales-formativos@main/assets/img/logo_dge_square.svg

icon:     https://cdn.jsdelivr.net/gh/datosgobes/materiales-formativos@main/assets/img/logo_dge_normal.svg

dark:   false

script: https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js

link: https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap
      https://cdn.jsdelivr.net/gh/datosgobes/materiales-formativos@main/assets/css/dge-styles.css

font: Montserrat

import: https://raw.githubusercontent.com/liaScript/mermaid_template/master/README.md

import: https://raw.githubusercontent.com/LiaTemplates/Communica/0.0.2/README.md

attribute: Iniciativa de datos abiertos del Gobierno de España [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
-->
```

---

### <span id="titulo-y-logos">Título y logos institucionales</span>

```markdown
# Unidad XX - Título de la unidad

<ul class="logo-list primary-logos">
  <li><a href="https://digital.gob.es/ministerio/organigrama_organos/SEDIA.html"><img alt="Secretaría de Estado de Digitalización e Inteligencia Artificial" src="https://raw.githubusercontent.com/datosgobes/materiales-formativos/refs/heads/main/assets/img/logo_sedia_red-es.jpg"></a></li>
  <li><a href="https://datos.gob.es"><img alt="datos.gob.es" src="https://raw.githubusercontent.com/datosgobes/materiales-formativos/refs/heads/main/assets/img/logo_dge_normal.svg"></a></li>
  <li><a href="https://datos.gob.es/acerca-de-la-iniciativa-aporta"><img alt="Iniciativa Aporta" src="https://raw.githubusercontent.com/datosgobes/materiales-formativos/refs/heads/main/assets/img/logo_iniciativa-aporta.svg"></a></li>
</ul>

[preview-lia](https://raw.githubusercontent.com/datosgobes/unidad-formativa-XX/refs/heads/main/README.md)
```

---

### <span id="bloque-inicio">Bloque de inicio (preview y descargas)</span>

```markdown
<div style="text-align:center; margin: 1.5em 0 1em 0;">
	<div style="display:flex; justify-content:center; gap:1rem; flex-wrap:wrap; margin-bottom:0.75rem;">
		<a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/datosgobes/unidad-formativa-XX/refs/heads/main/CURSO.md#3" class="pdf-download-btn" style="font-size:1.75em; padding:1rem 1.6rem; font-weight:800;">
      ▶️ Empezar curso
    </a>
  </div>
  <div style="display:flex; justify-content:center; gap:1rem; flex-wrap:wrap; margin-bottom:0.5rem;">
    <a href="https://github.com/datosgobes/unidad-formativa-XX/releases/download/latest/documentation-unidad-formativa-XX.pdf" target="_blank" rel="noopener" class="pdf-download-btn" style="font-size:0.95em; padding:0.55rem 0.9rem; background:#6b7280; color:#ffffff;">
      📄 PDF
    </a>
    <a href="https://github.com/datosgobes/unidad-formativa-XX/releases/download/latest/scorm-unidad-formativa-XX.zip" target="_blank" rel="noopener" class="pdf-download-btn" style="font-size:0.95em; padding:0.55rem 0.9rem; background:#6b7280; color:#ffffff;">
      📦 SCORM
    </a>
    <a href="https://github.com/datosgobes/unidad-formativa-XX/releases/download/latest/ims-unidad-formativa-XX.zip" target="_blank" rel="noopener" class="pdf-download-btn" style="font-size:0.95em; padding:0.55rem 0.9rem; background:#6b7280; color:#ffffff;">
      📚 IMS
    </a>
  </div>
  <div style="font-size:0.95em; color:#446DA2;">Empezar el curso o descargar documentación</div>
</div>
```

---

### <span id="aviso-legal">Aviso legal</span>

```markdown
<div style="background:#ebf3ff; border-left:4px solid rgb(var(--color-highlight)); padding:1rem 1rem; border-radius:8px; color:var(--color-highlight);">
  <p style="margin:0.5rem 0 0.25rem 0;text-align:center;">
    Esta unidad ha sido elaborada en el marco de la <a href="https://datos.gob.es/es/que-hacemos" target="_blank" rel="noopener">Iniciativa Aporta (datos.gob.es)</a>, desarrollada por el <a href="https://digital.gob.es/" target="_blank" rel="noopener">Ministerio para la Transformación Digital y de la Función Pública</a> a través de la <a href="https://www.red.es/" target="_blank" rel="noopener">Entidad Pública Empresarial Red.es</a>
  </p>
  <br>
  <div style="text-align:center;">
    <strong style="font-size:1.05em;">📝 Aviso legal</strong>
  </div>
  <p style="margin:0.5rem 0 0.25rem 0;text-align:center;">
    Esta obra está sujeta a una licencia Atribución 4.0 de Creative Commons (CC BY 4.0). Está permitida su reproducción, distribución, comunicación pública y transformación para generar una obra derivada, sin ninguna restricción, siempre que se cite al titular de los derechos (<i>Ministerio para la Transformación Digital y de la Función Pública a través de la Entidad Pública Empresarial Red.es</i>). La licencia completa se puede consultar en: <a href="https://creativecommons.org/licenses/by/4.0" target="_blank" rel="noopener">Attribution 4.0 International</a>
  </p>
</div>

![](media/image_001.jpg)

**DD/MM/YYYY**

![](media/image_002.png)
```

---

### <span id="tutorial">Tutorial</span>

Esta sección introduce al usuario en el uso del curso LiaScript con elementos animados.

```markdown
## TUTORIAL

{{|>}}
*************************************************************************************************************


<div style="background:#fdf8ec; border-left:4px solid rgb(var(--lia-warning)); padding:0; border-radius:8px; overflow:hidden; margin-top:1.5rem; margin-bottom:1.5rem;">
	<div style="background:#fdf2e4; color:rgb(var(--lia-warning)); padding:0.6rem 1rem; font-weight:600; font-size:1.05em;">
		⚠️ Aviso
	</div>
	<div style="padding:0 1rem 0 1rem;">
		<p style="margin:0.25rem 0 0.5rem 0;">
			Este curso está diseñado en <a href="https://liascript.github.io/" target="_blank" rel="noopener">LiaScript</a>. Para disfrutarlo con todas sus funcionalidades, accede a <a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/datosgobes/unidad-formativa-XX/refs/heads/main/CURSO.md" target="_blank" rel="noopener">este enlace</a>.
			</p>
			<p style="margin:0;">
			Para conocer más sobre el formato Markdown utilizado por LiaScript, consulta la <a href="https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md" target="_blank" rel="noopener">documentación oficial</a>.
		</p>
	</div>
</div>

{{1}}
Puedes navegar el curso a través del índice de la parte izquierda o usando las flechas de navegación del teclado o de la parte inferior de la web.

![Navegación del curso](https://raw.githubusercontent.com/datosgobes/materiales-formativos/refs/heads/main/media/tutorial_dge_sections.png)

{{2}}
Al finalizar cada sección, tendrás la oportunidad de responder preguntas para comprobar tu aprendizaje. Estas actividades solo están disponibles en la versión LiaScript, no en Markdown estándar.

<div style="background:#f8fafc; border:2px solid #154481; border-radius:12px; padding:1.5rem; text-align:center; margin:1rem 0;">
  <div style="font-size:2em; margin-bottom:0.5rem;">📋</div>
  <h4 style="margin:0 0 0.5rem 0;">Cuestionario Final</h4>
  <p style="margin:0 0 1rem 0; color:#666;">Evalúa tus conocimientos sobre datos abiertos</p>
  <a href="#cuestionario-final" 
     style="background:#154481; color:white; padding:0.5rem 1.5rem; border-radius:6px; text-decoration:none; font-weight:600; display:inline-block; transition:all 0.3s ease;"
     onmouseover="this.style.background='#0d2d5a'; this.style.transform='scale(1.05)';"
     onmouseout="this.style.background='#154481'; this.style.transform='scale(1)';">
    ▶️ Ir al cuestionario
  </a>
</div>

{{3}}

Recursos disponibles:

- <span class="res res-fuente">📖 <strong>Fuente</strong></span>: origen de la definición o de la información que respalda el concepto o información que se está presentando.
- <span class="res res-ejemplo">💡 <strong>Ejemplo</strong></span>: casos concretos que facilitan la comprensión.
- <span class="res res-aviso">⚠️ <strong>Aviso</strong></span>: consejo o dato práctico para entender lo presentado.
- <span class="res res-mas-info">ℹ️ <strong>Más información</strong></span>: material de relevancia que complementa lo explicado.
- <span class="res res-saber">🔍 <strong>Saber más</strong></span>: referencias y documentos adicionales.
- <span class="res res-caso">🧪 <strong>Caso de estudio</strong></span>: casos reales para afianzar conocimientos.
- <span class="res res-ejercicio">✏️ <strong>Ejercicio</strong></span>: actividades para aplicar los conocimientos adquiridos.

{{4}}
Existe la opción de seleccionar otro idioma para el curso usando la traducción -si existe aparecen listados- o seleccionando el servicio de traducción automática con un solo clic. Ten presente que la traducción automática puede contener errores o interpretaciones incorrectas de algunos conceptos.

![Botón para traducir el contenido](https://raw.githubusercontent.com/datosgobes/materiales-formativos/refs/heads/main/media/tutorial_dge_translate.png)

{{5}}
El curso incluye secciones con narración de audio. Puedes activar o desactivar la narración utilizando el botón situado en la parte superior de cada página.

![Ejemplo de narración de una página](https://raw.githubusercontent.com/datosgobes/materiales-formativos/refs/heads/main/media/tutorial_dge_audio.png)

*************************************************************************************************************>
```

---

### <span id="informacion-inicial">Información inicial</span>

Presenta el título y descripción de la unidad, con video introductorio opcional.

```markdown
## INFORMACIÓN INICIAL

{{|>}}
*************************************************************************************************************

<center>
__Título de la unidad__

[Título descriptivo de la unidad formativa]

__Descripción de la unidad__

[Descripción breve que explique el contenido y alcance de la unidad formativa]
</center>

---

!?[Vídeo descriptivo de la unidad](https://www.youtube.com/watch?v=XXXXX)

*************************************************************************************************************>
```

---

### <span id="objetivos-didacticos">Objetivos didácticos</span>

```markdown
## OBJETIVOS DIDÁCTICOS

{{|>}}
*************************************************************************************************************

Comenzamos presentando los **objetivos didácticos** de esta unidad:

> - [Objetivo 1 con palabras clave en **negrita**]
> - [Objetivo 2 con palabras clave en **negrita**]
> - [Objetivo 3 con palabras clave en **negrita**]
> - [Objetivo 4 con palabras clave en **negrita**]

*************************************************************************************************************>
```

---

### <span id="contenidos">Contenidos (índice)</span>

Índice animado del curso. Los elementos se revelan progresivamente con `{{n}}`.

```markdown
## CONTENIDOS

{{|>}}
*************************************************************************************************************

>{{1}} **[SECCIÓN 1](#seccion-1)**  
>
>{{2}} **[SECCIÓN 2](#seccion-2)** 
>
>{{3}} **[SECCIÓN 3](#seccion-3)**  
>
>{{4}} **[CUESTIONARIO FINAL](#cuestionario-final)**  
>
>{{5}} **[RESUMEN](#resumen)**

*************************************************************************************************************>
```

---

### <span id="publico-objetivo">Público objetivo</span>

```markdown
## PÚBLICO OBJETIVO

{{|>}}
*************************************************************************************************************

Esta unidad formativa está dirigida a:

> - [x] [Descripción del público objetivo al que va dirigida la unidad]

*************************************************************************************************************>
```

---

### <span id="conocimientos-previos">Conocimientos previos</span>

```markdown
## CONOCIMIENTOS PREVIOS NECESARIOS

{{|>}}
*************************************************************************************************************

Para poder asimilar los conceptos que vamos a desarrollar en la unidad:

> - [x] [Conocimientos necesarios o indicar: "No se precisan conocimientos previos"]

*************************************************************************************************************>
```

---

### <span id="introduccion-contenido">Introducción de contenido</span>

Bloque de introducción para una sección principal del curso.

```markdown
<!-- id="identificador-seccion" -->
## TÍTULO DE LA SECCIÓN

{{|>}}
*************************************************************************************************************

[Párrafo introductorio que contextualiza el contenido de la sección]

[Texto descriptivo con **conceptos clave en negrita**]

[Lista con puntos clave si aplica]

*************************************************************************************************************>
```

---

### <span id="bloque-contenido">Bloque de contenido con subsecciones</span>

Para organizar contenido extenso en subsecciones.

```markdown
<!-- id="seccion-principal" -->
## SECCIÓN PRINCIPAL

{{|>}}
*************************************************************************************************************

[Introducción a la sección principal]

*************************************************************************************************************>

### X.1. Subsección: Título

{{|>}}
*************************************************************************************************************

[Contenido de la subsección con definiciones, ejemplos, listas, etc.]

*************************************************************************************************************>

### X.2. Subsección: Título

{{|>}}
*************************************************************************************************************

[Contenido de la subsección]

*************************************************************************************************************>
```

---

## Componentes visuales pedagógicos

---

## <span id="fuente">📖 Fuente</span>

```html
<div style="background:#e6f7f7; border-left:4px solid #17a2b8; padding:0; border-radius:8px; overflow:hidden; margin-top:1.5rem; margin-bottom:1.5rem;">
  <div style="background:#d1f2f4; color:#17a2b8; padding:0.6rem 1rem; font-weight:600; font-size:1.05em;">
    📖 Fuente
  </div>
  <div style="padding:0 1rem 0 1rem;">
    <p style="margin:0.25rem 0 0.5rem 0;">
      Origen de la definición o de la información que respalda el concepto o información que se está presentado.
    </p>
  </div>
</div>
```

---

## <span id="ejemplo">💡 Ejemplo</span>

```html
<div style="background:#ebf8ed; border-left:4px solid #3fb950; padding:0; border-radius:8px; overflow:hidden; margin-top:1.5rem; margin-bottom:1.5rem;">
  <div style="background:#d8f1dc; color:#3fb950; padding:0.6rem 1rem; font-weight:600; font-size:1.05em;">
    💡 Ejemplo
  </div>
  <div style="padding:0 1rem 0 1rem;">
    <p style="margin:0.25rem 0 0.5rem 0;">
      Casos concretos de algunos de los temas o conceptos que permitan una mejor comprensión de lo tratado.
    </p>
  </div>
</div>
```

---

## <span id="aviso">⚠️ Aviso</span>

```html
<div style="background:#fdf8ec; border-left:4px solid #ff9800; padding:0; border-radius:8px; overflow:hidden; margin-top:1.5rem; margin-bottom:1.5rem;">
  <div style="background:#fdf2e4; color:#ff9800; padding:0.6rem 1rem; font-weight:600; font-size:1.05em;">
    ⚠️ Aviso
  </div>
  <div style="padding:0 1rem 0 1rem;">
    <p style="margin:0.25rem 0 0.5rem 0;">
      Es un consejo, truco o dato práctico y útil que ayudará a comprender lo presentado.
    </p>
  </div>
</div>
```

---

## <span id="mas-informacion">ℹ️ Más información</span>

```html
<div style="background:#f3e8ff; border-left:4px solid #7c3aed; padding:0; border-radius:8px; overflow:hidden; margin-top:1.5rem; margin-bottom:1.5rem;">
  <div style="background:#ede9fe; color:#7c3aed; padding:0.6rem 1rem; font-weight:600; font-size:1.05em;">
    ℹ️ Más información
  </div>
  <div style="padding:0 1rem 0 1rem;">
    <p style="margin:0.25rem 0 0.5rem 0;">
      Material de relevancia que complementa lo explicado.
    </p>
  </div>
</div>
```

---

## <span id="saber-mas">🔍 Saber más</span>

```html
<div style="background:#fffbeb; border-left:4px solid #fbbf24; padding:0; border-radius:8px; overflow:hidden; margin-top:1.5rem; margin-bottom:1.5rem;">
  <div style="background:#fef3c7; color:#d97706; padding:0.6rem 1rem; font-weight:600; font-size:1.05em;">
    🔍 Saber más
  </div>
  <div style="padding:0 1rem 0 1rem;">
    <p style="margin:0.25rem 0 0.5rem 0;">
      Información adicional de cada tema con referencias y documentos de consulta con los que poder completar y ampliar tus conocimientos.
    </p>
  </div>
</div>
```

---

## <span id="caso-de-estudio">🧪 Caso de estudio</span>

```html
<div style="background:#fee2e2; border-left:4px solid #dc2626; padding:0; border-radius:8px; overflow:hidden; margin-top:1.5rem; margin-bottom:1.5rem;">
  <div style="background:#fecaca; color:#dc2626; padding:0.6rem 1rem; font-weight:600; font-size:1.05em;">
    🧪 Caso de estudio
  </div>
  <div style="padding:0 1rem 0 1rem;">
    <p style="margin:0.25rem 0 0.5rem 0;">
      Sobre un caso real que nos sirva de modelo, se deberá buscar información y realizar alguna actividad para afianzar los conocimientos adquiridos.
    </p>
  </div>
</div>
```

---

## <span id="ejercicio">✏️ Ejercicio</span>

```html
<div style="background:#ffffff; border:2px solid #154481; border-radius:12px; box-shadow:0 2px 8px rgba(21,68,129,0.15); margin:1.5rem 0; overflow:hidden;">
  <div style="background:linear-gradient(135deg, #072142 0%, #154481 100%); color:#ffffff; padding:1rem 1.5rem; display:flex; align-items:center; gap:0.75rem;">
    <div style="font-size:1.5em;">✏️</div>
    <h4 style="margin:0; font-size:1.3em; font-weight:600;">Ejercicio</h4>
  </div>
  <div style="padding:1.25rem 1.5rem; background:#f8fafc;">
    <p style="margin:0; font-size:1em; color:#333; line-height:1.6;">
      Indica cuáles de las siguientes afirmaciones sobre los beneficios de los datos abiertos son verdaderas y cuáles falsas.
    </p>
  </div>
</div>
```

## <span id="cuestionario-final">📋 Cuestionario final</span>

```html
<div style="background:#ffffff; border:2px solid #154481; border-radius:16px; box-shadow:0 4px 12px rgba(147,51,234,0.2); margin:2rem 0; overflow:hidden;">
  <div style="background:linear-gradient(135deg, #072142 0%, #154481 100%); color:#ffffff; padding:2rem; text-align:center;">
    <div style="font-size:3em; margin-bottom:0.5rem;">📋</div>
    <h3 style="margin:0; font-size:2em; font-weight:700; text-transform:uppercase; letter-spacing:1px;">Cuestionario Final</h3>
    <p style="margin:0.75rem 0 0 0; font-size:1.1em; opacity:0.95;">Evalúa tus conocimientos sobre datos abiertos</p>
  </div>
  <div style="padding:1.5rem 2rem; background:linear-gradient(to bottom, #faf5ff 0%, #ffffff 100%);">
    <p style="margin:0; font-size:1.05em; color:#333; text-align:center;">
      <strong>Instrucciones:</strong> Indica si cada afirmación es <strong>verdadera</strong> o <strong>falsa</strong>
    </p>
  </div>
</div>
```

---

## Notas de uso

- Todos los componentes usan los estilos en línea de [datosgobes/materiales-formativos](https://github.com/datosgobes/materiales-formativos/blob/main/assets/css/dge-styles.css) para máxima compatibilidad y portabilidad.
- Se recomienda mantener los márgenes para evitar solapamientos visuales.
- Puedes copiar y pegar estos bloques en cualquier parte de tus materiales formativos.
- Personaliza el contenido interno según el contexto de tu curso.


---
