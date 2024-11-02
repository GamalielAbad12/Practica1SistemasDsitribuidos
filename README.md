# Práctica 1: Introducción a Git

**Descripción:**

En esta práctica, desarrollé un programa llamado `HolaMundo` que imprime en la consola el mensaje **"Hola Git"**. Este programa está escrito en Python, y utilicé la función `print` para mostrar la salida en la consola. El objetivo de esta práctica era comprender los conceptos básicos de Git y GitHub a través de la creación, modificación y subida de un proyecto sencillo. En esta práctica, además, aprendí el uso de comandos básicos de Git para administrar versiones de un proyecto en un entorno de desarrollo local y conectar este repositorio local con uno remoto en GitHub.

**Pasos detallados y comandos utilizados:**

1. **Crear una carpeta para el proyecto:**
   ```bash
   mkdir <nombre_carpeta>
   ```

2. **Inicializar el repositorio Git:**
   ```bash
   git init
   ```
   Este comando convirtió la carpeta en un repositorio de Git, generando una subcarpeta oculta llamada `.git` que almacena toda la información necesaria para el seguimiento de los cambios. Esto incluye el historial de versiones y las configuraciones del repositorio.

3. **Verificar el estado del repositorio:**
   ```bash
   git status
   ```
   Al ejecutar este comando, pude ver el estado actual del repositorio, indicando si había archivos nuevos, modificados o listos para ser confirmados (commits). Este paso me permitió verificar qué cambios se habían realizado antes de registrarlos oficialmente.

4. **Agregar archivos previo al commit:**
   ```bash
   git add <Nombre Archivo>
   ```
   Utilicé `git add` para agregar archivos `.py` previo al commit, preparándolos para su registro.

5. **Hacer un commit de los cambios:**
   ```bash
   git commit -m "Contenido commit"
   ```
   Realicé un commit para registrar los cambios realizados a los archivos, junto con un mensaje descriptivo que facilita el seguimiento de las modificaciones a lo largo del tiempo.

6. **Vincular el repositorio remoto:**
   ```bash
   git remote add origin <URL_del_repositorio>
   ```
   Con este comando, conecté mi repositorio local con un repositorio remoto en GitHub. La URL proporcionada corresponde al repositorio en GitHub donde planeaba almacenar mis cambios. Esta conexión me permite subir y sincronizar mis cambios entre el repositorio local y el remoto.

7. **Subir los cambios al repositorio remoto:**
   ```bash
   git push origin master
   ```
   Este comando me permitió enviar los commits realizados en mi repositorio local al repositorio remoto en GitHub.

> **Nota sobre autenticación:**  
> Durante el uso de `git push`, se me solicitó autenticación en GitHub. Dado que GitHub descontinuó el uso de autenticación por contraseña desde agosto de 2021, debí utilizar un **Token de Acceso Personal (PAT)** como método alternativo para la autenticación. Después de investigar, generé un token en GitHub y configuré la URL remota utilizando este token, ejecutando el siguiente comando:
> ```bash
> git remote set-url origin https://@github.com/GamalielAbad12/Practica1SistemasDistribuidos.git
> ```

**Notas sobre el archivo `.gitignore`:**  
Creé un archivo `.gitignore` para excluir archivos y carpetas que no deseaba incluir en el repositorio, como los archivos de registro `.log`, como `debug.log`. Este archivo me ayudó a asegurarme de que solo los archivos relevantes fueran rastreados y subidos, manteniendo mi repositorio limpio y organizado.

**Verificación de funcionamiento:**  
Al ejecutar el programa `HolaMundo.py`, debería mostrarse en la consola el mensaje "Hola Git". Para verificar que el archivo `debug.log` y otros archivos especificados en `.gitignore` no se subieron al repositorio remoto, utilicé el comando `git status`, el cual muestra solo los archivos que Git está rastreando. Cualquier archivo ignorado por `.gitignore` no aparecerá en esta lista, confirmando que no fue incluido en los futuros commits.
