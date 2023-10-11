# About project
Trata-se de um projeto para a aplicação da arquitetura de microservices com Spring, em que neste será registro pedido, simulando uma gestão de pedidos e pagamento, tendo uma comunicação com o [PAYMENTS](https://github.com/valentin-juan/payments)

---

## 👩‍💻 Technologies used
* Java 17
* Maven
* Spring Boot
* Spring Cloud
  * Eureka Server (Netflix)
  * Gateway
  * OpenFeign
* MySQL
* Flyway

---

## Requests examples

### GET
`http://localhost:{gateway_port}/pedidos/pedido`
* Response body
```json

```

### POST itens
`http://localhost:{gateway_port}/pedidos/pagamento`
```json
{
    "itens": [
    {
        "quantidade": 10,
        "descrição": "Coca-cola"
    },
    {
        "quantidade": 5,
        "descrição": "Mc Chicken"
    }
    ]
}
```
### PUT
`http://localhost:{gateway_port}/pedidos/pagamento`

### DELETE
