# 👷‍♂️⚒ work in progress 👨‍🏭🛠
## Order Management Microservice 🥙

### Overview
A order management microservice project for a food chain distributing shawarmas to thousands of people. Highly scalable microservices with low latency communications and high availability with concurrent processing.

Gateway => Orders => Orders Service => Inventory (stock management) => Inventory Service => Payments => Payments Service

Order Service  
- Validate order details (talk with stock service)
- CRUD of orders
- Initiates Payment flow (by sending an event)

Stock Service 
- Handles stock
- Validates order quantities.
- Returns items as menu

Menu Service   
- Handles menu
- Returns menu items

Payment Service
- Initiates payment with 3rd party provider
- Produces an order Paid/Cancelled event to (orders / stock and kitchen)


### Tools

- Go 1.22 or higher.
- Golang cosmtrek / air for hot-reloading.
- gRPC for communication between services.
- RabbitMQ for message broker.
- Docker with docker compose.
- MongoDb as storage layer.
- jaeger for Service tracing.
- Hashicorp consul for service discovery.
- Stripe for payments.


