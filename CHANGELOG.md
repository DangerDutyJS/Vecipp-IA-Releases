# Novedades de Vecipp IA

Lo que trae cada versión de la CLI y del escritorio. Los instaladores están en
[Releases](https://github.com/Vecipp/Vecipp-IA-Releases/releases) y en [ia.vecipp.com/descargas](https://ia.vecipp.com/descargas).

## CLI

### CLI 1.0.5 — 2026-10-12
- **Interfaz más limpia**: el banner queda arriba y el prompt abajo, con el espacio libre en medio; tus mensajes quedan como una sola línea `└─$ …` (el encabezado `┌──(vecipp㉿…)` ya no se repite); menos colores: verde para los marcos, blanco para el texto y gris para lo demás.
- **Más transparencia**: arranca con un 25 %. Si ya la cambiaste con `/appearance`, se respeta tu elección.
- **Cada vez que abres la CLI, conversación nueva** (como Claude). Para retomar la última de esa carpeta: `vecipp --continue` (o `-c`); `/resume` elige cualquiera.
- **Hostinger AI Router**: nuevo proveedor con Claude, GPT, Gemini, Grok y Kimi en una sola clave de créditos (`/provider`).

### CLI 1.0.4 — 2026-10-12
- **Interfaz nueva, estilo Kali**: pantalla completa con el prompt `┌──(vecipp㉿proyecto)-[~/ruta]` / `└─$` fijo abajo, marcas `[+] [-] [*] [!]` en cada acción, banner nuevo y enlaces azules. Sin parpadeos: al agrandar o achicar la ventana se redibuja de un golpe y todo se acomoda al ancho. Al salir, la conversación queda en tu terminal.
- **Terminal translúcida**: arranca con un 15 % de transparencia y `/appearance` la cambia en vivo (o la quita y deja tu terminal como estaba). Windows Terminal, GNOME Terminal (Ubuntu), QTerminal y Xfce (Kali).
- **Modo root**: `shift+tab` pasa de normal → root (aprobación automática: el prompt se pone rojo con `#`) → plan (pregunta todo).
- **Escribe mientras trabaja**: Enter con el agente ocupado le agrega tu mensaje a lo que está haciendo, sin interrumpirlo. Esc interrumpe.
- **Ratón de verdad**: la rueda desplaza la conversación (se queda quieta si estás leyendo arriba y sigue lo nuevo si estás abajo), arrastrar selecciona y copia (también por SSH), clic derecho pega, clic en un cambio abre su diff en un panel a la derecha, clic en un enlace lo abre, clic en el prompt mueve el cursor.
- **Atajos**: `ctrl+p` paleta de comandos, `ctrl+r` buscar en tus mensajes, `ctrl+o` enlaces, `ctrl+f` último cambio, `ctrl+t` tareas, `ctrl+y` copia la última respuesta, `?` todos los atajos. Consejos rotativos bajo el prompt.
- **Prompt completo**: flechas, Inicio/Fin, por palabras con `ctrl+←/→`, `\` + Enter para otra línea, pegar varias líneas; `@archivo` menciona un archivo (tab completa) y `!comando` lo corres tú y el agente ve la salida.
- **Freno de seguridad**: aunque tengas la aprobación automática, el agente pregunta siempre antes de un comando destructivo (borrar carpetas, `git reset --hard`, `git push --force`…) o de escribir fuera de la carpeta del proyecto.
- **Cada carpeta, su conversación**: al abrir la CLI en otra carpeta empieza limpia; en la tuya retoma la tuya.
- El agente ahora **lee PDF y notebooks** de Jupyter, **busca en la web**, lee una página respondiendo solo lo que pregunta, usa **PowerShell** además de Bash, **espera** a que un servidor esté listo sin consultar en bucle y busca en el código con más precisión (por tipo de archivo, con líneas de contexto, solo nombres o conteos).
- **Subagente general**: puede editar y correr comandos, pidiéndote permiso igual que el agente principal.
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

### Escritorio Próxima versión
- **Freno de seguridad**: aunque tengas la aprobación automática, el agente pregunta siempre antes de un comando destructivo (borrar carpetas, `git reset --hard`, `git push --force`…) o de escribir fuera de la carpeta del proyecto.
- El agente ahora **lee PDF y notebooks** de Jupyter, **busca en la web**, lee una página respondiendo solo lo que pregunta, usa **PowerShell** además de Bash, **espera** a que un servidor esté listo sin consultar en bucle y busca en el código con más precisión (por tipo de archivo, con líneas de contexto, solo nombres o conteos).
- **Subagente general**: puede editar y correr comandos, pidiéndote permiso igual que el agente principal.

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
