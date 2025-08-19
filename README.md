# How it Works

A fully implemented **RESTful Web API** built with **C# and ASP.NET (.NET 8)** to manage employee records. It handles all CRUD operations (Create, Read, Update, Delete) through well-defined endpoints, with built-in validation, documentation, and a clean architecture.

---

## Setting up the API

I created the project as an **ASP.NET Web API solution** in Visual Studio (`EmployeeAdminPortal.sln`):contentReference[oaicite:0]{index=0}. Using the built-in templates for .NET 8, I scaffolded controllers and services to manage employee data in memory (or a database, if extended).

---

## Defining the architecture

- **Controllers** → Exposed REST endpoints for `/employees`, handling CRUD requests.  
- **Models** → Defined strongly typed `Employee` objects with fields like `Id`, `Name`, `Email`, `Department`.  
- **Routing** → Configured attribute routing (`[HttpGet]`, `[HttpPost]`, `[HttpPut]`, `[HttpDelete]`) for clear endpoint mapping.  
- **Dependency Injection** → Registered services in `Program.cs` to manage employee data.  
- **Data Annotations** → Applied `[Required]`, `[EmailAddress]`, and `[StringLength]` attributes to enforce validation rules automatically.  

This separation followed **clean architecture principles**, ensuring that logic, validation, and endpoints were modular and testable.

---

## CRUD functionality

The API exposed the following endpoints:

- **GET /employees** → Retrieve all employees.  
- **GET /employees/{id}** → Retrieve a single employee by ID.  
- **POST /employees** → Create a new employee record.  
- **PUT /employees/{id}** → Update an existing employee record.  
- **DELETE /employees/{id}** → Remove an employee from the system.  

Each operation returned **JSON responses**, making the API easily consumable by frontends or other services.

---

## Testing & Documentation

I integrated **Swagger UI** for interactive testing and API documentation. This allowed me to:  

- Test each endpoint directly in the browser without external tools.  
- View request/response schemas automatically generated from my models.  
- Share a self-documented API with any potential frontend or developer.  

---

## What this project demonstrates

- **RESTful API design** → Proper use of HTTP verbs and status codes.  
- **Scalability** → Built on ASP.NET Core with .NET 8, ready to integrate with databases or authentication.  
- **Clean architecture** → Separation of concerns between models, controllers, and services.  
- **Validation-first design** → Used C# data annotations to enforce input quality at the API layer.  
