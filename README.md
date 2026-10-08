# Práctica 1.1 — Primeros endpoints y estructura inicial

## 1. Objetivo

El objetivo de esta práctica es crear una API inicial utilizando
FastAPI, configurar el entorno de desarrollo y comprobar la
documentación automática mediante Swagger.

## 2. Estructura del proyecto
<img width="225" height="233" alt="image" src="https://github.com/user-attachments/assets/378d4bde-89fe-412a-a0a0-be61f8406093" />

## 3. Entorno virtual

Se ha creado un entorno virtual mediante:

```bash
python -m venv venv
```
El entorno permite aislar las dependencias del proyecto.

## 4. Dependencias

Las dependencias utilizadas en el proyecto se encuentran definidas en el
archivo `requirements.txt`.

Las principales dependencias son:

- **FastAPI**: framework utilizado para desarrollar la API REST.
- **Uvicorn**: servidor ASGI utilizado para ejecutar la aplicación FastAPI.
- **Pydantic**: utilizado para definir y validar los modelos de respuesta.

Las dependencias se han instalado dentro del entorno virtual del proyecto
y sus versiones se encuentran fijadas en `requirements.txt`.

## 5. Endpoints

La aplicación dispone de tres endpoints funcionales:

### GET /health

Este endpoint permite comprobar el estado de la API.

**Respuesta:**

```json
{
  "status": "ok"
}
```
La aplicación dispone de tres endpoints funcionales:

### GET /health

Este endpoint permite comprobar el estado de la API.


**Respuesta:**

```json
{
  "status": "ok"
}
```

### GET /version

Este endpoint devuelve la versión actual de la API.

**respuesta**

```json
{
"status": "ok"
}
```
### GET /ping
Este endpoint permite comprobar que el servidor está respondiendo
correctamente.
**respuesta**
``` json
{
"message": "pong"
}
```
Los tres endpoints están documentados mediante summary, description
y response_model, por lo que aparecen correctamente definidos en la
documentación automática de Swagger (/docs).
## 6. Ejecución del servidor

Para iniciar el servidor de la aplicación se utiliza Uvicorn.

En primer lugar, se activa el entorno virtual del proyecto:

```bash
venv\Scripts\activate
```

A continuación, se inicia el servidor mediante el siguiente comando:

```bash
uvicorn app.main:app --reload
```

La opción `--reload` permite que el servidor se reinicie automáticamente cuando se realizan cambios en el código durante el desarrollo.

Una vez iniciado correctamente el servidor, la API queda disponible en:

```text
http://127.0.0.1:8000
```

La documentación automática de Swagger puede consultarse en:

```text
http://127.0.0.1:8000/docs
```

Desde Swagger se pueden consultar y probar los tres endpoints implementados:

- `GET /health`
- `GET /version`
- `GET /ping`

## 7. Documentación Swagger

<img width="225" height="253" alt="image" src="https://github.com/user-attachments/assets/88fadff3-85ef-4233-ab02-77ec8169d057"/>

La documentación automática permite consultar y probar los endpoints
de la API.

## 8. Control de versiones
El proyecto se ha gestionado mediante Git utilizando commits
descriptivos y separados por cambios funcionales.
