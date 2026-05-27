# Frontend Despacho

Aplicación frontend desarrollada con React + Vite para el sistema de despacho de Innovatech Chile.

## Tecnologías
- React + Vite
- Nginx (producción)
- Docker (multi-stage build)

## Requisitos
- Docker Desktop instalado
- Node.js 20+

## Cómo ejecutar localmente

### Con Docker
`ash
docker build -t frontend-despacho .
docker run -p 80:80 frontend-despacho
`
Acceder en: http://localhost

### Con docker-compose
`ash
docker-compose up
`

## Pipeline CI/CD
El pipeline se activa automáticamente con cada push a la rama deploy:
1. Construye la imagen Docker
2. Publica en Docker Hub
3. Despliega en EC2 (IP: 3.90.105.128)

## Estructura del proyecto
- src/ - Código fuente React
- Dockerfile - Configuración Docker multi-stage
- .github/workflows/deploy.yml - Pipeline CI/CD
