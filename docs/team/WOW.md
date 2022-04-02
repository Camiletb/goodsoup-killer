# Guía para trabajar en equipo a lo largo de este proyecto.
## 1 Gestión de ficheros y directorios
Al crearse un nuevo fichero o directorio se actualiza el árbol de contenidos del `goodsoup-killer/README.md`.
Cualquier fichero añadido a un directorio contiene un nombre válido desdel inicio. Intentamos evitar los nombres provisionales, o los nombres "heredados", como el de una imagen descargada de internet. Los nombres de ficheros y directorios empiezan por minúscula, tratan de ser cortos, autodescriptivos, y si se componen de varias palabras, éstas se separan por barrabaja (ejemplo_uno.md).
## 2 Documentación 
* Toda documentación se recogerá en ficheros markdown.
* Crearemos juntos un protocolo para que el código sea autodocumentado, necesitando el menor número de comentarios posibles. Una vez creado, se insertará aquí.
## 3 Gestión de versiones
<div style="text-align: center;">
<img src="https://imgs.xkcd.com/comics/git_commit_2x.png" alt="Commits IRL" width="400"/>

#### Commits IRL. Por xkcd.com
</div>

### ¿Cuándo haremos commits?
Se hará un commit cada vez que se llegue a un punto de progreso estable. Tratando que los cambios entre commits sean pequeños, bien acotados. y más frecuentes.
### ¿Cómo debe ser el mensaje del commit?

Según la recomendación de [Tim Pope](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html), un mensaje debe seguir un estilo como este:
```
Capitalized, short (50 chars or less) summary

More detailed explanatory text, if necessary.  Wrap it to about 72
characters or so.  In some contexts, the first line is treated as the
subject of an email and the rest of the text as the body.  The blank
line separating the summary from the body is critical (unless you omit
the body entirely); tools like rebase can get confused if you run the
two together.

Write your commit message in the imperative: "Fix bug" and not "Fixed bug"
or "Fixes bug."  This convention matches up with commit messages generated
by commands like git merge and git revert.

Further paragraphs come after blank lines.

- Bullet points are okay, too

- Typically a hyphen or asterisk is used for the bullet, followed by a
  single space, with blank lines in between, but conventions vary here

- Use a hanging indent
```
Para crear un mensaje de commit por consola puedes usar:
```
git commit -m "Título" -m "Descripción del commit"
```
Para abrir el editor y poder darle un formato más claro y/o atractivo, con elementos como saltos de línea puedes usar el comando
```
git commit
```

### Buenas prácticas
1. Usa los verbos en presente y no en pasado, como el propio git nos añade en algunas operaciones (usa `add` y no *added*, usa `merge` y no *merged*). 
El verbo indica cómo queremos que se encuentre el proyecto al añadir el commit. **"Si aplico este commit, entonces este commit…**"
    * `add`
    * `change`
    * `fix`
    * `remove`

2. Especifica el tipo de commit con un prefijo. Una convención bastante famosa es la usada por [Angular](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines), con tipos como:
    * `feat`: La nueva característica que agregas a una aplicación en particular.
    * `fix`: Arregla un bug que afecta al usuario.
    * `perf`: Cambios que mejoran el rendimiento del sitio.
    * `style`: Cambios de formato, tabulaciones, espacios o puntos y coma, etc; no afectan al usuario.
    * `refactor`: Cambios de nombre de variables o funciones.
    * `test`: Todo lo relacionado con pruebas.
    * `docs`: Todo lo relacionado con documentación.
    * `chore`: Mantenimiento de código regular.

    En monorepositorios multipaquete, puedes añadir también la información del paquete que es afectado por el commit. Se le conoce como `scope` y sería de la siguiente forma:
    ```
    feat(backend): add filter for cars
    fix(web): remove wrong color
    ```

3. Separa el título del cuerpo del mensaje con una línea vacía.
4. No uses punto final ni puntos suspensivos en el título. 0 suspense.
5. Usa un máximo de 50 caracteres. Si necesitas más, tu commit hace demasiadas cosas.
6. Usa el cuerpo del mensaje para explicar qué cambios has hecho y por qué los hiciste.

7. No asumas que las personas que revisarán el código entienden cuál era el problema original.
8. No pienses que tu código se explica solo.

[Fuente 1: midu.dev](https://midu.dev/buenas-practicas-escribir-commits-git/)

[Fuente 2: freecodecamp.org](https://www.freecodecamp.org/espanol/news/como-escribir-un-buen-mensaje-de-commit/)

## 4 Planificación
Al final de cada semana se plasma el tiempo dedicado a la aplicación (incialmente, 5 horas semanales) en un registro dentro del fichero meeting_minutes (acta de reunión, en castellano), cuya ubicación es: `goodsoup-killer/docs/team/meeting_minutes/log.md`. En este documento se recoge:
* Progreso respecto a la semana anterior.
* Contraste respecto a los objetivos marcados.
    * Qué hemos hecho.
    * Qué no hemos podido hacer.
* Actualicación del árbol de contenidos, si fuera necesario.
* Nuevos objetivos.

Actualizar el documento no debería ocupar más de 15 minutos semanales.