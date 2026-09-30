# 🖥️ Configuración del entorno local y documentación del proyecto

<div align="center">

🚀 Proyecto `misitio`

Documentación del proceso de instalación, configuración y puesta en marcha del sitio web local

---

📦 Git · 🔧 GitHub CLI · 🐘 PHP 8.4 · 🏠 Herd · 🌐 HTTPS · 📚 Read the Docs

</div>

---

## 📖 Introducción

En esta documentación se recoge paso a paso el proceso necesario para preparar
un entorno de desarrollo local desde cero y poner en funcionamiento el sitio
web **`misitio`**.

El objetivo es documentar todo el proceso, desde la instalación de las
herramientas necesarias hasta conseguir que el proyecto esté disponible
localmente mediante **HTTPS**.

La documentación está pensada para que cualquier persona que parta de un
equipo sin las herramientas necesarias pueda seguir los pasos y reproducir
el entorno.

---

## 🎯 Objetivos

Durante el proceso se realizan las siguientes tareas:

- 🧰 Instalar y configurar **Git**.
- 🐙 Instalar y autenticar **GitHub CLI**.
- 🏠 Instalar **Herd** como entorno de desarrollo local.
- 🐘 Configurar **PHP 8.4**.
- 📦 Clonar el repositorio **`misitio`** en el equipo local.
- 🔗 Enlazar el proyecto con **Herd**.
- 🔒 Configurar el proyecto para utilizar **HTTPS**.
- 🌐 Comprobar que el sitio funciona correctamente en el navegador.
- 📚 Documentar y publicar el proceso mediante **Read the Docs**.

---

## 🛠️ Herramientas utilizadas

| Herramienta | Función |
| :---: | --- |
| 🧰 **Git** | Control de versiones del proyecto |
| 🐙 **GitHub CLI** | Interacción con GitHub desde la terminal |
| 🏠 **Laravel Herd** | Entorno de desarrollo local |
| 🐘 **PHP 8.4** | Lenguaje y versión utilizada por el proyecto |
| 🌐 **HTTPS** | Acceso seguro al sitio web local |
| 📝 **Markdown** | Lenguaje utilizado para escribir la documentación |
| 📚 **MkDocs** | Generador de la documentación |
| 🎨 **Material for MkDocs** | Tema visual de la documentación |
| ☁️ **Read the Docs** | Plataforma utilizada para publicar la documentación |

---

## 🔄 Proceso de instalación

El proceso completo sigue el siguiente recorrido:

    A[🧰 Git] --> B[🐙 GitHub CLI]
    B --> C[🏠 Herd]
    C --> D[🐘 PHP 8.4]
    D --> E[📦 Clonar misitio]
    E --> F[🔗 Enlazar con Herd]
    F --> G[🔒 Activar HTTPS]
    G --> H[🌐 misitio.test]
    H --> I[📚 Read the Docs]
