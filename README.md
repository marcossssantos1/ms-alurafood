microservices-spring-alurafood
Este é um projeto de exemplo de um sistema de pedidos de comida, implementado com arquitetura de microservices, utilizando Spring Cloud e Docker. O projeto foi desenvolvido como parte do curso Microservices with Spring Cloud oferecido pela Alura.

Tecnologias Utilizadas

O projeto utiliza as seguintes tecnologias e frameworks:

Java Version Spring Boot Version
Spring Cloud Version Spring Cloud Eureka Server Version Spring Cloud Eureka Client Version Spring Cloud Openfeign Version
Lombok Version
ModelMapper Version
Resilience4j Version
Docker Version Docker Compose Version
MySql Version Flyway Version
Arquitetura de Microservices

O projeto utiliza a arquitetura de microservices, com os seguintes serviços:

server: servidor de descoberta de serviços, para que os serviços possam se comunicar entre si
gateway: serviço responsável por fazer o roteamento das requisições entre os serviços
pedidos: serviço responsável por gerenciar os pedidos
pagamentos: serviço responsável por gerenciar os pagamentos
Banco de Dados
O projeto utiliza o MySQL como banco de dados. Cada serviço possui seu próprio banco de dados.

O arquivo docker-compose.yml na raiz do projeto contém a definição dos serviços e suas dependências. O arquivo também configura as variáveis de ambiente necessárias para cada serviço.

Os serviços estarão disponíveis nos seguintes endereços:

Discovery Server - Eureka: http://localhost:8761
Gateway: http://localhost:8082
Pagamentos: http://localhost:8082/pagamentos-ms/pagamentos
Pedidos: http://localhost:8082/pedidos-ms/pedidos

Postman Collection
A coleção alurafood na raíz do projeto contém as seguintes requisições:

pagamentos: lista todos os pagamentos cadastrados.
pagamentos-por-id: retorna um pagamento específico, com base em seu ID.
criar-pagamento: cria um novo pagamento.
atualizar-pagamento: atualiza um pagamento existente.
deletar-pagamento: deleta um pagamento existente.
confirmar-pagamento: confirma um pagamento existente.
pedidos: lista todos os pedidos cadastrados.
pedidos-por-id: retorna um pedido específico, com base em seu ID.
criar-pedido: cria um novo pedido.
atualizar-status-pedido: atualiza o status de um pedido existente.
porta-pedidos-ms: retorna qual a porta de origem do serviço retornado da requisição.
