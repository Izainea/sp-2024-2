
# Instructivo completo para manejar GitHub

## Introducción a Git y GitHub

### ¿Qué es Git?
Git es un sistema de control de versiones distribuido que permite registrar los cambios en el código fuente a lo largo del tiempo. Facilita la colaboración entre múltiples desarrolladores y la gestión eficiente de proyectos.

> **Nota:** Git permite trabajar de manera offline y sincronizar los cambios posteriormente con el repositorio remoto.

### ¿Qué es GitHub?
GitHub es una plataforma de alojamiento de código basada en la web que utiliza Git para el control de versiones. Proporciona herramientas para la colaboración y la distribución de proyectos.

> **Resumen:** Git = control de versiones; GitHub = plataforma de colaboración y hospedaje de repositorios Git.

## Instalación y configuración de Git

### Instalación de Git en diferentes sistemas operativos

- **Windows**: Descargar e instalar desde [git-scm.com](https://git-scm.com/). Aceptar las configuraciones predeterminadas durante la instalación.
- **macOS**: Usar Homebrew.
    ```bash
    brew install git
    ```
- **Linux**: Instalar desde el gestor de paquetes.
    ```bash
    sudo apt-get install git  # Debian/Ubuntu
    sudo yum install git      # Fedora
    ```

### Configuración inicial de Git

Configurar tu nombre de usuario y correo electrónico. Esto se usará en cada commit.

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
```

> **Tip:** Usa el comando `git config --list` para verificar tu configuración.

## Comandos básicos de Git

- **Inicializar un repositorio**:
    ```bash
    git init
    ```
  > **Nota:** Este comando crea un nuevo repositorio Git en el directorio actual.

- **Clonar un repositorio**:
    ```bash
    git clone https://github.com/usuario/repositorio.git
    ```
  > **Tip:** Clonar un repositorio crea una copia local del repositorio remoto.

- **Ver el estado del repositorio**:
    ```bash
    git status
    ```
  > **Resumen:** Muestra el estado de los archivos en el área de trabajo y el área de preparación.

- **Añadir cambios al área de preparación**:
    ```bash
    git add nombre_del_archivo
    ```
  ```bash
    git add .
    ```
  > **Tip:** Usa `git add .` para agregar todos los archivos modificados al área de preparación.

- **Crear un commit**:
    ```bash
    git commit -m "Mensaje del commit"
    ```
  > **Nota:** Un commit es un registro de los cambios en el área de preparación.

- **Enviar cambios al repositorio remoto**:
    ```bash
    git push origin main
    ```
  > **Tip:** Asegúrate de estar en la rama correcta antes de hacer `push`.

- **Actualizar el repositorio local con cambios del remoto**:
    ```bash
    git pull origin main
    ```
  > **Resumen:** `pull` es una combinación de `fetch` y `merge`.

## Manejo de ramas en Git

- **Crear una nueva rama**:
    ```bash
    git branch nombre_de_la_rama
    ```
  > **Nota:** Las ramas permiten trabajar en diferentes versiones de un proyecto simultáneamente.

- **Cambiar a una rama diferente**:
    ```bash
    git checkout nombre_de_la_rama
    ```
  > **Tip:** Usa `git checkout -b nombre_de_la_rama` para crear y cambiar a una nueva rama en un solo paso.

- **Fusionar una rama en la rama actual**:
    ```bash
    git merge nombre_de_la_rama
    ```
  > **Nota:** Resolver conflictos de fusión editando manualmente los archivos afectados, luego `git add` y `git commit`.

## Trabajo colaborativo en GitHub

- **Crear un repositorio en GitHub**:
    1. Ir a GitHub y hacer clic en "New repository".
    2. Completar los detalles y crear el repositorio.
    3. Opcional: agregar un archivo README, una licencia y un archivo .gitignore.

- **Clonar un repositorio de GitHub**:
    ```bash
    git clone https://github.com/usuario/repositorio.git
    ```
  > **Tip:** Clonar un repositorio te permite trabajar con una copia local.

- **Usar forks y pull requests**:
    1. Hacer un fork del repositorio.
    2. Clonar el fork a tu máquina local.
        ```bash
        git clone https://github.com/tu_usuario/repositorio_forkeado.git
        ```
    3. Hacer cambios y `push` a tu fork en GitHub.
        ```bash
        git push origin rama_de_cambios
        ```
    4. Crear un pull request desde tu fork al repositorio original.

- **Revisión y aprobación de pull requests**:
    1. Revisar los cambios propuestos en la sección de pull requests del repositorio original.
    2. Comentar, solicitar cambios o aprobar los pull requests.

> **Resumen:** Los forks y pull requests son esenciales para la colaboración en proyectos open-source.

## Buenas prácticas en Git y GitHub

- **Escribir mensajes de commit claros y descriptivos**:
    ```bash
    git commit -m "Añadida la función de autenticación"
    ```
  > **Tip:** Un buen mensaje de commit facilita la comprensión del historial de cambios.

- **Usar `.gitignore`**:
    Crear un archivo `.gitignore` para excluir archivos y directorios no deseados.
    ```bash
    echo node_modules/ >> .gitignore
    ```

- **Estrategias de ramificación (Git Flow, GitHub Flow)**:
    - **Git Flow**: Utiliza ramas para desarrollo (`develop`), producción (`master`) y características (`feature`).
    - **GitHub Flow**: Utiliza ramas cortas basadas en `main` y pull requests para integrar cambios.

> **Resumen:** Usar estrategias de ramificación facilita la gestión de versiones y colaboraciones.

## Herramientas y características avanzadas

- **GitHub Actions**: Automatización de flujos de trabajo directamente en GitHub.
    ```yaml
    name: CI
    on: [push]
    jobs:
      build:
        runs-on: ubuntu-latest
        steps:
        - uses: actions/checkout@v2
        - name: Set up JDK 11
          uses: actions/setup-java@v1
          with:
            java-version: '11'
        - name: Build with Gradle
          run: ./gradlew build
    ```
  > **Nota:** GitHub Actions permite automatizar tareas como integración continua y despliegue.

- **GitHub Pages**: Publicación de sitios web directamente desde repositorios GitHub.
    - Crear una rama `gh-pages` o configurar desde el repositorio en GitHub.

> **Tip:** GitHub Pages es ideal para alojar documentación o sitios personales.

- **GitHub Projects**: Gestión de proyectos y tareas utilizando tableros Kanban.

> **Resumen:** GitHub Projects facilita la gestión de tareas y la organización del trabajo en equipo.

## Recursos adicionales

- **Documentación oficial de Git**: [git-scm.com/doc](https://git-scm.com/doc)
- **Documentación de GitHub**: [docs.github.com](https://docs.github.com/)
- **Tutoriales y guías en línea**: Existen numerosos tutoriales y guías disponibles en línea para profundizar en temas específicos.

> **Tip:** Aprovecha los recursos en línea y la comunidad de GitHub para aprender y resolver dudas.
