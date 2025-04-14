# Library App

## Description
The **Library App** is a console-based application designed to manage library operations such as patron management, book loans, and membership renewals. It is built using .NET 8.0 and follows a modular architecture with a clear separation of concerns.

## Project Structure
- **AccelerateDevGitHubCopilot.sln**: The solution file for the project.
- **README.md**: Documentation for the project.
- **src/**
  - **Library.ApplicationCore/**: Contains core business logic, entities, enums, and interfaces.
    - **Entities/**: Defines domain models such as `Patron`, `Loan`, `Book`, etc.
    - **Enums/**: Contains enumerations like `ConsoleState`.
    - **Interfaces/**: Defines contracts for repositories and services.
    - **Services/**: Implements business logic services like `LoanService` and `PatronService`.
    - **Library.ApplicationCore.csproj**: Project file for the core library.
  - **Library.Console/**: Implements the console application.
    - **appSettings.json**: Configuration file for the application.
    - **CommonActions.cs**: Defines common user actions in the console.
    - **ConsoleApp.cs**: The main application class managing the console workflow.
    - **ConsoleState.cs**: Enum representing the states of the console application.
    - **Program.cs**: Entry point for the console application.
    - **Json/**: Contains sample JSON data files for authors, books, patrons, etc.
    - **Library.Console.csproj**: Project file for the console application.
  - **Library.Infrastructure/**: Provides infrastructure-level implementations for data access.
    - **Data/**: Contains classes for JSON-based data storage and retrieval.
      - **JsonData.cs**: Manages loading and saving data from JSON files.
      - **JsonPatronRepository.cs**: Implements `IPatronRepository` for patron data.
      - **JsonLoanRepository.cs**: Implements `ILoanRepository` for loan data.
    - **Library.Infrastructure.csproj**: Project file for the infrastructure library.
- **tests/**
  - **UnitTests/**: Contains unit tests for the application.
    - **LoanFactory.cs**: Provides helper methods for creating test data.
    - **UnitTests.csproj**: Project file for the unit tests.

## Key Classes and Interfaces
- **Core Classes**:
  - `Patron`, `Loan`, `Book`, `BookItem`: Domain models representing library entities.
  - `ConsoleState`: Enum defining the states of the console application.
- **Interfaces**:
  - `IPatronRepository`, `ILoanRepository`: Contracts for data access.
  - `ILoanService`, `IPatronService`: Contracts for business logic services.
- **Console Application**:
  - `ConsoleApp`: Manages the console application's workflow and state transitions.
  - `Program`: Entry point for the application.
- **Infrastructure**:
  - `JsonData`: Handles JSON file operations for data storage.
  - `JsonPatronRepository`: Implements patron-related data access.
  - `JsonLoanRepository`: Implements loan-related data access.

## Usage
1. **Build the Project**:
   - Open the solution file `AccelerateDevGitHubCopilot.sln` in Visual Studio or your preferred IDE.
   - Build the solution to restore dependencies and compile the code.

2. **Run the Console Application**:
   - Navigate to the `src/Library.Console/` directory.
   - Run the application using the following command:
     ```sh
     dotnet run
     ```

3. **Unit Tests**:
   - Navigate to the `tests/UnitTests/` directory.
   - Run the tests using the following command:
     ```sh
     dotnet test
     ```

## License
This project is licensed under the MIT License. See the LICENSE file for details.
