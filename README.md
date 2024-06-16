# MICROSERVICES
## Description
Microservices practice project

## Diagram
```mermaid
flowchart LR

  AG[API Gateway]
  RS[Registry and Discovery]
  CS[Configuration Service]
  CR[Configurations repository]
  subgraph MS[Microservicios]
    direction TB
  end

  subgraph DB[Database]
    direction TB
  end

  AG <-- Registers --> RS
  AG <--> MS
  MS <-- Registers --> RS
  MS <--> CS
  MS <--> DB
  CS <--> CR
  

  click RS "https://github.com/SaulMMBP/microservices-registry-service" _blank
  click AG "https://github.com/SaulMMBP/microservices-gateway-service" _blank
  click CS "https://github.com/SaulMMBP/microservices-config-server" _blank

```
