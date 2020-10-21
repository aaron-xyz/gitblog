# Gitblog
Blog para estudio y repaso de la terminal, git y github.
Lista de comandos que se explican en este blog corto.

# Git
**Comandos básicos**
- `git init`: Para crear un nuevo repositorio.
- `git add`: Agregar elementos al **index**.
- `git status`: Despliega el estado de cada elemento dentro del directorio de trabajo de git. 
- `git rm --cached`: Elimina los elementos seleccionados del *staging area* previamente agregados por el comando `git add`.
- `git commit -m "mensaje"`: Guardamos una cambio de forma *permanente*, con un mensaje especificando los cambios realizados.
- `git log`: Muetra todos los commits hechos.
- `git diff commitA commitB`: Muestra las diferencias entre el commitA (antes) y el commitB (despues).
- `git show`: Muestra las diferencias entre los ultimos cambios hechos.

**Comandos usando ramas**
- `git reset`: puedes volver a commits anteriores, eliminando todos los commits que habia despues de este. Usarse con cuidado.
    - `git reset --hard`: Usando *hard*, eliminamos todo, incluyendo lo del staging area.
    - `git reset --soft`: Usando *soft*, eliminamos todo, pero queda lo del staging area en caso de que queramos hacer commit de los últimos cambios hechos.
- `git checkout -b "nueva_rama"`: Creamos una nueva rama de nombre `nombre_rama` y te cambias a ella.
- `git checkout nueva_rama`: Nos cambia el `HEAD` a la rama `nombre_rama`.
- `git checkout master`: Nos devuelve a la rama `master`.
- `git checkout -d "nombre_rama"`: Elimina la rama de nombre `nombre_rama`.
- `git branch nueva_rama`: Crea una nueva rama de nombre `nueva_rama` pero permanecemos en la rama actual.
- `git branch -l`: Lista las ramas existentes.
- `git branch -d nombre_rama`: Elimina la rama de nombre `nombre_rama`. En caso de nu funcionar con `-D` forzamos la eliminacion.
- `git brach -m vieja_rama nueva_rama`: Cambiamos el nombre de una rama de `vieja_rama` a `nueva_rama`.

> **Nota importante**: Si queremos cambiar de ubicacion un archivo trackeado, es mejor usar el comando `git mv` para no perder el track y
> evitar posibles dolores de cabeza futuros.

**Comandos para trabajo remoto**
- `git clone <url>`: Copia la ultima version hasta el momento del repositorio remoto con direccion `<url>` en tu directorio local.
- `git remote add origin <url-repository>`: Si no haz clonado un repositorio ya existentey quieres conectar tu repositorio local a un repositorio local a uno remoto. Con esto podras subir cambios al repositorio remoto seleccionado.   
- `git push`: Envia todos los commits hechos en tu repositorio local al repositorio remoto.s
- `git fetch`: Trae todos los cambios del repositorio remoto pero no los aplica. 
- `git merge`: Une los cambios del repositorio remoto traidos por `git merge` con la rama `master` del repositorio local.
- `git pull`: Aplica `fetch` y `merge` en un solo comando.

**Tags y visualizacion de ramas**
- `git log --all`: Muestra todos los commits realizados en todas las ramas.
- `git log -n`: Muestra los ultimos `n` commits, empezando por el mas reciente.
- `git log --stat`: Muestra los cambios realizados en cada commit.
- `git log --all --graph --decorate --oneline`: Muestra todos el historial de registros de manera grafica, ordenada y compacta.
- `git alias arbolito = "git log --all --graph --decorate --oneline"`: Creamos un alias con usando la palabra arbolito. Ahora podemos ejecutar el comando entre comillas solo escribiendo el comando `arbolito`.
- `git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"`: Esta es otra manera de establecer un alias llamando superlog, esta vez dentro del entorno de Git. Ahora podemos ejecutar el comando que tenemos entre comillas solo escrbiendo `git superlog`. El comando entre comillas es una version mejorada del usado en `arbolito`, haciendo usa de una sintaxis mas facil de leer, con mas informacion y bien ordenada.
- `git tag -a v0.1 -m "mensaje" 5fc611d`: Registra un tag con nombre `v0.1`, con mesaje `"mensaje"` y el HASH (`5fc611d`) del commit al que le agregaremos este tag.
- `git tag -l`: Lista los tags existentes.
- `git show-ref --tags`: Lista los tags existentes con sus commits respectivos.
- `git tag -d v0.1`: Elimina el tag de nombre `v0.1` del repositorio local del git.
- `git push origin --tags`: Envia los tags al repositorio remoto en Github.
- `git push origin :refs/tags/nombre-del-tag`: Elimina el tag de nombre `nombre-del-tag` en el repositorio remoto.
- `git push origin nombre-de-la-rama`: Mandar una rama local de nombre `nombre-de-la-rama` al repositorio remoto.

## Github
Comandos para github.