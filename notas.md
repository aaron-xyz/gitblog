# Notas cortas: Curso profesional de Git y Github

Estas notas serán cortas y al punto, solo para recordar lo que voy viendo en cada lección y
para futuras referencias. Tal como acostumbro hacerlo.
Eso tal vez cambie en una futura versión, pero no se sabe. ;)

## 2. Comandos básicos en Git
### 2.3 Crea un repositorio de Git y haz to primer commit
Práctica 1: Comandos básicos
- git init
- git add
- git status
- git rm --cached
- git commit -m "mensaje"
- git log
### 2.4 Analizar cambios en tu proyecto con Git
- git diff commitA commitB
- git show
### 2.5 Volver en el tiempo en nuestros repositorios utilizando reset y checkout
- git reset
    - git reset --hard
    - git reset --soft
- git checkout
> **Nota importante**: Si queremos cambiar de ubicacion un archivo trackeado, es mejor usar el comando git mv para no perder el track y
> evitar posibles dolores de cabeza futuros.

## 3. Flujo de trabajo basico en Git
### 3.1 Flujo de trabajo basico con un repositorio remoto
- git clone
- git push
- git fetch
- git merge
- git pull
