## Micro serviço de pagamento implementado com nodejs por meio do framework NestJS

Endpoint disponível: (POST) /credit-card/send

```json
{
	id?: "",
	idUser: "213Fee43",
	orderNumber: 1000,
	orderValue: 300,
	paymentConfirmed?: false
}
```

Serviços necessários para funcionamento do projeto

- DB Postgres
- RabbitMQ

Comando para iniciar os serviços com docker

```jsx
docker-compose -f docker/docker-compose.rabbitmq.yml -f docker/docker-compose.postgres.yml up -d
```

Micro serviço utilizado para envio de notificações no projeto: https://github.com/sidney-essjr/ms-notification-service 

Bibliotecas utilizadas

```jsx
npm install @nestjs/microservices amqplib
npm install amqp-connection-manager
npm install @nestjs/config
npm install prisma --save-dev
npm install @prisma/client
```
