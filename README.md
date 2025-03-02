# Library App

## Description
Library App is a console-based library management system. It allows users to search for patrons, view patron details, manage loans, and update patron information. The application is built using C# and follows a layered architecture with separate projects for core application logic, console interface, and data access.

## Project Structure
- `AccelerateDevGitHubCopilot.sln`
- `README.md`
- `src/`
  - `Library.ApplicationCore/`
    - `Entities/`
    - `Enums/`
    - `Interfaces/`
    - `Services/`
    - `Library.ApplicationCore.csproj`
  - `Library.Console/`
    - `appSettings.json`
    - `CommonActions.cs`
    - `ConsoleApp.cs`
    - `ConsoleState.cs`
    - `Json/`
    - `Library.Console.csproj`
    - `Program.cs`
  - `Library.Infrastructure/`
    - `Data/`
    - `Library.Infrastructure.csproj`
- `tests/`
  - `UnitTests/`
    - `ApplicationCore/`
    - `UnitTests.csproj`

## Key Classes and Interfaces
- **Library.ApplicationCore**
  - `Entities/`
    - `Patron`: Represents a library patron.
    - `Loan`: Represents a loan of a book item to a patron.
  - `Enums/`
    - `ConsoleState`: Enum representing the different states of the console application.
  - `Interfaces/`
    - `IPatronRepository`: Interface for patron data access.
    - `ILoanRepository`: Interface for loan data access.
    - `ILoanService`: Interface for loan-related operations.
    - `IPatronService`: Interface for patron-related operations.
  - `Services/`
    - `LoanService`: Implementation of `ILoanService`.
    - `PatronService`: Implementation of `IPatronService`.

- **Library.Console**
  - `ConsoleApp`: Main class for the console application.
  - `Program`: Entry point for the console application.
  - `CommonActions`: Enum representing common actions in the console application.
  - `ConsoleState`: Enum representing the different states of the console application.

- **Library.Infrastructure**
  - `Data/`
    - `JsonData`: Utility class for loading and saving data from/to JSON files.
    - `JsonPatronRepository`: Implementation of `IPatronRepository` using JSON data.
    - `JsonLoanRepository`: Implementation of `ILoanRepository` using JSON data.

## Usage
1. Clone the repository.
2. Open the solution file `AccelerateDevGitHubCopilot.sln` in Visual Studio.
3. Build the solution to restore dependencies and compile the projects.
4. Run the `Library.Console` project to start the console application.
5. Follow the on-screen instructions to interact with the library management system.

## License
This project is licensed under the MIT License.
