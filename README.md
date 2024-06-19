# ProductAPI

## Description
ProductAPI is a .NET Core Web API project that demonstrates CRUD operations using .NET Core, Entity Framework Core with SQL Server, and Dependency Injection.

## Prerequisites
- [.NET Core SDK](https://dotnet.microsoft.com/download) (version 5.0 or higher)
- [Visual Studio Code](https://code.visualstudio.com/) or [Visual Studio](https://visualstudio.microsoft.com/) (optional, for development)

## Getting Started
Follow these steps to get the project up and running on your local machine.

### 1. Clone the repository
```bash
git clone https://github.com/mustafakbaser/ProductManagementAPI.git
cd ProductAPI
```

### Restore Necessary Packages:
```bash
dotnet restore
```

### Update Database with Migrations:
```bash
dotnet ef database update
```

*Note:* Ensure your connection string in appsettings.json is correctly configured.

### 2. Configure the database connection
Update the database connection string in appsettings.json file located in the ProductAPI directory.

```bash
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost\\SQLEXPRESS;Database=YourDatabaseName;Trusted_Connection=True;"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning",
      "Microsoft.Hosting.Lifetime": "Information"
    }
  },
  "AllowedHosts": "*"
}
```

Replace YourDatabaseName with the name of your SQL Server database. Also, check your server name and replace `localhost\\SQLEXPRESS` if it differs.

### 3. Apply EF Core Migrations
Open a terminal or command prompt and navigate to the ProductAPI directory.

```bash
cd ProductAPI
dotnet ef database update
```

This command will apply the EF Core migrations and create/update the database schema based on your DbContext.

### 4. Run the application
Run the following command to start the API server:

```bash
dotnet run
```

### 5. Access the API:

Open your web browser and navigate to https://localhost:5001/swagger/index.html to view and interact with the Swagger UI of the API.

## Project Structure
The project structure is organized as follows:

- Controllers/: Contains API controller classes.
- Models/: Contains data models used in the application.
- Services/: Contains business logic services.
- Data/: Contains DbContext and migrations.
  
### Configuration
Modify appsettings.json to configure database connection strings and other settings as needed.

### Additional Notes
Ensure you have SQL Server installed and running locally, or update the connection string to point to your SQL Server instance.
