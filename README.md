# Java-REST-API-

# Project Structure
- Create a new Spring Boot project named ecommerce-store-api with the following package structure:

ecommerce-store-api/
* ecommerce-store-api/
  * src/
    * main/
      * java/
        * com/
          * example/
            * ecommercestoreapi/
              * config/
                * SecurityConfig.java
                * WebConfig.java
              * controller/
                * CategoryController.java
                * ProductController.java
              * dto/
                * CategoryDTO.java
                * ProductDTO.java
              * entity/
                * Category.java
                * Product.java
              * repository/
                * CategoryRepository.java
                * ProductRepository.java
              * service/
                * CategoryService.java
                * ProductService.java
              * util/
                * ResponseUtil.java
      * resources/
        * static/
        * templates/
        * application.properties
      * test/
        * java/
          * com/
            * example/
              * ecommercestoreapi/
                * controller/
                  * CategoryControllerTest.java
                  * ProductControllerTest.java
                * service/
                  * CategoryServiceTest.java
                  * ProductServiceTest.java
    * target/
  * pom.xml



## Configuration Files

### application.properties:
- Database connection properties
- Server port configuration
- Logging settings
- Swagger UI configurations
- CORS settings
### pom.xml (if using Maven):
- Project dependencies (Spring Web, Spring Data JPA, etc.)
- Build configurations
- Dependencies for validation, Swagger, H2 database
## Entity Package
### Product.java:
* Define Product entity class
* Add @Entity annotation
* Include fields: id, name, price, availability, category
* Implement getters and setters
* Override toString() method
* Add validation annotations (@NotNull, etc.)
### Category.java:
* Define Category entity class
* Add @Entity annotation
* Include fields: id, categoryName, description, imageUrl
* Implement getters and setters
* Override toString() method
* Add validation annotations
##Repository Package
### ProductRepository.java:
Extend JpaRepository interface
Define custom query methods for product operations
Add @Repository annotation
### CategoryRepository.java:
Extend JpaRepository interface
Define custom query methods for category operations
Add @Repository annotation
## Service Package
### ProductService.java:
Implement business logic for product management
Methods for CRUD operations
Validation checks
Autowire ProductRepository
Add @Service annotation
### CategoryService.java:
Implement business logic for category management
Methods for CRUD operations
Validation checks
Autowire CategoryRepository
Add @Service annotation
## DTO Package
### ProductDTO.java:
Define data transfer object for product
Include fields: id, name, price, availability, categoryId
Implement constructors and getter/setter methods
Add validation annotations
### CategoryDTO.java:
Define data transfer object for category
Include fields: id, categoryName, description, imageUrl
Implement constructors and getter/setter methods
Add validation annotations
## Controller Package
### ProductController.java:
* Handle HTTP requests for product endpoints
* Implement RESTful API endpoints for CRUD operations
* Use ResponseEntity for proper HTTP responses
* Autowire ProductService and CategoryService
* Add @RestController and @RequestMapping annotations
### CategoryController.java:
* Handle HTTP requests for category endpoints
* Implement RESTful API endpoints for CRUD operations
* Use ResponseEntity for proper HTTP responses
* Autowire CategoryService
* Add @RestController and @RequestMapping annotations
## Utility Package
### ResponseUtil.java:
* Helper methods for creating consistent API responses
* Method to create ApiResponse objects
### WebConfig.java:
* Configure CORS settings
* Add @Configuration annotation

## Main Application Class
### EcommerceStoreApiApplication.java:
* Main application class with @SpringBootApplication annotation
* Entry point for the Spring Boot application

## Security Configuration (Optional)
### SecurityConfig.java:
* Configure security settings for the API
* Implement authentication and authorization
* Add @EnableWebSecurity annotation

  # Order of Building :
- Main Application Class
- Core Packages
- Configuration Files
- Entities
- Repositories
- Service Layer
- DTOs
- Controllers
- Utility Classes
- Resource Classes
- Testing/POM.xml
