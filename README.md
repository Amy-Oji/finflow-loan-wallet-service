# **Finflow Loan Wallet Service**

A backend Spring Boot service for managing customer loan wallets, loan limits, wallet transactions, and loan balance operations. 
This service is designed with clean architecture principles and can be integrated with fintech applications, mobile banking platforms, or loan decisioning systems.

---

## **Features**

* Create and manage customer loan wallets
* Check loan eligibility and limits
* Process loan top-ups, deductions, and repayments
* Track wallet transaction history
* Validate wallet balance before transactions
* Integrate with external services (payments, loan decisioning)
* RESTful API design
* Follows layered architecture (Controller → Service → Repository)

---

## **Tech Stack**

* **Java 17+**
* **Spring Boot 3**
* **Spring Web**
* **Spring Data JPA**
* **PostgreSQL**
* **Lombok**
* **Jakarta Validation**
* **Maven**

---

## **Architecture**

```
src/
 └── main/
     ├── java/
     │    └── com.ammie.finflow.wallet
     │         ├── controller/
     │         ├── service/
     │         ├── service/impl/
     │         ├── repository/
     │         ├── entity/
     │         └── dto/
     └── resources/
          ├── application.properties
          └── data.sql (optional)
```

---

## **API Endpoints (Summary)**

| Method | Endpoint                                    | Description                    |
| ------ | ------------------------------------------- | ------------------------------ |
| `POST` | `/api/v1/wallets`                           | Create customer loan wallet    |
| `GET`  | `/api/v1/wallets/{customerId}`              | Fetch customer wallet details  |
| `POST` | `/api/v1/wallets/topup`                     | Increase wallet loan balance   |
| `POST` | `/api/v1/wallets/debit`                     | Debit wallet for loan payments |
| `GET`  | `/api/v1/wallets/{customerId}/transactions` | Wallet transaction history     |

---

## **Setup Instructions**

### **1. Clone the Repository**

```
git clone https://github.com/yourusername/finflow-loan-wallet-service.git
cd finflow-loan-wallet-service
```

### **2. Configure Database**

Update `src/main/resources/application.properties`:

```
spring.datasource.url=jdbc:postgresql://localhost:5432/finflow
spring.datasource.username=postgres
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
```

### **3. Run the App**

```
./mvnw spring-boot:run
```

---

## **Future Enhancements**

* Add JWT authentication
* Support for loan scoring engine integration
* Add pagination to wallet transactions
* Implement soft deletes
* Add Swagger/OpenAPI documentation

---

## **Author**

**Amarachukwu Ojiakor**
Backend Engineer | Java | Spring Boot
