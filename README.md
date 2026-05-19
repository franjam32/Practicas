# FCT App Alumnos

App web estática para que los alumnos marquen asistencia de prácticas.

## Qué hace

- Acceso por correo electrónico.
- Código temporal enviado por Google Apps Script.
- Bloqueo automático fuera del periodo de prácticas.
- Marcaje de asistencia: `Asisto` / `No asisto`.
- Si marca `No asisto`, exige motivo y justificante.
- Bandeja de mensajes enviados desde el panel del instructor.

## Antes de subirla a GitHub

1. Abre `index.html`.
2. Comprueba esta línea:

```js
const API_URL = 'https://script.google.com/macros/s/AKfycbwLJnogGie6-IyAzsB7h5ef7tnYf1ZKK2vS2PCBhd9Y-_UZOgrZkTRmLsnx4I7NgwvU5w/exec';
```

Debe ser la URL de tu Apps Script desplegado como aplicación web.

## Subir a GitHub Pages

1. Crea un repositorio nuevo en GitHub, por ejemplo `fct-app-alumnos`.
2. Sube este contenido:
   - `index.html`
   - `README.md`
3. En GitHub entra en `Settings` -> `Pages`.
4. En `Build and deployment`, selecciona:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Guarda.
6. GitHub te dará una URL parecida a:

```text
https://TU_USUARIO.github.io/fct-app-alumnos/
```

Esa será la URL que podrán usar los alumnos.

## Importante

Para que la app funcione desde GitHub Pages, el Apps Script debe tener soporte JSONP.
Usa la versión actualizada de `apps_script_fct_alumnos.gs` incluida en la carpeta superior del proyecto.

Después de pegar la versión actualizada en Apps Script:

1. Pulsa `Implementar`.
2. Elige `Gestionar implementaciones`.
3. Edita la implementación actual o crea una nueva.
4. Selecciona `Nueva versión`.
5. Mantén:
   - Ejecutar como: tú
   - Acceso: cualquier usuario
6. Copia la URL `/exec`.
