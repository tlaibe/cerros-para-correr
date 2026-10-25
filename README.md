# Cerros para Correr

App web para planificar salidas de trail running en los cerros de Santiago y registrar tiempos de subida y bajada.

## Qué hay en esta carpeta

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa: diseño, rutas y lógica |
| `manifest.webmanifest` | Le dice al iPhone el nombre, ícono y colores de la app instalada |
| `sw.js` | Guarda la app en caché para que abra sin conexión |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | Íconos de la app |

## Publicar en GitHub Pages (una sola vez)

Conviene hacerlo desde un computador.

1. Crea una cuenta en [github.com](https://github.com) si no tienes una.
2. Arriba a la derecha toca **+ → New repository**.
   - Nombre: `cerros-para-correr`
   - Marca **Public**. GitHub Pages gratis requiere repositorio público.
   - Toca **Create repository**.
3. En el repositorio nuevo toca **uploading an existing file**. Arrastra todos los archivos de esta carpeta, sin la carpeta, y toca **Commit changes**.
4. Ve a **Settings → Pages**. En *Branch* elige `main` y carpeta `/ (root)`, y toca **Save**.
5. Espera uno o dos minutos y recarga la página de Settings. Arriba aparecerá tu link:
   `https://TU-USUARIO.github.io/cerros-para-correr/`

## Instalarla en el iPhone

1. Abre tu link en **Safari**.
2. Toca **Compartir → Agregar a pantalla de inicio → Agregar**.
3. Ábrela desde el ícono. Se abre a pantalla completa, como una app.
4. Dentro de la app ve a **Respaldo → Importar respaldo** y elige el archivo `respaldo-cerros-2026-10-25.json` para cargar tus tiempos y planes.

## Cómo hacer cambios

1. En GitHub abre `index.html` y toca el lápiz ✏️ para editar. También puedes pedirle el cambio a Claude y subir el archivo nuevo con **Add file → Upload files**, que reemplaza el anterior.
2. Abre `sw.js` y sube el número de versión: `cerros-v1` → `cerros-v2`. Así el iPhone descarga la versión nueva en vez de la guardada.
3. Toca **Commit changes**. En uno o dos minutos el cambio está publicado.

Cada cambio queda registrado en el historial (**Commits**), así que siempre puedes volver a una versión anterior.

## Tus datos

- Los planes y tiempos se guardan **en el navegador de cada dispositivo**. No se suben a GitHub ni quedan públicos.
- No se sincronizan solos entre el iPhone y el computador. Para pasarlos, usa **Descargar respaldo** en uno e **Importar respaldo** en el otro.
- Si borras los datos de Safari o desinstalas la app, se pierden. Descarga un respaldo de vez en cuando.

Cuando quieras sincronización automática entre dispositivos, el siguiente paso es conectar una base de datos gratuita como Supabase.
