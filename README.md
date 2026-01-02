# ASP.NET Core Web API – Clean Architecture

## Overview
This project demonstrates an enterprise-grade ASP.NET Core Web API built using **Clean Architecture principles**.  
The objective is to create a maintainable, scalable, and testable application by enforcing a clear separation of concerns across layers.

The solution follows modern software engineering practices and is suitable for building backend systems or integrating with Single Page Applications (SPA) such as Angular or React.

## Project Goals
- Apply Clean Architecture in real-world applications
- Build scalable and maintainable backend services
- Follow Software Development Life Cycle (SDLC) best practices
- Design enterprise-ready Web APIs using ASP.NET Core

## Technology Stack
- ASP.NET Core
- C#
- Entity Framework Core
- SQL Server / PostgreSQL / SQLite
- RESTful Web APIs
- Git

Optional (for SPA integration):
- Angular
- React

## Architecture Overview
The solution is structured into multiple layers:
- **Domain** – Core business entities and rules
- **Application** – Use cases, business logic, and validation
- **Infrastructure** – Database access and external services
- **Web/API** – API endpoints and request handling

This structure ensures low coupling and high maintainability.

## Getting Started

### Prerequisites
To build and run this project, ensure you have:
- .NET SDK (latest version)
- Node.js (LTS version – only required for Angular/React)

### Installation
Install the Clean Architecture solution template:
```bash
dotnet new install Clean.Architecture.Solution.Template

Create a new solution using the template:

ASP.NET Core Web API only

dotnet new ca-sln -cf None -o YourProjectName


Angular + ASP.NET Core

dotnet new ca-sln --client-framework Angular --output YourProjectName


React + ASP.NET Core

dotnet new ca-sln -cf React -o YourProjectName

Run the Application
cd src/Web
dotnet run

Use Case Generation

The template supports structured creation of commands and queries inside the Application layer.

Create a command

dotnet new ca-usecase --name CreateEntity --feature-name FeatureName --usecase-type command


Create a query

dotnet new ca-usecase -n GetEntities -fn FeatureName -ut query


This approach encourages clean, testable business logic.

Database Support

Supported databases:

SQL Server (default)

PostgreSQL

SQLite

During development, the database is:

Automatically deleted

Recreated from the model

Seeded with sample data

This helps maintain consistency during early development.
For production environments, EF Core migrations should be used.

Deployment

The solution follows Azure Developer CLI (azd) conventions and can be deployed to Azure.

azd auth login
azd up

Testing

The project supports automated testing using:

NUnit

Moq

FluentValidation

Shouldly

Testing is integrated into the architecture to support validation and long-term maintainability.

Learning Outcomes

Understanding Clean Architecture in ASP.NET Core

Designing enterprise-level backend systems

Applying SDLC concepts in real applications

Writing clean, maintainable, and testable code

Working with modern backend technologies
