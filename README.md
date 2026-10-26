# ZAEL CMG — Sitio web oficial del artista

**Experiencia web musical desarrollada con Vue 3**, enfocada en presentar la identidad visual de ZAEL CMG, sus lanzamientos y los canales donde escuchar su música.

[**Ver sitio web**](https://zael-cmg.netlify.app/) · [**Explorar diseño en Figma**](https://www.figma.com/design/05aEwoLv3G2gRyxQO0nSNI/WEB-PAGES?node-id=0-1) · [**Código fuente**](https://github.com/xorzzz/zael-cmg)

## Descripción

ZAEL CMG es una landing page de presentación artística que combina contenido musical, composición visual y elementos interactivos. El proyecto parte de un diseño en Figma y organiza la experiencia en secciones reutilizables, con especial atención a su presentación en pantallas móviles y de escritorio.

La aplicación permite descubrir lanzamientos, reproducir fragmentos de audio desde la página, acceder a plataformas externas y contactar al artista. Se trata de un **proyecto frontend**; los archivos multimedia y el envío del formulario utilizan servicios externos.

## Funcionalidades

- **Presentación visual del artista:** portada con elementos gráficos, capas e identidad de marca.
- **Lanzamientos musicales:** listado de canciones con carátula, título, artistas y controles de reproducción.
- **Reproductor integrado:** componente flotante de audio HTML5 con controles de reproducción/pausa, indicador de progreso y enlaces a plataformas musicales.
- **Álbumes y contenido destacado:** sección visual con carátulas e información de los lanzamientos.
- **Plataformas digitales:** acceso a Spotify, YouTube y redes sociales.
- **Contenido multimedia:** integración de imágenes alojadas externamente y video incrustado de YouTube.
- **Contacto:** formulario enviado mediante Formspree y enlace directo a WhatsApp.
- **Diseño adaptable:** estilos para dispositivos móviles y pantallas de escritorio mediante Sass y media queries.

## Tecnologías

| Tecnología | Uso en el proyecto |
| --- | --- |
| **Vue 3** | Interfaz y componentes de la aplicación. |
| **JavaScript** | Interactividad y lógica del reproductor. |
| **Pinia** | Estado compartido de la reproducción musical. |
| **Vue Router** | Configuración de las rutas de la aplicación. |
| **Sass (SCSS)** | Estilos y adaptación responsive. |
| **Vite** | Servidor de desarrollo y compilación de producción. |
| **Firebase Storage** | Alojamiento externo de imágenes y archivos de audio utilizados por el sitio. |
| **Formspree** | Recepción de los mensajes del formulario de contacto. |
| **Netlify** | Alojamiento de la versión publicada. |
| **Figma** | Diseño y referencia visual para la implementación. |

## Organización del código

```text
src/
├── assets/                # Recursos y estilos
├── components/
│   ├── AudioPlayer.vue     # Reproductor de audio flotante
│   ├── BackgroundVideo.vue # Video integrado
│   └── view/               # Secciones de la landing page
│       ├── LandView.vue
│       ├── ReleasesView.vue
│       ├── AlbumsView.vue
│       ├── ChannelsView.vue
│       ├── AboutView.vue
│       └── ContactView.vue
├── router/                 # Rutas con Vue Router
├── store/                  # Estado global con Pinia
│   ├── musicStore.js
│   └── imagesStore.js
├── views/                  # Vistas de la aplicación
├── data.js                 # Datos de canciones y álbumes
├── App.vue
└── main.js
```

La lógica relacionada con la reproducción se concentra en `src/store/musicStore.js` y se utiliza desde los componentes de lanzamientos y el reproductor flotante. El catálogo musical se configura en `src/data.js`.

## Ejecución local

**Requisito:** Node.js y npm instalados.

1. Clona el repositorio:

   ```bash
   git clone https://github.com/xorzzz/zael-cmg.git
   cd zael-cmg
   ```

2. Instala las dependencias:

   ```bash
   npm ci
   ```

3. Inicia el servidor de desarrollo:

   ```bash
   npm run dev
   ```

   Abre en el navegador la dirección local que muestre Vite.

4. Para compilar y probar la versión de producción:

   ```bash
   npm run build
   npm run preview
   ```

## Decisiones de implementación

- **Arquitectura basada en componentes:** separación de las secciones visuales para facilitar mantenimiento y reutilización.
- **Estado compartido con Pinia:** coordinación de la información y las acciones del reproductor entre distintos componentes.
- **Diseño a implementación:** traducción de las composiciones para escritorio y móvil de Figma a plantillas Vue y estilos SCSS.
- **Servicios externos:** uso de Firebase Storage para recursos multimedia y Formspree para el formulario, sin desarrollar un servidor backend para este sitio.

## Diseño y despliegue

El diseño de referencia incluye propuestas para **escritorio y móvil** y está disponible en [Figma](https://www.figma.com/design/05aEwoLv3G2gRyxQO0nSNI/WEB-PAGES?node-id=0-1).

La versión publicada puede consultarse en **[zael-cmg.netlify.app](https://zael-cmg.netlify.app/)**.
