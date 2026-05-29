# Proyecto Semestral Frontend

## Descripción

Frontend desarrollado en React para el sistema de gestión de ventas y despachos.

La aplicación permite interactuar con los servicios backend desplegados en AWS, consumiendo las APIs de Ventas y Despacho mediante una interfaz web.

## Tecnologías Utilizadas

* React
* JavaScript
* Docker
* Docker Compose
* GitHub Actions
* Docker Hub
* AWS EC2

## Arquitectura

El frontend se ejecuta en una instancia EC2 Web dentro de AWS y se encuentra dockerizado mediante Docker.

Contenedor utilizado:

* frontend-despacho

Imagen Docker:

* bertasotoj/despacho-frontend

Puerto utilizado:

* 80

## Ejecución Local

### Clonar repositorio

```bash
git clone https://github.com/BertaSoto/proyecto-semestral-frontend.git
cd proyecto-semestral-frontend
```

### Ejecutar con Docker Compose

```bash
docker compose up -d
```

### Acceder a la aplicación

```text
http://localhost
```

## Pipeline CI/CD

Cada push realizado sobre la rama deploy ejecuta automáticamente:

1. Build de la imagen Docker.
2. Publicación en Docker Hub.
3. Despliegue automático en AWS EC2 mediante GitHub Actions.

## Autoras

* Daniela Gómez Palacios
* Berta Soto Jerez