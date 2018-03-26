# Discovery Server

Servidor Eureka de registro para microservicios.

1. Dependencias:
	* Cloud Discovery: Eureka Server.
	* Cloud Config: Config Client.
	* Actuator.

2. Anotar con *@EnableEurekaServer* la clase de configuración.

3. Renombrar *application.yml* por *bootstrap.yml* y agregar:
```[yml]
server:
  port: 8761
spring:
  application:
    name: discovery-server
eureka:
  client:
    register-with-eureka: false
    fetch-registry: false
```