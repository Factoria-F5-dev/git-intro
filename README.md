# Git

## Índice

- [Introducción](#introducción)
- [Instalaciones](#instalaciones)
- [Conceptos Fundamentales](#conceptos-fundamentales)
- [Flujo de Trabajo en Git](#flujo-de-trabajo-en-git)
- [Comandos Esenciales](#comandos-esenciales)
- [Ejemplo Completo: Proyecto NodeJS](#ejemplo-completo-proyecto-nodejs)
- [Subir código a GitHub](#subir-código-a-github)
- [Despliegue en Heroku](#despliegue-en-heroku)
- [Ejemplo Completo: Proyecto Python](#ejemplo-completo-proyecto-python)
- [Extra: Despliegue en producción](#extra-despliegue-en-producción)
- [Recursos Adicionales](#recursos-adicionales)

---

## 1. Introducción

![Git Logo](https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png)

**Git** 🌐: Git es un sistema de control de versiones distribuido, diseñado para manejar todo, desde proyectos pequeños hasta proyectos muy grandes con velocidad y eficiencia.

🚀 **Git** permite a los desarrolladores rastrear cambios en el código fuente durante el desarrollo de software. Es una herramienta esencial para la colaboración en equipo, ya que facilita la fusión de cambios de múltiples contribuyentes.

👨‍💻 **Linus Torvalds**, el creador de Linux, desarrolló Git en 2005 para gestionar el desarrollo del kernel de Linux. Git fue diseñado para ser rápido, eficiente y capaz de manejar grandes proyectos con miles de colaboradores.

💻 Antes de Git, los sistemas de control de versiones como **CVS** y **Subversion (SVN)** eran populares. Sin embargo, estos sistemas eran centralizados y menos eficientes en términos de velocidad y manejo de ramas. Git introdujo un enfoque distribuido, lo que significa que cada desarrollador tiene una copia completa del repositorio, lo que permite un trabajo más flexible y seguro.

![Meme Git](./img/memegit.png)

🚨 **¿Entendemos para qué sirve? ¿Qué puede pasar en el caso de no usarlo? ¿Qué se usaba antes?** 🚨

---

## 2. Instalaciones

### Instalar Git en varios sistemas operativos

- **Git para Windows**: Descarga el instalador oficial para Windows.
- **Git para macOS**: Se puede instalar con Homebrew:  
  ```sh
  brew install git
  ```
- **Git para Linux**: Se puede instalar con el gestor de paquetes de la distribución. En Ubuntu:
  ```sh
  sudo apt-get install git
  ```

![Terminal Git](./img/terminalgit.png)

### GitHub

**GitHub** es una plataforma de alojamiento de código basada en Git. Permite a los desarrolladores almacenar y gestionar repositorios, colaborar en proyectos y realizar revisiones de código.

![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Logo.png)

### Problemas comunes al instalar Git

- **Configurar usuario y correo:**
  ```sh
  git config --global user.name "Tu Nombre"
  git config --global user.email "tu@email.com"
  ```
- **Problemas con SSH:** Es recomendable configurar una clave SSH para interactuar con repositorios remotos.

🚨 🚨 **¿Entendéis lo que necesitamos? ¿Entendéis el problema de la configuración inicial?** 🚨 🚨

---

## 3. Conceptos Fundamentales

![Conceptos Git](./img/conceptosgit.png)

📖 **Repositorio**: Espacio donde se almacena el código de un proyecto.

🖼️ **Commit**: Registro de cambios en el repositorio con un mensaje descriptivo y un identificador único (hash).

📦 **Rama (Branch)**: Línea de desarrollo independiente que permite trabajar en nuevas características sin afectar la rama principal.

💾 **Merge**: Proceso de combinar dos ramas.

📜 **Pull Request (PR)**: Solicitud para fusionar una rama con otra en GitHub.

🚨 🚨 **Metáfora del árbol** 🚨 🚨
- El **commit** es una hoja en una rama.
- La **rama** es una rama del árbol.

---

## 4. Flujo de Trabajo en Git

![Flujo de Trabajo Git](./img/flujogit.png)

### 4.1. Clonar un repositorio
```sh
git clone https://github.com/usuario/repositorio.git
```

### 4.2. Crear una nueva rama
```sh
git checkout -b nueva-rama
```

### 4.3. Hacer cambios y commit
```sh
git add .
git commit -m "Descripción de los cambios"
```

### 4.4. Subir cambios al repositorio remoto
```sh
git push origin nueva-rama
```

### 4.5. Crear un Pull Request
En GitHub, crea un Pull Request para fusionar tu rama con la rama principal.

### 4.6. Fusionar cambios
```sh
git checkout main
git merge nueva-rama
```

🚨 🚨 **¿Diferenciamos entre rama y commit? ¿Entendemos la función de un Pull Request?** 🚨 🚨

---

## 5. Comandos Esenciales

- **Inicializar un repositorio:**  
  ```sh
  git init
  ```
- **Clonar un repositorio:**  
  ```sh
  git clone <url>
  ```
- **Ver estado actual del repositorio:**  
  ```sh
  git status
  ```
- **Añadir archivos al área de preparación:**  
  ```sh
  git add <archivo>
  ```
- **Hacer un commit:**  
  ```sh
  git commit -m "mensaje"
  ```
- **Subir cambios al repositorio remoto:**  
  ```sh
  git push <remoto> <rama>
  ```
- **Descargar cambios del repositorio remoto:**  
  ```sh
  git pull <remoto> <rama>
  ```
- **Listar todas las ramas:**  
  ```sh
  git branch
  ```
- **Cambiar de rama:**  
  ```sh
  git checkout <rama>
  ```
- **Fusionar ramas:**  
  ```sh
  git merge <rama>
  ```
- **Ver historial de commits:**  
  ```sh
  git log
  ```
- **Ver diferencias entre archivos:**  
  ```sh
  git diff
  ```
- **Deshacer cambios en el área de preparación:**  
  ```sh
  git reset
  ```
- **Guardar cambios temporalmente:**  
  ```sh
  git stash
  ```
- **Crear una etiqueta:**  
  ```sh
  git tag
  ```

🚨 🚨 **¿Me suenan los comandos esenciales?** 🚨 🚨
