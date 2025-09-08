# aplicacionCitas
Aplicación Móvil para Citas, incluye autenticación segura y procesamiento de datos en la nube

## Estrategia de Ramas

Este repositorio utiliza un flujo de trabajo basado en lanzamientos versionados para garantizar la estabilidad del código y un desarrollo organizado. Las ramas principales son:

-   **main**: Esta es la rama principal y refleja el código que está en **producción**. Es una rama estable y protegida. Solo se actualiza a partir de la rama `release` cuando una nueva versión está lista para ser desplegada.

-   **release**: Actúa como una rama de "pre-producción". En ella se integran todas las funcionalidades y correcciones que compondrán una próxima versión. Es la rama donde se realizan las pruebas finales de integración antes de pasar a `main`.

-   **vX.X.X** (ej. `v1.1.0`, `v1.2.0`): Son las ramas de desarrollo para una versión específica. Se crean a partir de `release` y sirven como base para integrar nuevas funcionalidades (`features`) y correcciones (`fixes`) .
 
-   **Ramas de Tarea**: Son ramas de corta duración que se crean a partir de una rama de versión (ej. `v1.1.0`). Aquí es donde se trabaja en una tarea específica. Una vez completada, se integra de nuevo en la rama de versión correspondiente.

## Nomenclatura para Ramas y Commits

Para mantener la consistencia y claridad, utilizamos la convención de **Conventional Commits**.

**Formato de Rama**: `tipo(alcance)-descripción-breve`

-   **`tipo`**: Describe el cambio.
    -   `feat`: Una nueva funcionalidad para el usuario.
    -   `fix`: Una corrección de un bug.
    -   `docs`: Cambios exclusivos en la documentación.
    -   `refactor`: Cambios en el código que no corrigen un bug ni añaden una funcionalidad.
    -   `test`: Añadir o modificar tests existentes.
    -   `chore`: Tareas de mantenimiento (actualizar dependencias, scripts, etc.).

-   **`(alcance)`**: El contexto o módulo del código que se modifica (ej. `api`, `ui`, `auth`, `db`). Es opcional.

-   **`descripción`**: Un resumen corto en imperativo y minúsculas (ej. `add-patient-endpoint`).

**Ejemplos**:
-   `feat(api)-add-patient-endpoint`
-   `fix(ui)-correct-login-button-alignment`


  ## Protección de Ramas Para garantizar la máxima estabilidad y calidad del código en las ramas críticas, se han establecido las siguientes reglas de protección:

-   **Ramas Protegidas**: `main`, `release` y todas las ramas de versión (`v*.*.*`).
-   **No se permiten pushes directos**: Nadie puede enviar cambios directamente a estas ramas.
-   **Integración mediante Pull Request (PR)**: Todo cambio debe ser propuesto a través de un Pull Request.
-   **Aprobaciones Requeridas**: Para que un Pull Request pueda ser fusionado en una rama protegida, debe contar con la aprobación de al menos **dos miembros del equipo**.

-   ## Flujo de Trabajo para el Desarrollo

El ciclo de vida de una nueva funcionalidad o corrección es el siguiente:

1.  **Inicio de una Versión**: Se crea una nueva rama de versión (ej. `v1.1.0`) a partir de la rama `release`.

2.  **Desarrollo de Tareas**: Para cada nueva funcionalidad o corrección de bug, se crea una sub-rama a partir de la rama de versión actual.
    -   **Ejemplo de nueva función**: `git checkout -b feat(ui)-Citas v1.1.0`
    -   **Ejemplo de corrección**: `git checkout -b fix(ui)-Citas-BugVisual v1.1.0`

3.  **Integración de Tareas**: Una vez que el trabajo en la sub-rama está completo y probado, se crea un *Pull Request (PR)* para fusionarla con su rama de versión de orige esto permite la revisión de código.

4.  **Cierre del Sprint / Preparación del Lanzamiento**: Al final del sprint o cuando todas las tareas para la versión están completas, la rama de versión (`v1.1.0`) se fusiona con la rama `release` a través de un *Pull Request*.

5.  **Pruebas Finales**: En la rama `release` se realizan las últimas pruebas de regresión e integración para asegurar que la versión es estable.

6.  **Lanzamiento a Producción**: Una vez que `release` está validada y libre de errores críticos, se fusiona con `main`. En este punto, se crea un *tag* con el número de la versión (ej. `git tag -a v1.1.0`) y se procede al despliegue a producción.

 # Cómo Empezar (Getting Started)
*Para el siguiente proyecto se necesitan conocimientos en los siguientes lenguajes de programación:*
- JavaScript
- CSS

*Además de conocer* **React y NextJS**

**Una vez dicho esto es necesario clonar el repositorio con el siguiente comando**
*git clone https://github.com/Carmona52/aplicacionCitas.git*

*Ya clonado procederemos a ir a la carpeta donde clonamos el repositorio y hacer los siguientes pasos*

# Instalación de librerias y dependencias
**npm install**

# Ejecución del proyecto
**npm run dev** 
