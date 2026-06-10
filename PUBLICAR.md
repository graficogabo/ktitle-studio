# Guía: publicar KTitle Studio en GitHub

Esta guía te lleva paso a paso para subir el proyecto a un repositorio de GitHub y publicarlo con GitHub Pages.

---

## Requisitos previos

- Tener [Git instalado](https://git-scm.com/downloads) en tu computadora
- Tener una cuenta de GitHub
- (Opcional) Configurar Git con tu identidad la primera vez:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

---

## Paso 1 — Crear el repositorio en GitHub

1. Entra a [github.com/new](https://github.com/new)
2. **Repository name**: `ktitle-studio` (o el nombre que prefieras)
3. **Description**: `Generador de títulos animados para Kdenlive`
4. Selecciona **Public**
5. **NO** marques "Add a README", "Add .gitignore" ni "Choose a license" (ya los tenemos en local)
6. Haz clic en **Create repository**

GitHub te mostrará la URL del repo, algo como:
`https://github.com/graficogabo/ktitle-studio.git`

---

## Paso 2 — Preparar la carpeta local

Abre una terminal en la carpeta que contiene estos archivos (`index.html`, `README.md`, `LICENSE`, `.gitignore`) y ejecuta:

```bash
# Inicializar el repositorio Git
git init

# Agregar todos los archivos
git add .

# Crear el primer commit
git commit -m "Initial commit: KTitle Studio v1.0"
```

---

## Paso 3 — Conectar con GitHub y subir

Reemplaza la URL por la de tu repositorio:

```bash
# Renombrar la rama principal a main
git branch -M main

# Conectar tu repo local con GitHub
git remote add origin https://github.com/graficogabo/ktitle-studio.git

# Subir todo a GitHub
git push -u origin main
```

Si te pide credenciales, usa tu usuario de GitHub y un **token de acceso personal** (no tu contraseña). Puedes generar uno en: *GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)* con permiso `repo`.

---

## Paso 4 — Publicar con GitHub Pages

1. En tu repositorio en GitHub, ve a **Settings**
2. En el menú lateral, haz clic en **Pages**
3. En **Source**, selecciona la rama **main** y la carpeta **/ (root)**
4. Haz clic en **Save**
5. Espera 1-2 minutos. GitHub te dará una URL pública como:
   `https://graficogabo.github.io/ktitle-studio/`

Esa URL abre `index.html` directamente, así cualquiera puede usar la herramienta sin descargar nada.

---

## Cambios futuros

Cada vez que modifiques el proyecto, repite este ciclo:

```bash
# Ver qué archivos cambiaron
git status

# Agregar los cambios
git add .

# Crear un commit describiendo el cambio
git commit -m "Descripción de lo que cambiaste"

# Subir a GitHub
git push
```

GitHub Pages se actualiza automáticamente unos minutos después de cada `push`.

---

## Estructura del repositorio

```
ktitle-studio/
├── index.html       # La aplicación completa (un solo archivo)
├── README.md        # Documentación bilingüe
├── LICENSE          # Licencia GPL v3
├── .gitignore       # Archivos que Git debe ignorar
└── PUBLICAR.md      # Esta guía
```

---

## Consejos

- **Versiones**: cuando hagas un cambio importante, considera crear una *Release* en GitHub (*Releases → Create a new release*) con un número de versión (ej. `v1.1`) para marcar hitos.
- **Issues**: activa los *Issues* en Settings para que la gente reporte errores o sugiera mejoras.
- **Topics**: en la página principal del repo, agrega temas como `kdenlive`, `video-editing`, `title-generator`, `canvas`, `javascript` para que sea más fácil de encontrar.
