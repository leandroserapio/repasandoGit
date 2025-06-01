# 📚 Notas de Curso Git

> **Fuente del curso:** [Git y GitHub desde cero - HolaMundo](https://www.youtube.com/watch?v=VdGzPZ31ts8&t=14s&ab_channel=HolaMundo)

---

## 🔍 ¿Qué es Git?

Git es un **sistema de control de versiones distribuido** que nos permite mantener un historial completo de todo el código que escribimos. A medida que el código crece, aumenta la probabilidad de errores, y Git nos ayuda a gestionarlos eficientemente.

### 🔑 Características principales

- **📜 Rollback:** Capacidad de volver a una versión anterior del código
- **🌐 Descentralizado:** Cada desarrollador tiene una copia completa del código
- **🔄 Sincronización:** Los cambios pueden ser sincronizados entre diferentes copias

### 🎯 Usos principales de Git

- Mantener un historial detallado de cambios
- Almacenar y versionar código fuente
- Facilitar el trabajo colaborativo en equipo
- Identificar cuándo y dónde se introdujo un error

---

## 💻 Configuración inicial

### Terminal y Git Bash
Git se utiliza principalmente a través de la **terminal** o **Git Bash** en Windows.

### Configuración de saltos de línea

En Windows, los saltos de línea utilizan dos caracteres:
- **CR** (Carriage Return)
- **LF** (Line Feed)

Para compatibilidad al subir código, se debe eliminar CR configurando:
```bash
git config core.autocrlf true
```

---

## 📋 Comandos básicos

### Ayuda y navegación
```bash
git config -h          # Ver todas las opciones de configuración
ls                      # Listar archivos (Linux/Mac)
dir                     # Listar archivos (Windows)
cd                      # Cambiar directorio
```

### Inicialización del repositorio
```bash
git init               # Inicializar Git en el directorio actual
```

Al ejecutar `git init`, se crea una carpeta `.git` que contiene:
- HEAD
- config
- description
- hooks/
- info/
- objects/
- refs/

> ⚠️ **Nota:** La carpeta `.git` siempre es ignorada automáticamente

---

## 🔄 Flujo de trabajo Git

### 1. **Working Directory → Stage**
```bash
git add <archivo>      # Agregar archivo específico
git add *.extensión    # Agregar archivos por extensión
git add .              # Agregar todos los archivos (⚠️ MALA PRÁCTICA)
```

### 2. **Stage → Commit**
```bash
git commit -m "mensaje descriptivo"
```

### 3. **Commit → Servidor remoto**
```bash
git push               # Subir cambios al servidor (ej: GitHub)
```

---

## 🛠️ Comandos de gestión

### Verificar estado
```bash
git status             # Ver cambios, archivos nuevos, etc.
```

### Gestión de archivos
```bash
git rm <archivo>       # Eliminar archivo del repositorio
mv archivo.txt nuevo_nombre.txt  # Renombrar archivo
```

### Ver diferencias
```bash
git diff               # Mostrar cambios realizados
```

### Ver contenido de archivos
```bash
cat <archivo>          # Mostrar contenido del archivo
```

---

## 🚫 Archivos a ignorar

Crear un archivo `.gitignore` para excluir:
- Variables de entorno (`.env`)
- Contraseñas
- Configuraciones de bases de datos
- Archivos temporales

```bash
# Ejemplo de .gitignore
.env
*.log
node_modules/
.DS_Store
```

**Proceso:**
1. `git add .gitignore`
2. `git commit -m "Agregar archivo .gitignore"`

---

## 🌿 Trabajo con ramas (Branches)

Las ramas permiten **bifurcar el desarrollo** y posteriormente **unir los cambios**.

### Comandos de ramas
```bash
git branch                    # Ver rama actual
git checkout -b <nombre>      # Crear y cambiar a nueva rama
git checkout <rama>           # Cambiar de rama
git merge <nombre_rama>       # Unir rama (desde master/main)
```

### 📝 Flujo de trabajo con ramas
1. Crear nueva rama para función específica
2. Desarrollar en la rama secundaria
3. Cambiar a rama principal (master/main)
4. Hacer merge de los cambios

> ⚠️ **Importante:** Para hacer merge, debes estar en la rama de destino (generalmente master/main)

---

## 📝 Buenas prácticas

- ✅ Hacer commits frecuentes con mensajes descriptivos
- ✅ Usar ramas para nuevas funcionalidades
- ✅ Mantener el archivo `.gitignore` actualizado
- ❌ Evitar `git add .` indiscriminadamente
- ❌ No commitear archivos sensibles (contraseñas, variables de entorno)