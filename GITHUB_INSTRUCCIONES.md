# Instrucciones para subir el proyecto a GitHub

## Requisitos previos

1. Tener una cuenta en [GitHub](https://github.com/)
2. Tener Git instalado en tu computadora. Si no lo tienes, puedes descargarlo desde [git-scm.com](https://git-scm.com/downloads)

## Pasos para subir el proyecto

### 1. Inicializar el repositorio Git local

Abre una terminal (PowerShell o CMD en Windows) y navega hasta la carpeta de tu proyecto:

```
cd c:\Users\hansd\Downloads\project225
```

Inicializa un repositorio Git en esta carpeta:

```
git init
```

### 2. Añadir los archivos al área de preparación

Añade todos los archivos del proyecto al área de preparación:

```
git add .
```

### 3. Realizar el primer commit

Crea un commit con los archivos añadidos:

```
git commit -m "Primer commit: Proyecto de E-Commerce para Android"
```

### 4. Crear un nuevo repositorio en GitHub

1. Inicia sesión en tu cuenta de GitHub
2. Haz clic en el botón "+" en la esquina superior derecha y selecciona "New repository"
3. Asigna un nombre al repositorio (por ejemplo, "project225" o "android-ecommerce")
4. Puedes añadir una descripción opcional
5. Elige si quieres que el repositorio sea público o privado
6. NO inicialices el repositorio con README, .gitignore o licencia, ya que ya tienes estos archivos localmente
7. Haz clic en "Create repository"

### 5. Conectar tu repositorio local con GitHub

Después de crear el repositorio, GitHub te mostrará comandos para conectar tu repositorio local. Ejecuta el siguiente comando en tu terminal (reemplaza `TU_USUARIO` y `NOMBRE_REPOSITORIO` con tus datos):

```
git remote add origin https://github.com/TU_USUARIO/NOMBRE_REPOSITORIO.git
```

### 6. Subir tu código a GitHub

Finalmente, sube tu código al repositorio remoto:

```
git push -u origin master
```

O si estás usando la rama principal como "main":

```
git push -u origin main
```

### 7. Verificar que todo se haya subido correctamente

1. Visita tu repositorio en GitHub (https://github.com/TU_USUARIO/NOMBRE_REPOSITORIO)
2. Deberías ver todos tus archivos, incluyendo el README.md con los diagramas (si las imágenes están en la carpeta `images`, también se subirán)

## Consideraciones adicionales

### Ignorar archivos innecesarios

El proyecto ya incluye un archivo `.gitignore` que excluye archivos generados automáticamente y archivos de configuración específicos del entorno. Si necesitas ignorar archivos adicionales, puedes editar este archivo.

### Actualizar el repositorio

Cuando realices cambios en tu proyecto, puedes subirlos a GitHub con los siguientes comandos:

```
git add .
git commit -m "Descripción de los cambios realizados"
git push
```

### Visualización de imágenes en GitHub

GitHub renderiza automáticamente los archivos Markdown, por lo que tu README.md se mostrará correctamente con las imágenes de los diagramas, siempre que las rutas sean correctas y las imágenes estén en el repositorio.

### Problemas con archivos grandes

Si tienes problemas al subir archivos grandes (como imágenes de alta resolución), considera usar [Git LFS](https://git-lfs.github.com/) (Large File Storage).

## Solución de problemas comunes

### Error de autenticación

Si recibes un error de autenticación al intentar hacer push, es posible que necesites configurar tu autenticación. GitHub ya no acepta autenticación por contraseña para operaciones Git. En su lugar, puedes:

1. Usar GitHub CLI
2. Configurar una clave SSH
3. Usar un token de acceso personal

Para más información, consulta la [documentación oficial de GitHub sobre autenticación](https://docs.github.com/es/authentication).

### Conflictos de fusión

Si trabajas con colaboradores y surgen conflictos de fusión, deberás resolverlos antes de poder hacer push. Consulta la [documentación de Git sobre resolución de conflictos](https://git-scm.com/book/es/v2/Ramificaciones-en-Git-Procedimientos-Básicos-para-Ramificar-y-Fusionar).