# Desafío 2 - Jenkins Webhook y Node.js API

## Descripción

Este proyecto tiene como objetivo configurar un webhook en un repositorio de GitHub y crear un pipeline en Jenkins para automatizar el proceso de build y testing de una API en Node.js.

## Requisitos

- Cuenta en GitHub.
- Jenkins instalado y configurado.
- Ngrok para exponer Jenkins públicamente.
- Node.js y NPM instalados.
- Proyecto de ejemplo: `nodejs-helloworld-api`.

## Configuración

### 1. Forkear el Repositorio

- Ir al repositorio original: [nodejs-helloworld-api](https://github.com/).
- Hacer un fork a tu cuenta de GitHub.

### 2. Configurar Webhook en GitHub

- Ir a `Settings` → `Webhooks` en tu fork.
- Crear un nuevo webhook:
  - **Payload URL**: `http://<tu-ngrok-url>/github-webhook/`
  - **Content Type**: `application/json`
  - **Eventos**: Seleccionar "Push" y "Pull request".
- Guardar los cambios.

### 3. Exponer Jenkins con Ngrok

- Descargar e instalar ngrok desde [ngrok.com](https://ngrok.com/).
- Abrir una terminal y ejecutar:

  ```bash
  ngrok http 8080
