# Gitblog
Blog para estudio y repaso de la terminal, git y github.
Lista de comandos que se explican en este blog corto.

**Comandos básicos**
- `git init`: Para crear un nuevo repositorio.
- `git add`: Agregar elementos al **index**.
- `git status`: Despliega el estado de cada elemento dentro del directorio de trabajo de git. 
- `git rm --cached`: Elimina los elementos seleccionados del *staging area* previamente agregados por el comando `git add`.
- `git commit -m "mensaje"`: Guardamos una cambio de forma *permanente*, con un mensaje especificando los cambios realizados.
- `git log`: Muetra todos los commits hechos.
- `git diff commitA commitB`: Muestra las diferencias entre el commitA (antes) y el commitB (despues).
- `git show`: Muestra las diferencias entre los ultimos cambios hechos.

**Comandos para moverse entre ramas**
- `git reset`: puedes volver a commits anteriores, eliminando todos los commits que habia despues de este. Usarse con cuidado.
    - `git reset --hard`: Usando *hard*, eliminamos todo, incluyendo lo del staging area.
    - `git reset --soft`: Usando *soft*, eliminamos todo, pero queda lo del staging area en caso de que queramos hacer commit de los últimos cambios hechos.
- `git checkout -b "nueva_rama"`: Creamos una nueva rama de nombre `nombre_rama` y te cambias a ella.
- `git checkout nueva_rama`: Nos cambia el `HEAD` a la rama `nombre_rama`.
- `git checkout master`: Nos devuelve a la rama `master`.
- `git checkout -d "nombre_rama"`: Elimina la rama de nombre `nombre_rama`.

> **Nota importante**: Si queremos cambiar de ubicacion un archivo trackeado, es mejor usar el comando git mv para no perder el track y
> evitar posibles dolores de cabeza futuros.

**Comandos para trabajo remoto**
- `git clone <url>`: Copia la ultima version hasta el momento del repositorio remoto con direccion `<url>` en tu directorio local.
- `git remote add origin <url-repository>`: Si no haz clonado un repositorio ya existentey quieres conectar tu repositorio local a un repositorio local a uno remoto. Con esto podras subir cambios al repositorio remoto seleccionado.   
- `git push`: Envia todos los commits hechos en tu repositorio local al repositorio remoto.s
- `git fetch`: Trae todos los cambios del repositorio remoto pero no los aplica. 
- `git merge`: Une los cambios del repositorio remoto traidos por `git merge` con la rama `master` del repositorio local.
- `git pull`: Aplica `fetch` y `merge` en un solo comando.
