dotnet new sln -n CrudDemo
cd CrudDemo


dotnet new classlib -n CrudDemo.Data
dotnet new webapi -n CrudDemo.API
dotnet new mvc -n CrudDemo.MVC

dotnet sln add CrudDemo.Data/CrudDemo.Data.csproj
dotnet sln add CrudDemo.API/CrudDemo.API.csproj
dotnet sln add CrudDemo.MVC/CrudDemo.MVC.csproj


dotnet add CrudDemo.API/CrudDemo.API.csproj reference CrudDemo.Data/CrudDemo.Data.csproj
dotnet add CrudDemo.MVC/CrudDemo.MVC.csproj reference CrudDemo.Data/CrudDemo.Data.csproj


cd CrudDemo.Data
mkdir Models DTOs Common IRepositories Repositories


dotnet sln CrudDemo.sln add Direct/CrudDemo.API/CrudDemo.API.csproj
