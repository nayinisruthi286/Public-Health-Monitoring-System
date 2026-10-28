# 🏥 HealthNet – Public Health Monitoring and Disease Surveillance System

HealthNet is a web-based public health management platform designed to help manage patient information, disease cases, laboratory reports, outbreak monitoring, and public health analytics in one centralized system.

The application provides role-based access to different healthcare stakeholders, helping them manage health information, monitor disease trends, maintain audit records, and support public health decision-making.

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Objectives](#-objectives)
- [Key Features](#-key-features)
- [System Modules](#-system-modules)
- [Technologies Used](#-technologies-used)
- [System Architecture](#-system-architecture)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Installation and Setup](#-installation-and-setup)
- [User Roles](#-user-roles)
- [Security](#-security)
- [Future Enhancements](#-future-enhancements)
- [Contributing](#-contributing)
- [License](#-license)

## 📖 Project Overview

HealthNet aims to provide a centralized digital platform for public health monitoring and healthcare data management. It connects different healthcare stakeholders through a web application and RESTful APIs.

The system supports disease case registration, patient management, laboratory test reporting, outbreak monitoring, analytics, audit tracking, and compliance management.

By organizing information in one system, HealthNet aims to improve data accessibility, monitoring, reporting, and coordination among healthcare stakeholders.

## 🎯 Objectives

- Centralize patient and disease-related information.
- Simplify disease case registration and tracking.
- Manage laboratory tests and reports digitally.
- Support disease outbreak monitoring.
- Provide dashboards and analytics for health data.
- Maintain audit records for accountability.
- Support compliance tracking and reporting.
- Implement role-based access for different users.

## ✨ Key Features

### 🔐 Authentication and Authorization
- User registration and login.
- Token-based authentication.
- Role-based access control.
- Protected routes for authorized users.

### 🧑‍⚕️ Patient Management
- Maintain patient information.
- Access patient records according to user permissions.
- Support patient-related healthcare workflows.

### 🦠 Disease Case Management
- Record and manage disease cases.
- Track case-related information.
- Support public health surveillance workflows.

### 🧪 Laboratory Management
- Manage laboratory test information.
- Upload laboratory reports.
- Associate test reports with relevant records.

### 📊 Outbreak Monitoring and Analytics
- Monitor disease-related trends.
- Display public health metrics and dashboards.
- Support health data analysis and reporting.

### 📝 Audit Management
- Manage audit records.
- Track audit-related activities.
- Support accountability and record management.

### 📋 Compliance Management
- Support compliance record management.
- Help organize compliance information and reporting.

## 🧩 System Modules

| Module | Description |
|---|---|
| User Management | Registration, login, roles, and access control |
| Patient Management | Patient information and records |
| Case Management | Disease case registration and tracking |
| Laboratory Management | Test details and report uploads |
| Outbreak Monitoring | Disease surveillance and outbreak information |
| Analytics and Reporting | Health metrics, dashboards, and reports |
| Audit Management | Audit record creation and tracking |
| Compliance Management | Compliance records and monitoring |

## 🛠️ Technologies Used

### Frontend
- **Angular 20** – Component-based web application development
- **TypeScript** – Application logic and type safety
- **HTML5 and CSS3** – User interface structure and styling
- **Bootstrap** – Responsive UI components
- **Angular Material** – UI components
- **RxJS** – Asynchronous operations and reactive data handling

### Backend
- **C#** – Backend programming language
- **ASP.NET Core Web API** – REST API development
- **Entity Framework Core** – Database access and ORM
- **JWT** – Token-based authentication

### Database
- **Microsoft SQL Server** – Relational database
- **SQL** – Data storage and querying

### Development Tools
- Visual Studio / Visual Studio Code
- Git and GitHub
- .NET CLI
- Node.js and npm
- Angular CLI

## 🏗️ System Architecture

HealthNet follows a frontend–backend architecture.

```text
              ┌──────────────────────────┐
              │        Users             │
              │ Citizens, Doctors, Admin │
              └────────────┬─────────────┘
                           │
                           ▼
              ┌──────────────────────────┐
              │ Angular 20 Frontend      │
              │ UI, Forms, Routing        │
              └────────────┬─────────────┘
                           │ HTTP / REST API
                           ▼
              ┌──────────────────────────┐
              │ ASP.NET Core Web API     │
              │ Controllers and Services │
              └────────────┬─────────────┘
                           │
                           ▼
              ┌──────────────────────────┐
              │ Entity Framework Core    │
              └────────────┬─────────────┘
                           │
                           ▼
              ┌──────────────────────────┐
              │ Microsoft SQL Server     │
              │ Healthcare Data          │
              └──────────────────────────┘
```

## 📁 Project Structure

The repository contains the solution file, API project, and database project.

```text
HealthNet/
├── HealthNet.slnx
├── README.md
├── .gitignore
├── HealthNet/
│   ├── Controllers/
│   ├── DTOs/
│   ├── Repository/
│   ├── Services/
│   ├── Utility/
│   ├── Properties/
│   ├── Program.cs
│   ├── appsettings.json
│   └── HealthNet.csproj
└── HealthNetDb/
    ├── Data/
    ├── Entities/
    └── HealthNetDb.csproj
```

*Note: This is a representative structure. Your actual folders and files may differ.*

## ⚙️ Prerequisites

Install the following before running the project:

- [Node.js and npm](https://nodejs.org/)
- [.NET SDK](https://dotnet.microsoft.com/download)
- [Angular CLI](https://angular.dev/tools/cli)
- [SQL Server](https://www.microsoft.com/sql-server)
- [SQL Server Management Studio](https://learn.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms)

Check your installations:

```bash
node --version
npm --version
dotnet --version
ng version
```

## 🚀 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/nayinisruthi286/Public-Health-Monitoring-System.git
cd Public-Health-Monitoring-System
```

### 2. Configure the Database

1. Install and start SQL Server.
2. Create or restore the required HealthNet database.
3. Configure the connection string in the backend's local configuration.
4. Verify that the database server and database name match your environment.

**Important:** Do not commit database passwords, JWT signing keys, or other secrets to GitHub. Use local configuration or environment variables for sensitive settings.

### 3. Restore Backend Dependencies

From the repository root:

```bash
dotnet restore HealthNet.slnx
```

### 4. Run the Backend API

```bash
dotnet run --project HealthNet/HealthNet.csproj
```

The API is configured to use the following local URL in the current development setup:

```text
http://localhost:5171
```

The exact URL may vary depending on your launch settings.

### 5. Install Frontend Dependencies

Open a separate terminal in the Angular frontend directory—the directory containing the frontend's `package.json` file.

Run:

```bash
npm install
```

### 6. Start the Frontend

From the Angular workspace directory, run:

```bash
npx ng serve
```

Open the local URL printed in the terminal, commonly:

```text
http://localhost:4200
```

**Note:** The frontend directory must contain `angular.json` and `package.json`. Confirm the actual frontend location before running these commands.

## 👥 User Roles

HealthNet supports role-based workflows for the following user categories:

- **Citizen:** Access citizen-related healthcare features.
- **Doctor:** Manage relevant patient and disease case information.
- **Lab Technician:** Manage laboratory tests and reports.
- **Public Health Officer:** Monitor public health cases and outbreak information.
- **Compliance Officer:** Manage compliance-related records.
- **Administrator:** Manage users and administrative workflows.
- **Researcher:** Access relevant health information and analytics.

Available actions depend on the permissions configured for each role.

## 🔒 Security

HealthNet includes authentication and role-based authorization features.

Security considerations for deployment include:

- Protecting API endpoints.
- Validating user input.
- Storing secrets outside source control.
- Using HTTPS in production.
- Applying least-privilege database permissions.
- Protecting sensitive health information.
- Reviewing dependencies for known vulnerabilities.

## 🔮 Future Enhancements

Potential future improvements include:

- Advanced disease trend visualization.
- Automated outbreak alerts.
- Improved reporting and export functionality.
- Integration with additional healthcare systems.
- Enhanced analytics and predictive monitoring.
- Expanded accessibility and mobile-friendly features.

These are proposed enhancements and may not be implemented in the current version.

## 🤝 Contributing

Contributions and suggestions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make and test your changes.
4. Commit your changes with a descriptive message.
5. Open a pull request.

## 📄 License

No license has been specified yet. Add an appropriate open-source license before permitting others to reuse, modify, or distribute this project.

---

**Developed as a public health technology project.**

**Repository:** [Public-Health-Monitoring-System](https://github.com/nayinisruthi286/Public-Health-Monitoring-System)
