# DevOps Backend Despachos - Innovatech Chile

## Descripción

Este repositorio contiene el microservicio Backend de Despachos del proyecto Innovatech Chile.

El servicio fue desarrollado con Spring Boot y Java 17. Está contenedorizado mediante Docker, se ejecuta en una instancia EC2 privada de AWS y utiliza una base de datos MySQL en contenedor con persistencia mediante volúmenes Docker.

## Tecnologías utilizadas

- Java 17
- Spring Boot
- Maven
- Spring Data JPA
- MySQL
- Docker
- Docker Compose
- GitHub Actions
- Docker Hub
- AWS EC2

## Arquitectura del servicio

El microservicio de despachos se ejecuta en la instancia Backend privada. No se expone directamente a Internet.

La comunicación se realiza desde la instancia Frontend pública hacia la instancia Backend privada.

```text
EC2 Frontend pública
        |
        v
EC2 Backend privada
        |
        ├── back-despachos-app
        └── mysql-despachos
