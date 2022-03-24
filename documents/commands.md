# Commands for initial setup directories

mkdir FullDotNetCore
cd FullDotNetCore
mkdir sources
mkdir documents
mkdir sqlQueries

# Commands for the first project. web app

cd FullDotNetCore
dotnet new sln -o sources/1_project
cd sources/1_project/
dotnet new globaljson --sdk-version 6.0.101
dotnet new mvc --auth Individual -o FullDev.WebApp
dotnet new classlib -o FullDev.Business
dotnet new classlib -o FullDev.Data
dotnet sln add FullDev.*