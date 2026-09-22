# Product Service

Spring Boot REST API for product management.

## Technologies
- Java 17
- Spring Boot 4.1.1
- Spring Web
- Spring Data MongoDB
- MongoDB
- Testcontainers
- JUnit 5
- Maven

## Endpoints

| Method | Endpoint | Purpose |
|---|---|---|
| POST | `/api/products` | Create product |
| GET | `/api/products` | Get all products |
| GET | `/api/products/{id}` | Get product by ID |
| PUT | `/api/products/{id}` | Update product |
| DELETE | `/api/products/{id}` | Delete product |

## Example POST body

```json
{
  "name": "Laptop",
  "description": "Development laptop",
  "price": 65000.00
}
```

## Run

Start MongoDB locally on port 27017, then:

```bash
mvn spring-boot:run
```

Application URL:

`http://localhost:8082`

## Tests

Docker must be running because Testcontainers starts MongoDB automatically for the integration tests.

```bash
mvn test
```
