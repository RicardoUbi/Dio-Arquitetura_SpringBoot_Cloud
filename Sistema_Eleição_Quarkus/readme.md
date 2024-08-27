# Desenvolvendo um Sistema para Eleição Usando Quarkus Framework

Neste projeto, desenvolvemos um Sistema para Eleições utilizando o framework Quarkus. O objetivo geral desse projeto foi entender na prática um pouco de como funciona o desenvolvimento de um sistema, desde a escolha da Arquitetura até as melhores práticas de Testes.

## Funcionalidades do projeto

- Candidatos são listados, cadastrados e editados
- Todos os candidatos registrados participam de uma eleição, quando for iniciada
- Candidatos recebem votos de eleitores
- Resultado disponível em tempo real

## Tecnologias Utilizadas

* **Backend:** Java, Quarkus, Hibernate
* **Banco de dados:** MariaDB, Redis
* **Contêineres:** Docker, Docker Compose
* **Orquestração:** Traefik
* **Logging:** Graylog
* **Tracing:** Jaeger
* **Testes:** JUnit, Testcontainers

## Arquitetura escolhida

O sistema segue a arquitetura Onion, com uma clara separação de responsabilidades entre as camadas:

    src/
    ├── api/
    │   └── Expor a API RESTful para interação com o sistema.
    ├── domain/
    │   └── Contém a lógica de negócio do sistema, como os modelos de entidades (Candidato, Voto) e os serviços (Cadastro de Candidato, Contagem de Votos).
    ├── infrastructure/
    │   └── Contém detalhes de implementação, como acesso ao banco de dados e etc.
    ├── test/
    │   └── Contém a lógica para realizar testes unitários e de integração.

## Próximos Passos:

- **(Developer)** Adicione métricas nas aplicações usando Grafana como dashboard 
- **(Developer)** Finalize a implementação do gerenciamento de candidatos no election-management
    - Remoção, Listagem com Paginação
- **(Developer)** Substitua o gerenciamento de candidatos por REST Data with Panache
- **(Developer)** Implemente alterações no código para tornar as aplicações mais reactivas/assíncrona
- **(DevOps)** Provisione uma réplica de leitura do banco de dados, habilitando múltiplas conexões nos repositories
- **(DevOps)** Planeje a migração desse sistema para um ambiente Kubernetes
- **(DevSecOps)** Planeje um processo de Modelagem de Ameaças considerando técnicas de detecção e prevenção de DDoS
- **(Architect)** Documente ADRs para: 
    - Evitar múltiplos votos de uma mesma origem 
    - Detecção de fraude incluindo auditoria
- **(Data Scientist)** Modele um workflow para Análise Preditiva do resultado da eleição.
- **(Product Owner)** Crie um roadmap com novas funcionalidades

## Considerações finais

Em geral, este projeto foi uma excelente oportunidade para aprofundar os conhecimentos em arquitetura de software, testes unitarios e de integração e ferramentas de desenvolvimento. O conteúdo foi tão rico em conhecimento, que tenho certeza que sempre que rever este projeto, aprenderei mais.

Se você quiser mais informações sobre o desenvolvimento deste sistema, pode acessar este PDF explicativo feito pelo Autor/Instrutor deste projeto [Thiago Poiani](https://www.linkedin.com/in/thpoiani/).

[Desenvolvendo um Sistema para Eleição Usando Quarkus Framework .pdf](https://academiapme-my.sharepoint.com/personal/renato_dio_me/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Frenato%5Fdio%5Fme%2FDocuments%2FDigital%20Innovation%20One%2Fslides%20aulas%20diversas%2FDesenvolvendo%20um%20Sistema%20para%20Elei%C3%A7%C3%A3o%20Usando%20Quarkus%20Framework%2FAula%20%2D%20Desenvolvendo%20um%20Sistema%20para%20Elei%C3%A7%C3%A3o%20Usando%20Quarkus%20Framework%20%2Epdf&parent=%2Fpersonal%2Frenato%5Fdio%5Fme%2FDocuments%2FDigital%20Innovation%20One%2Fslides%20aulas%20diversas%2FDesenvolvendo%20um%20Sistema%20para%20Elei%C3%A7%C3%A3o%20Usando%20Quarkus%20Framework&ga=1)

## Divirta-se!