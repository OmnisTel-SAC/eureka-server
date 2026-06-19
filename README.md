# Eureka Server

Servidor de registro y descubrimiento de servicios del sistema OmnisTel.
Permite que los microservicios se encuentren entre sí dinámicamente
sin necesidad de direcciones IP fijas.

## Tecnologías

- Java 17
- Spring Boot 3.x
- Spring Cloud Netflix Eureka Server
- Spring Cloud Config Client
- OpenAPI / Swagger

## Estructura

```
eureka-server/
├── src/
│   ├── main/
│   │   ├── java/com/omnistel/eurekaserver/
│   │   │   └── EurekaServerApplication.java
│   │   └── resources/
│   │       ├── application.yml
│   │       └── bootstrap.yml
│   └── test/
│       └── java/.../eurekaserver/
│           └── EurekaServerApplicationTests.java
├── Dockerfile
├── pom.xml
└── .gitignore
```

## Patrones de Diseño

| Patrón | Descripción |
|--------|-------------|
| **Service Registry** | Registro centralizado de instancias de microservicios |
| **Service Discovery** | Descubrimiento dinámico de servicios sin IP fijas |
| **Heartbeat / Lease** | Renovación periódica de registro y expiración automática |

## Infraestructura

| Componente | Uso |
|------------|-----|
| **Eureka Server** | Registro y descubrimiento de todos los microservicios |

## Puerto

- `8761`

## Servicios Registrados

- `CONFIG-SERVER`
- `AUTH-SERVICE`
- `TICKET-SERVICE`
- `NOTIFICATION-SERVICE`
- `API-GATEWAY`

## Dependencias

- **Config Server** — configuración centralizada
