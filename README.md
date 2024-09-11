# Service Discovery - Spring Cloud Eureka

Este projeto é uma implementação básica de um **Service Discovery** usando **Spring Cloud Netflix Eureka**. O Service Discovery permite que os microsserviços registrem-se dinamicamente e descubram uns aos outros sem a necessidade de configuração manual dos endereços dos serviços. Também utilizamos um **API Gateway** para roteamento das requisições entre os microsserviços.

## Requisitos

- **Java 21** ou superior
- **Maven 3.6+**
- **Spring Boot 3.3.3+**

## Tecnologias Usadas

- **Spring Boot**
- **Spring Cloud Eureka Server**
- **Spring Cloud Eureka Client**
- **Spring Cloud Gateway**
- **Maven**

## Como Funciona

### Service Discovery (Eureka Server)

O **Eureka Server** é o serviço central onde os microsserviços se registram para serem descobertos por outros serviços. Ele mantém uma lista atualizada dos serviços disponíveis no sistema.

### Microsserviços (Eureka Clients)

Os microsserviços se registram no **Eureka Server** e são capazes de descobrir outros serviços registrados. Isso facilita a comunicação entre os serviços sem precisar conhecer os detalhes da infraestrutura.

### API Gateway

O **API Gateway** atua como um ponto de entrada unificado para as requisições aos microsserviços. Ele roteia as requisições de entrada para os serviços apropriados e pode ser usado para aplicar políticas como autenticação, autorização, limitação de taxa, etc.

## Configuração do Projeto

### Estrutura do Projeto

```bash
service-discovery/
├── service-discovery/     # Eureka Server
├── hello-api/            # Exemplo de microsserviço registrado no Eureka Server
├── ola-api/              # Outro microsserviço registrado no Eureka Server
└── api-gateway/          # API Gateway para gerenciar as requisições
