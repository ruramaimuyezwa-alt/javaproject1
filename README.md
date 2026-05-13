# Task 1 — First Spring Boot Project

A basic Spring Boot MVC application demonstrating Spring controllers,
@ResponseBody annotation, and Thymeleaf templates.

## Tech Stack
- Java 21
- Spring Boot 4.0.5
- Spring MVC
- Thymeleaf
- Lombok
- Maven

## How to Run

1. Open the project in IntelliJ IDEA
2. Right-click pom.xml → Maven → Reload Project
3. Run Task1Application.java
4. The app starts on *http://localhost:8080*

## Endpoints

### GET /
Returns a plain text greeting directly in the HTTP response body.

- *Method:* GET
- *URL:* http://localhost:8080/
- *Response:* Hello Vistula, in my first Spring controller.

*How it works:*
The @GetMapping("/") annotation maps this URL to the hello() method.
The @ResponseBody annotation tells Spring to write the returned
String directly into the HTTP response body instead of looking
for a Thymeleaf template.

### GET /greeting
Returns an HTML page rendered by Thymeleaf with a personalized greeting.

- *Method:* GET
- *URL:* http://localhost:8080/greeting?name=Vistula
- *Optional param:* name (default value is World)
- *Response:* HTML page displaying "Hello, Vistula!"

*How it works:*
The @RequestParam annotation reads the name query parameter from
the URL. The Model object passes the name value to the Thymeleaf
template. The method returns the string "greeting" which tells
Thymeleaf to look for greeting.html in the templates folder.

## Project Structure