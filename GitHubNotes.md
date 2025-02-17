# 1. Apuntes Esenciales de Git para Programación

## 1.1. ¿Qué es Git y por qué usarlo?
Git es un sistema de control de versiones distribuido que permite a los desarrolladores rastrear cambios en el código, colaborar con otros y mantener un historial de versiones seguro y organizado.

## 1.2. Comandos Esenciales
### 1.2.1. Configuración
```sh
# Configurar nombre de usuario
git config --global user.name "Tu Nombre"

# Configurar correo electrónico
git config --global user.email "tuemail@example.com"

# Ver la configuración actual
git config --list
```

### 1.2.2. Inicialización y Clonación
```sh
# Iniciar un nuevo repositorio en el directorio actual
git init

# Clonar un repositorio remoto
git clone <URL_DEL_REPO>
```

### 1.2.3. Gestión de Cambios
```sh
# Ver estado del repositorio
git status

# Agregar archivos al área de staging
git add <archivo>
# Agregar todos los archivos
git add .

# Confirmar cambios con un mensaje
git commit -m "Mensaje descriptivo del cambio"

# Ver historial de commits
git log
```

### 1.2.4. Trabajo con Ramas (Branches)
```sh
# Listar ramas
git branch

# Crear una nueva rama
git branch <nombre_rama>

# Cambiar a otra rama
git checkout <nombre_rama>

# Crear y cambiar a una nueva rama
git checkout -b <nombre_rama>

# Fusionar una rama en la rama actual
git merge <nombre_rama>
```

### 1.2.5. Trabajo con Repositorios Remotos
```sh
# Agregar un repositorio remoto
git remote add origin <URL_DEL_REPO>

# Ver repositorios remotos configurados
git remote -v

# Enviar cambios al repositorio remoto
git push origin <nombre_rama>

# Obtener cambios del repositorio remoto
git pull origin <nombre_rama>

# Descargar cambios sin fusionar automáticamente
git fetch
```

### 1.2.6. Manejo de Cambios y Resolución de Conflictos
```sh
# Revertir un archivo modificado al último commit
git checkout -- <archivo>

# Deshacer el último commit (manteniendo los cambios en staging)
git reset --soft HEAD~1

# Deshacer el último commit (eliminando cambios)
git reset --hard HEAD~1

# Resolver conflictos de fusión manualmente, luego:
git add <archivo_resuelto>
git commit -m "Conflicto resuelto"
```

### 1.2.7. Buenas Prácticas
- Escribe mensajes de commit claros y descriptivos.
- Usa ramas para organizar características y correcciones.
- Realiza `pull` antes de hacer `push` para evitar conflictos.
- Usa `.gitignore` para excluir archivos innecesarios del repositorio.

### 1.2.8. Archivo `.gitignore`
Ejemplo de `.gitignore` para proyectos en Node.js:
```
node_modules/
.env
.DS_Store
```

---
Estos comandos y prácticas te ayudarán a gestionar proyectos de programación de manera eficiente con Git.git 