# About project
Trata-se de um projeto para a aplicação da arquitetura de microservices com Spring, em que neste será registro pedido, simulando uma gestão de pedidos e pagamento, tendo uma comunicação com o [PAYMENTS](https://github.com/valentin-juan/pagamentos)

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
[
    {
        "id": 1,
        "dataHora": "2023-10-12T20:50:50",
        "status": "REALIZADO",
        "itens": [
            {
                "id": 1,
                "quantidade": 10,
                "descricao": null
            },
            {
                "id": 2,
                "quantidade": 5,
                "descricao": null
            }
        ]
    }
]
```

### POST itens
`http://localhost:{gateway_port}/pedidos/pagamento`
Campos obrigatórios
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

Body completo
```json
{
  "id": 1,
  "dataHora": "2023-10-12T20:50:50.3394675",
  "status": "REALIZADO",
  "itens": [
    {
      "id": 1,
      "quantidade": 10,
      "descricao": null
    },
    {
      "id": 2,
      "quantidade": 5,
      "descricao": null
    }
  ]
}
```
### PUT
`http://localhost:{gateway_port}/pedidos/pagamento`

### DELETE
