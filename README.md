<!--

author:   Equipo gestor de la plataforma datos.gob.es
email:    contacto@datos.gob.es
version:  0.1.0
language: es
narrator: Spanish Female

comment:  Materiales formativos de Reutilización de la Información del Sector Público. Iniciativa Aporta. datos.gob.es

-->

# Materiales formativos RISP de Iniciativa Aporta

Recursos didácticos abiertos sobre Reutilización de la Información del Sector Público (RISP), adaptados desde contenidos SCORM a materiales interactivos en Markdown con LiaScript. Este repositorio facilita su visualización online, su reutilización y su mantenimiento colaborativo desde GitHub.

[![Abrir en LiaScript](https://img.shields.io/badge/Ver%20online-Abrir%20en%20LiaScript-brightgreen)](https://liascript.github.io/course/?https://raw.githubusercontent.com/datosgobes/materiales-formativos/refs/heads/main/README.md)
[![License: CC-BY 4.0](https://img.shields.io/badge/CC%20BY-4.0-lightgrey?logo=creativecommons)](LICENSE)
[![Hecho con Markdown](https://img.shields.io/badge/Made%20with-Markdown-blueviolet)](https://github.com/datosgobes)

## ¿Qué hay en este repositorio?

- [Unidades didácticas](https://datos.gob.es/es/conocimiento/materiales-formativos-risp-de-iniciativa-aporta) en formato Markdown compatibles con [LiaScript](https://github.com/LiaScript/LiaScript), un dialecto de Markdown para crear cursos interactivos y material educativo, un *open educational resource* (OER/REA, [Recurso Educativo Abierto](https://www.unesco.org/es/open-educational-resources)).
- Interactividad nativa: cuestionarios, bloques ejecutables, incrustación multimedia y narración.
- Estilos, imágenes y recursos compartidos para una experiencia homogénea.

## ¿Cómo usar estos materiales?

### Renderizar documentación LiaScript (navegador)

1. Ábrela en tu navegador `https://liascript.github.io/course/?https://github.com/<usuario>/<repo>/<archivo>.md`:

   https://liascript.github.io/course/?https://github.com/datosgobes/materiales-formativos/blob/main/unidades/06.md

#### Editor
1. Abre el [LiveEditor](https://liascript.github.io/liveeditor/)
2. Modifica el contenido en el editor y clicka en *parse* para ver el resultado.

### LiaScript DevServer (desarrollo local)

Requisitos previos:

- [Node.js](https://nodejs.org/) (recomendado: la versión LTS moderna). Instálalo desde https://nodejs.org/
- [npm](https://www.npmjs.com/) (viene con Node.js)

Instalación del `devserver` globalmente (en una terminal Bash en Windows o WSL):

```sh
npm install -g @liascript/devserver
```

Levantar el servidor desde la carpeta del proyecto (por ejemplo, desde la raíz del repositorio `materiales-formativos`):

```sh
# Clona el repositorio
git clone https://github.com/datosgobes/materiales-formativos.git

# en el directorio del proyecto
liascript-devserver

# o para abrir el navegador automáticamente en la vista del archivo actual
liascript-devserver --open
# usar una carpeta concreta como raíz
liascript-devserver -i unidades -o
# puerto alternativo
liascript-devserver -p 3001 -o
# live reload (recarga automática al guardar)
liascript-devserver --input unidades --live -o
```

>[!TIP]
> Para modificar el CSS en local, puedes modificar en las opciones de configuracion (inicio del Markdown) `link: https://cdn.jsdelivr.net/gh/datosgobes/materiales-formativos@main/assets/css/dge-liascript.css` por una hoja CSS situada en el mismo directorio que el document, ej `./dge-liascript.css`


Salida esperada (ejemplo):

```sh
 _     _       ____            _       _
| |   (_) __ _/ ___|  ___ _ __(_)_ __ | |_
| |   | |/ _` \___ \ / __| '__| | '_ \| __|
| |___| | (_| |___) | (__| |  | | |_) | |_
|_____|_|\__,_|____/ \___|_|  |_| .__/ \__|
                                |_|

✨ watching for changes on: "unidades"
📡 starting server
   - local:           http://localhost:3000
   - on your network: http://192.168.68.102:3000
✨ hit Ctrl-c to close the server
```

## Estructura del repositorio

- `unidades/` — Unidades didácticas principales (LiaScript Markdown).
- `assets/` — Recursos compartidos (imágenes, estilos CSS, fuentes, etc.).
- `ref/` — Documentación de referencia (documentos PDF; SCORM, LiaScript).

## Licencia

Contenido con licencia Creative Commons Attribution 4.0 International (CC BY 4.0). Puedes reutilizar y adaptar siempre citando a: “Ministerio para la Transformación Digital y de la Función Pública a través de la Entidad Pública Empresarial Red.es”. Más información en el archivo [LICENSE](LICENSE).

## Créditos

- Autoría: Equipo gestor de la plataforma datos.gob.es (Iniciativa Aporta)
- Web: [datos.gob.es](https://datos.gob.es)

## Enlaces de interés

- Iniciativa Aporta — Materiales formativos RISP: https://datos.gob.es/es/conocimiento/materiales-formativos-risp-de-iniciativa-aporta
- LiaScript — Documentación y ejemplos: https://liascript.github.io
