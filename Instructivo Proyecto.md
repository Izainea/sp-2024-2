
# Guía para crear un repositorio para proyectos de ciencia de datos

## Crear un nuevo repositorio en GitHub

1. Ve a [GitHub](https://github.com/) y accede a tu cuenta.
2. Haz clic en el botón "New" para crear un nuevo repositorio.
3. Completa los detalles del repositorio:
    - Nombre del repositorio (por ejemplo, `proyecto-ciencia-datos`).
    - Descripción (opcional).
    - Configura la visibilidad (público o privado).
    - Opcional: selecciona la opción para añadir un archivo `README.md`, una licencia y un archivo `.gitignore`.
4. Haz clic en "Create repository".

## Clonar el repositorio a tu máquina local

```bash
git clone https://github.com/tu_usuario/proyecto-ciencia-datos.git
cd proyecto-ciencia-datos
```

## Crear las carpetas del proyecto

```bash
mkdir Datos Codigo Documentacion
touch Datos/README.md Codigo/README.md Documentacion/README.md
```

## Configurar la gestión de paquetes con Poetry

Poetry es una herramienta para la gestión de dependencias y empaquetado en Python. Permite definir y gestionar las dependencias de manera sencilla y coherente.

### Instalar Poetry:
Sigue las instrucciones de instalación desde la [documentación oficial de Poetry](https://python-poetry.org/docs/#installation).

### Inicializar un nuevo proyecto con Poetry:

```bash
poetry init
```

Este comando te guiará a través de una serie de preguntas para configurar tu proyecto.

### Instalar dependencias:

```bash
poetry add numpy pandas scikit-learn
```

Puedes añadir cualquier otra dependencia necesaria para tu proyecto.

## Crear un archivo README.md principal

```bash
echo "# Proyecto de Ciencia de Datos" > README.md
```

## Hacer un primer commit y subir los cambios al repositorio remoto

```bash
git add .
git commit -m "Estructura inicial del proyecto"
git push origin main
```

## Crear una nueva rama para trabajar en el proyecto

```bash
git checkout -b desarrollo
```

## Hacer cambios en la rama de desarrollo

Trabaja en la rama `desarrollo` realizando los cambios necesarios en tu proyecto. Por ejemplo, añade código, datos y documentación.

## Hacer commit de los cambios en la rama de desarrollo

```bash
git add .
git commit -m "Añadidos los primeros scripts y datos"
```

## Crear un Pull Request (PR)

### Subir los cambios de la rama `desarrollo` al repositorio remoto:

```bash
git push origin desarrollo
```

### Crear el Pull Request en GitHub:

1. Navegar a tu repositorio en GitHub.
2. Ir a la pestaña de "Pull requests".
3. Hacer clic en "New pull request".
4. Asegúrate de que la base sea `main` y la comparación sea tu rama de desarrollo (`desarrollo`).
5. Revisar los cambios propuestos.
6. Proporcionar un título y descripción para el Pull Request.
7. Hacer clic en "Create pull request".

## Revisar y discutir el Pull Request

1. Revisar los cambios en GitHub.
2. Comentar y discutir cualquier sugerencia o corrección.

## Actualizar el Pull Request (si es necesario)

1. Hacer los cambios en tu rama `desarrollo`.
2. Hacer commit de los cambios.
3. Empujar los cambios a la misma rama:

```bash
git push origin desarrollo
```

GitHub actualizará automáticamente el Pull Request con los nuevos commits.

## Aprobar y fusionar el Pull Request

1. Aprobar el Pull Request en GitHub.
2. Hacer clic en "Merge pull request".
3. Confirmar la fusión.

## Eliminar la rama de desarrollo (opcional pero recomendado)

1. Eliminar la rama en GitHub haciendo clic en "Delete branch".
2. Eliminar la rama localmente:

```bash
git branch -d desarrollo
```

## Resumen del proceso de Pull Request

1. Crear una nueva rama y trabajar en ella.
2. Hacer commit de los cambios y subir la rama al repositorio remoto.
3. Crear un Pull Request en GitHub.
4. Revisar y discutir los cambios en el Pull Request.
5. Realizar cambios adicionales si es necesario y actualizar el Pull Request.
6. Aprobar y fusionar el Pull Request.
7. Eliminar la rama de desarrollo después de fusionar.

## Tips

- **Comentarios constructivos**: Proporciona comentarios útiles y constructivos durante la revisión.
- **Commits frecuentes**: Realiza commits frecuentes con mensajes claros para facilitar la revisión y el seguimiento de cambios.
- **Resolución de conflictos**: Si hay conflictos durante la fusión, resuélvelos localmente y actualiza el Pull Request.

---

