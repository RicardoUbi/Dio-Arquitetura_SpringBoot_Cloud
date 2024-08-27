# election-management

Este projeto utiliza o Quarkus, o Supersonic Subatomic Java Framework.

Se você quiser saber mais sobre o Quarkus, por favor visite seu site: https://quarkus.io/.

## Executando a aplicação em modo de desenvolvimento

Você pode executar sua aplicação em modo de desenvolvimento, o que habilita codificação ao vivo, usando:
```shell script
./mvnw compile quarkus:dev
```

> **OBS:** O Quarkus agora vem com uma Dev UI, que está disponível somente em modo de desenvolvimento em http://localhost:8080/q/dev/.

## Empacotando e executando a aplicação

A aplicação pode ser empacotada usando:
```shell script
./mvnw package
```
Isso produz o arquivo `quarkus-run.jar` no diretório `target/quarkus-app/`.
Note que não é um _über-jar_, pois as dependências são copiadas para o diretório `target/quarkus-app/lib/`.

A aplicação agora pode ser executada usando `java -jar target/quarkus-app/quarkus-run.jar`.

Se você quiser criar um _über-jar_, execute o seguinte comando:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

A aplicação, empacotada como um _über-jar_, agora pode ser executada usando `java -jar target/*-runner.jar`.

## Criando um executável nativo

Você pode criar um executável nativo usando:
```shell script
./mvnw package -Pnative
```

Ou, se você não tiver o GraalVM instalado, pode executar a construção do executável nativo em um container usando:
```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

Você pode então executar seu executável nativo com: `./target/election-management-1.0.0-SNAPSHOT-runner`

Se você quiser saber mais sobre como construir executáveis nativos, por favor consulte https://quarkus.io/guides/maven-tooling.

## Guias Relacionados

- Logging GELF ([guia](https://quarkus.io/guides/centralized-log-management)): Faça logs usando o formato Graylog Extended Log Format e centralize seus logs em ELK ou EFK
- SmallRye Health ([guia](https://quarkus.io/guides/microprofile-health)): Monitore a saúde do serviço
- SmallRye Context Propagation ([guia](https://quarkus.io/guides/context-propagation)): Propague contextos entre threads gerenciadas em aplicações reativas
- RESTEasy Reactive ([guia](https://quarkus.io/guides/resteasy-reactive)): Uma implementação de JAX-RS utilizando processamento em tempo de build e Vert.x. Esta extensão não é compatível com a extensão quarkus-resteasy, ou com quaisquer extensões que dependem dela.
- OpenTelemetry ([guia](https://quarkus.io/guides/opentelemetry)): Use o OpenTelemetry para rastrear serviços