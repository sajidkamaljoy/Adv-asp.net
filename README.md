# Adv-asp.net

Coursework for an advanced ASP.NET course: three separate ASP.NET MVC 5 projects (.NET Framework 4.7.2), each in its own folder.

| Project | What it is |
|---|---|
| `assignment1` | A personal CV/portfolio site. Pages for personal info, education, projects and references, backed by simple `Student`, `Education`, `Project` and `References` models. |
| `lab-task-3` | **College Management.** Entity Framework (database-first) CRUD for students, courses and departments, with create and list screens for each. |
| `zerohunger` | **Zero Hunger**, a food-donation app. Restaurants post surplus food requests (weight, start time, validity); collectors pick them up; admins oversee everything. |

## Zero Hunger

- Sign up and log in with three roles: `admin`, `restaurant` and `collector`.
- Restaurants create and delete food requests.
- Admins assign a request to a collector, and each collector tracks how many requests are currently assigned.
- Access is restricted per role with custom authorization filters (`Auth/`).
- Entity Framework models: `user`, `restrurant`, `collector`, `request`. DTOs are in `DTOs/`.

## Tech stack

ASP.NET MVC 5, Entity Framework 6 (database-first for `lab-task-3` and `zerohunger`), SQL Server, Razor views, Bootstrap.

## Running a project

1. Open the project's `.sln` (or `.csproj`) in Visual Studio.
2. Restore NuGet packages.
3. For `lab-task-3` and `zerohunger`, point the `connectionStrings` entry in `Web.config` at your own SQL Server instance and create the database to match the EF model.
4. Press F5 to run with IIS Express.

## Notes

- `bin/` output and NuGet DLLs were committed with the code, so the repo is larger than the source alone.
- Database credentials and server names in `Web.config` belong to the original dev machine. Change them before running.
