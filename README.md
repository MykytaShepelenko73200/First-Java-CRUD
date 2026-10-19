# First-Java-CRUD

A simple CRUD app for customers, built with Spring Boot, Spring Data JPA, Vaadin and an in-memory H2 database.
It is based on the guide [Creating CRUD UI with Vaadin](https://spring.io/guides/gs/crud-with-vaadin/).

## Run

Requires JDK 21 or newer. Maven doesn't need to be installed because the wrapper is included.

```sh
./mvnw spring-boot:run
```

Then open http://localhost:8080. The app starts with five demo customers. You can:

- **Create** a customer with "New customer", fill in the names, then click Save.
- **Read** the customers in the grid, and filter them by last name.
- **Update** a customer by selecting a row, editing it, then clicking Save.
- **Delete** a customer by selecting a row and clicking Delete.

Data is kept in memory, so it resets each time the app restarts.

## Code

| File | Role |
|------|------|
| `Customer.java` | JPA entity |
| `CustomerRepository.java` | Spring Data repository with a last-name filter query |
| `MainView.java` | Main page: filter field, "New customer" button and grid |
| `CustomerEditor.java` | Form for saving, cancelling and deleting |
| `CrudwithvaadinApplication.java` | Entry point; loads the demo data |
