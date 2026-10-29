# 🤖 Bot de Telegram con n8n, Docker y Ngrok (Ainastibot)

Este repositorio contiene la arquitectura, configuraciones y documentación completa para desplegar e integrar un Bot de Telegram (**Ainastibot**) utilizando herramientas *open-source* como **n8n**, **Docker** y **Ngrok**.

## 📝 Descripción Corta (para la sección *About* de GitHub)

> **Descripción:**
> 🤖 Automatización y despliegue de un Bot de Telegram con n8n, Docker y Ngrok (Ainastibot) e integración de webhooks.

## 🚀 Componentes del Proyecto

* 🤖 **Bot de Telegram (Ainastibot):** Interacción automatizada y gestión de flujos mediante la API de Telegram.
* 🔄 **n8n:** Plataforma de automatización de flujos de trabajo (*workflow automation*) para procesar eventos e integrar servicios.
* 🐳 **Docker & Docker Compose:** Contenedorización de la instancia de n8n para garantizar portabilidad y facilidad de despliegue.
* 🌐 **Ngrok:** Creación de túneles HTTP/HTTPS seguros para la recepción local de *webhooks* de Telegram.

## 📁 Estructura del Repositorio

```text
Open-Source-n8n/
├── Manual De Usuario n8n.pdf   # Guía paso a paso de uso y configuración
└── n8n_docker.zip              # Archivos de Docker y flujos de n8n
```

## 🛠️ Tecnologías Utilizadas

* **n8n** (Motor de automatización)
* **Docker & Docker Compose**
* **Ngrok** (Túneles de red / Webhooks)
* **Telegram Bot API**

## 🚀 Instalación y Despliegue

Sigue estos pasos para desplegar la infraestructura en tu entorno local:

### 1. Clonar el Repositorio

```bash
git clone https://github.com/JuanAnd-coder/Open-Source-n8n.git
cd Open-Source-n8n
```

### 2. Descomprimir los Recursos de Docker

Descomprime el archivo de configuración en la raíz del proyecto:

```bash
# En Windows (PowerShell)
Expand-Archive -Path n8n_docker.zip -DestinationPath .

# En Linux / macOS
unzip n8n_docker.zip
```

### 3. Iniciar el Servidor de n8n con Docker

Asegúrate de tener **Docker Desktop** activo y ejecuta:

```bash
docker-compose up -d
```

n8n quedará disponible en tu navegador en `http://localhost:5678`.

### 4. Exponer n8n con Ngrok (para Webhooks)

Para que Telegram pueda enviar mensajes a tu servidor local de n8n, abre una nueva terminal e inicia Ngrok:

```bash
ngrok http 5678
```

Copia la URL pública en HTTPS generada por Ngrok (ejemplo: `https://abcd-123.ngrok-free.app`) para configurarla en los nodos *Webhook* de n8n.

### 5. Documentación y Configuración del Bot

Para el paso a paso detallado sobre la creación del token en *BotFather* y la importación de los flujos de trabajo en n8n, consulta el archivo **`Manual De Usuario n8n.pdf`** incluido en este repositorio.

## 👤 Autor

Desarrollado por **Juan Andrés Cárdenas** ([@JuanAnd-coder](https://github.com/JuanAnd-coder)).
