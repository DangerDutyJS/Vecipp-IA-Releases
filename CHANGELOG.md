# Novedades de Vecipp IA

Lo que trae cada versión de la CLI y del escritorio. Los instaladores están en
[Releases](https://github.com/Vecipp/Vecipp-IA-Releases/releases) y en [ia.vecipp.com/descargas](https://ia.vecipp.com/descargas).

## CLI

### CLI Próxima versión
- `vecipp --chrome` activa Vecipp for Chrome **una sola vez**: desde ahí cada inicio se conecta solo a la extensión (`--no-chrome` lo apaga).

### CLI 1.0.3 — 2026-10-11
- **Vecipp for Chrome**: el agente puede usar tu propio Chrome (pestañas, leer páginas, clic, escribir, capturas, errores de consola y peticiones de red), siempre pidiendo permiso antes de actuar. `/chrome` lo conecta y `/chrome login` inicia sesión en la extensión desde la terminal.
- **Reglas del proyecto (VECIPP.md)**: el agente sigue tus reglas como obligatorias, en varios niveles (las tuyas para todos los proyectos, las del proyecto, las de cada subcarpeta). `/init` las escribe y `# regla` agrega una.
- **Pregunta de confianza** la primera vez que abres una carpeta; si dices que sí, se crea `.vecipp/` con sus ajustes.
- **Permisos que no se saltan**: en `.vecipp/settings.json` prohíbes acciones (por ejemplo `git push` o editar el `.env`) y Vecipp las bloquea antes de ejecutar.
- Comandos y subagentes propios en `.vecipp/commands` y `.vecipp/agents`; `/memory`, `/permissions` y `/commands` muestran lo que aplica.

### CLI 1.0.2 — 2026-10-11
- `vecipp --help` muestra dónde ver las novedades y bajar los instaladores: el repo público [Vecipp-IA-Releases](https://github.com/Vecipp/Vecipp-IA-Releases).

### CLI 1.0.1 — 2026-10-11
- **Artefactos al instante**: cuando el agente crea un documento, una página o un diseño, se sube a tu cuenta y se abre solo en tu navegador, ya renderizado, en `ia.vecipp.com/artifacts`.
- `/artifacts` muestra el enlace de cada uno; `/artifacts open off` apaga la apertura automática.
- Artefactos más profesionales: el agente sigue una guía de diseño (paleta, tipografía, modo oscuro, responsive, contenido real).

### CLI 1.0.0 — 2026-10-11
- Primera versión pública: se instala con una línea en Windows, macOS, Linux o un VPS.
- Proveedor **Vecipp IA**: usa los modelos con tu cuenta de Vecipp, sin API key.
- `/uso` y la barra de estado muestran tu uso de la sesión de 5 horas y de la semana, el mismo de la web y el escritorio.
- Tus sesiones se guardan en tu cuenta y se ven en ia.vecipp.com › Código (`/sync on|off`).
- Los artefactos que creas suben solos a ia.vecipp.com › Artefactos.

## Escritorio

### Escritorio 1.0.3 — 2026-10-11
- **Vecipp for Chrome**: el agente puede usar tu propio Chrome con la extensión instalada (pide permiso antes de hacer clic, escribir o navegar).
- **Reglas del proyecto (VECIPP.md) y `.vecipp/settings.json`**: el agente sigue las reglas del proyecto y los permisos prohibidos se bloquean antes de ejecutar.
- **Pregunta de confianza** al abrir una carpeta nueva; si dices que sí, se crea `.vecipp/`.

### Escritorio 1.0.2 — 2026-10-11
- **Ajustes › Acerca de Vecipp IA**: enlaces a las novedades y versiones en GitHub y a ia.vecipp.com/descargas.

### Escritorio 1.0.1 — 2026-10-11
- **Artefactos al instante**: lo que el agente crea (documentos, páginas, diseños) se guarda en tu cuenta y se abre solo en tu navegador, en `ia.vecipp.com/artifacts`.
- Artefactos más profesionales: el agente sigue una guía de diseño (paleta, tipografía, modo oscuro, responsive, contenido real).

### Escritorio 1.0.0 — 2026-10-11
- Primera versión para Windows (beta): el agente de Vecipp con ventana propia, sobre las carpetas de tu PC.
- Proveedor **Vecipp IA** con tu cuenta, y el panel de uso con la sesión de 5 horas y la semana.
- Tus sesiones se guardan en tu cuenta y se ven en ia.vecipp.com › Código.
