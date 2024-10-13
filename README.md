# Clean Architecture with Blazor Example

## Application Structure

![image](https://github.com/user-attachments/assets/7116147f-5950-402d-8c4e-251d8bf2adb8)

### Explanations of each part

#### Presentation (CleanArchitectureBlazorExample.WebUI.Client / CleanArchitectureBlazorExample.WebUI.Server)
Handles user interface and presentation logic. For Blazor, this includes your Razor components and pages. It's responsible for displaying data and capturing user input, passing it to the application layer for processing.

#### Application (CleanArchitectureBlazorExample.Application)
Defines business logic, rules, and workflows. It coordinates actions and orchestrates interaction between entities and services. This layer is independent of external frameworks.

#### Infrastructure Layer (CleanArchitectureBlazorExample.Infrastructure)
Implements data access, external API calls, and other external resources. It provides concrete implementations of interfaces (e.g., repositories, services) that the application layer depends on. This is where you interact with databases, file systems, etc.

#### Domain Layer (CleanArchitectureBlazorExample.Domain)
Contains the core business entities, logic, and rules (e.g., Task, User). It represents the business logic and rules, and is isolated from other layers. This layer should not depend on any infrastructure, UI, or database code.

## Entry Point
The entry point into the application (i.e. the startup project) for this project is the CleanArchitectureBlazorExample.WebUI.Server
