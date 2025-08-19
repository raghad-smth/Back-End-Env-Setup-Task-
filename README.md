# Spring Boot Practice Project

## 1. Setup

* **IDE:** Visual Studio Code
* **Installed Packages / Tools:**

  * Java 21
  * Spring Boot Extension Pack (Spring Tools)
* **API Testing Tool:** Postman

---

## 2. Needed Concepts

### Controller

* Responsible for handling HTTP requests and returning responses.
* Example:

```java
@RestController
public class HelloController {
    @GetMapping("/hello")
    public String sayHello() {
        return "Hello World";
    }
}
```

### Service

* Contains business logic of the application.
* Example:

```java
@Service
public class HelloService {
    public String getMessage() {
        return "Hello from Service";
    }
}
```

### Repository

* Handles database interactions (e.g., queries, saving, updating data).
* Example:

```java
@Repository
public interface UserRepository extends JpaRepository<User, Long> {}
```

### Model

* Represents the structure of data (entities).
* Example:

```java
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;
}
```

### Route

* Defined by annotations (`@GetMapping`, `@PostMapping`, etc.) inside the controller.
* Example:

```java
@GetMapping("/users")
public List<User> getAllUsers() { ... }
```

---

## 3. Practice Work

* Created a **simple Spring Boot project** with a single API endpoint.
* Implemented a controller that returns `"Hello World"`.
* Tested the endpoint using **Postman** by calling the route:

  * `GET http://localhost:8080/hello`
  * Response: `"Hello World"`
   
* Finally, pushed the project to **GitHub repository**.
* Pushed the Postman collection in the repo here as well.

---

