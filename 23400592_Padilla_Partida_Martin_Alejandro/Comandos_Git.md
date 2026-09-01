# Lista de comandos para git
Pequeña lista de comandos de Git para equipos.


---
### Configuración local inicial
> **git config --global user.name "MartinPadilla":** Define tu nombre global para firmar commits en tu máquina.

**Caso de uso:** Acabas de instalar Git en tu nueva computadora y necesitas registrar tu nombre para que cada commit que hagas lleve tu firma.

> **git config --global user.email "example@gmail.com":** Define tu email global para firmar commits en tu máquina.

**Caso de uso:** Vinculas tu dirección de correo electrónico a la configuración global de Git para que plataformas como GitHub o GitLab reconozcan las contribuciones que haces desde tu laptop.

---

### Configuración de repositorio local
> **git init:** Inicializa un repositorio de git en la carpeta actual.

**Caso de uso:** Creaste una carpeta vacía en tu sistema para iniciar un proyecto nuevo desde cero y necesitas activar el control de versiones en esa carpeta.

> **git remote add origin [URL-GITHUB]:** Conecta tu repositorio local con tu repositorio de GitHub.

**Caso de uso:** Tienes un proyecto ya creado en tu computadora y acabas de crear un repositorio vacío en GitHub; ejecutas este comando para enlazar ambos entornos.

---

### Interacción con remote (GitHub)
> **git clone:** Descarga un repositorio remoto a tu máquina local.

**Caso de uso:** Te integras a un equipo de desarrollo y necesitas descargar por primera vez todo el código del proyecto que está alojado en GitHub a tu computadora.

> **git pull:** Trae cambios del repositorio remoto.

**Caso de uso:** Llegas a trabajar por la mañana y deseas actualizar tu copia local con los cambios que tus compañeros subieron al repositorio remoto durante la noche.

> **git pull --rebase:** Trae los cambios del repositorio remoto y "adelanta" tus commits locales sobre los commits remotos, manteniendo un historial lineal.

**Caso de uso:** Un compañero subió cambios a la rama principal mientras tú trabajabas localmente; ejecutas esto para colocar tus commits arriba de los de él y mantener un historial limpio sin merge commits.

> **git pull --merge:** Trae los cambios del repositorio remoto y crea un merge commit para combinar los cambios remotos con los locales si hay divergencia.

**Caso de uso:** Necesitas traer las novedades del servidor remoto sabiendo que tus cambios locales entraron en divergencia, creando explícitamente un commit de fusión para unir ambas historias.

> **git push:** Sube tus commits locales al repositorio remoto.

**Caso de uso:** Terminaste de programar una funcionalidad en una rama previamente vinculada y deseas enviar tus últimos commits al repositorio remoto.

> **git push -u origin [nombre rama]:** Sube una nueva rama al remoto y la deja vinculada con la rama actual para futuros push/pull automaticos.

**Caso de uso:** Creaste localmente la rama feature-login y es la primera vez que la vas a subir a GitHub, estableciendo el rastreo automático para futuros envíos.

---

### Creación de commit
> **git status:** Nos indica el estado actual de los archivos que podemos agregar o commitear.

**Caso de uso:** Modificaste tres archivos y agregaste uno nuevo; usas este comando para revisar qué archivos han sido detectados por Git y cuáles están listos para el commit.

> **git add .:** Agrega todos los cambios del directorio actual al área de staging (Zona intermedia donde se almacena todo lo que va entrar en el siguiente commit).

**Caso de uso:** Hiciste cambios en el diseño, la lógica y la base de datos local de tu proyecto y quieres agregar absolutamente todo el trabajo reciente al área de preparación (staging).

> **git commit -m "Cambios del commit:"** Crea un commit con los cambios agregados y el mensaje especificado.

**Caso de uso:** Guardas una foto fija de los cambios que pusiste en staging asignándole una nota breve que explique lo realizado.

---

### Historial de commits
> **git log:** Muestra el historial completo de commits con detalles. (Si es muy largo, usa las flechas para navegar y "Q" para salir).

**Caso de uso:** Detectaste un error reciente en el código y necesitas inspeccionar detalladamente los últimos commits, quién los hizo, la fecha y la hora exacta.

> **git log --oneline:** Muestra el historial resumido en una linea por commit.

**Caso de uso:** Quieres revisar rápidamente la lista compacta de commits realizados en el proyecto sin ver detalles extra como fechas o correos de los autores.

>**git stash:** Almacena temporalmente en borrador los cambios no guardados para dejar limpio el directorio de trabajo.

**Caso de uso:** Estás a la mitad de programar una función y tus cambios no están listos para hacer un commit, pero surge una emergencia y necesitas cambiarte de rama para corregir un fallo crítico. Guardas temporalmente tu trabajo inconcluso en un borrador para dejar tu directorio limpio sin perder nada.

---

### Manejo de ramas
> **git checkout:** Cambia tu posición a otra rama o commit.

**Caso de uso:** Deseas salir de la rama de trabajo feature-login y moverte a la rama main para verificar cómo estaba la aplicación antes de tus cambios.

> **git checkout -b [nombre nueva rama]:** Crea una nueva rama y se mueve a ella.

**Caso de uso:** Vas a empezar a trabajar en la vista de perfil de usuario, por lo que creas la rama feature-perfil y te cambias a ella en un solo paso.

> **git merge [rama a mergear]:** Fusiona la rama indicada con la rama actual.

**Caso de uso:** Terminaste y probaste la funcionalidad de la rama feature-perfil, te posicionas en main y ejecutas el comando para incorporar ese trabajo a la rama principal.

> **git branch -d [nombre rama]:** Elimina la rama seleccionada.

**Caso de uso:** La funcionalidad de feature-perfil ya fue integrada con éxito en main, así que procedes a borrar la rama local para mantener limpio tu espacio de trabajo.

---
