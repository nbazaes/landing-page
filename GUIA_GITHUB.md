# 📚 Guía Completa: Cómo Subir Archivos a GitHub

## 🎯 Objetivo
Esta guía te enseña paso a paso cómo subir archivos locales a un repositorio de GitHub desde cero.

---

## 📋 Prerrequisitos

### 1. Tener Git instalado
```bash
# Verificar si Git está instalado
git --version
```
Si no está instalado:
- **Ubuntu/Debian:** `sudo apt install git`
- **CentOS/RHEL:** `sudo yum install git`
- **macOS:** `brew install git`
- **Windows:** Descargar desde https://git-scm.com/

### 2. Tener una cuenta en GitHub
- Crear cuenta en https://github.com
- Verificar tu email

---

## 🚀 Proceso Completo

### Paso 1: Configurar Git (Solo la primera vez)

```bash
# Configurar tu nombre (usar tu nombre real)
git config --global user.name "Tu Nombre Completo"

# Configurar tu email (DEBE ser el mismo de GitHub)
git config --global user.email "tu-email@ejemplo.com"

# Verificar configuración
git config --global --list
```

### Paso 2: Navegar al directorio de tu proyecto

```bash
# Ir al directorio donde están tus archivos
cd /ruta/a/tu/proyecto

# Verificar que estés en el lugar correcto
pwd
ls -la
```

### Paso 3: Inicializar repositorio Git local

```bash
# Inicializar repositorio Git
git init

# Verificar estado
git status
```

### Paso 4: Crear archivo .gitignore (Recomendado)

```bash
# Crear archivo .gitignore
touch .gitignore
```

Contenido típico para proyectos web:
```gitignore
# Archivos del sistema
.DS_Store
Thumbs.db

# Archivos temporales
*.tmp
*.temp

# Dependencias
node_modules/
.npm/

# Logs
*.log

# IDEs
.vscode/
.idea/
*.swp
```

### Paso 5: Añadir archivos al staging area

```bash
# Añadir archivos específicos
git add archivo1.html archivo2.css

# O añadir todos los archivos
git add .

# Verificar qué se añadió
git status
```

### Paso 6: Hacer el primer commit

```bash
# Hacer commit con mensaje descriptivo
git commit -m "Initial commit: Add project files"

# Verificar historial
git log --oneline
```

### Paso 7: Crear repositorio en GitHub

1. **Ir a GitHub.com**
2. **Hacer clic en "+" → "New repository"**
3. **Llenar información:**
   - Repository name: `mi-proyecto`
   - Description: (opcional)
   - Public/Private: según prefieras
   - **NO marcar** "Add a README file"
   - **NO marcar** "Add .gitignore"
   - **NO marcar** "Choose a license"
4. **Hacer clic en "Create repository"**
5. **Copiar la URL del repositorio** (aparece después de crear)

### Paso 8: Conectar repositorio local con GitHub

```bash
# Añadir repositorio remoto
git remote add origin https://github.com/tu-usuario/tu-repositorio.git

# Verificar conexión
git remote -v

# Cambiar a rama main (estándar actual)
git branch -M main
```

### Paso 9: Subir archivos a GitHub

```bash
# Primera subida
git push -u origin main

# En siguientes ocasiones solo:
git push
```

---

## 🔄 Flujo para Actualizaciones Futuras

Cuando modifiques archivos existentes o añadas nuevos:

```bash
# 1. Verificar cambios
git status

# 2. Añadir cambios
git add .

# 3. Hacer commit
git commit -m "Descripción clara de los cambios"

# 4. Subir a GitHub
git push
```

---

## 🌐 Activar GitHub Pages (Opcional)

Para que tu sitio web sea público:

1. **Ir a tu repositorio en GitHub**
2. **Settings → Pages**
3. **Source:** "Deploy from a branch"
4. **Branch:** "main"
5. **Save**

Tu sitio estará en: `https://tu-usuario.github.io/nombre-repositorio`

---

## 🐛 Comandos de Troubleshooting

### Verificar estado actual
```bash
git status
git log --oneline
git remote -v
```

### Deshacer cambios
```bash
# Deshacer cambios no confirmados
git checkout -- archivo.txt

# Deshacer último commit (mantener cambios)
git reset --soft HEAD~1

# Ver diferencias
git diff
```

### Problemas comunes

#### Error: "fatal: not a git repository"
```bash
# Solución: Inicializar repositorio
git init
```

#### Error: "Author identity unknown"
```bash
# Solución: Configurar usuario
git config --global user.name "Tu Nombre"
git config --global user.email "tu-email@ejemplo.com"
```

#### Error: "remote origin already exists"
```bash
# Solución: Actualizar URL
git remote set-url origin https://github.com/usuario/repo.git
```

---

## 📝 Buenas Prácticas

### Mensajes de Commit
- **Usar presente:** "Add feature" no "Added feature"
- **Ser descriptivo:** "Fix login validation bug" no "Fix bug"
- **Mantener línea corta:** Máximo 50 caracteres

### Estructura de Proyectos
```
mi-proyecto/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
├── images/
│   └── logo.png
├── .gitignore
└── README.md
```

### Archivos importantes
- **README.md:** Descripción del proyecto
- **.gitignore:** Archivos a ignorar
- **LICENSE:** Licencia del proyecto

---

## 🔗 Comandos de Referencia Rápida

```bash
# Configuración inicial
git config --global user.name "Nombre"
git config --global user.email "email@ejemplo.com"

# Flujo básico
git init
git add .
git commit -m "mensaje"
git remote add origin URL
git push -u origin main

# Actualizaciones
git add .
git commit -m "mensaje"
git push

# Información
git status
git log
git remote -v
```

---

## 📚 Recursos Adicionales

- **Documentación oficial:** https://git-scm.com/doc
- **GitHub Guides:** https://guides.github.com/
- **Git Cheat Sheet:** https://education.github.com/git-cheat-sheet-education.pdf
- **Visualizador Git:** https://git-school.github.io/visualizing-git/

---

## ✅ Checklist para Nuevo Proyecto

- [ ] Git configurado con nombre y email
- [ ] Directorio del proyecto ubicado
- [ ] `git init` ejecutado
- [ ] Archivo `.gitignore` creado
- [ ] Archivos añadidos con `git add`
- [ ] Primer commit realizado
- [ ] Repositorio creado en GitHub
- [ ] Repositorio remoto conectado
- [ ] Archivos subidos con `git push`
- [ ] GitHub Pages activado (si es sitio web)

---

**💡 Tip:** Guarda esta guía en tu repositorio como `GUIA_GITHUB.md` para tenerla siempre disponible.

---

*Guía creada el 30 de octubre de 2025 por Nicolás Bazaes*