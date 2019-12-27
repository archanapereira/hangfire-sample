HangfireApplication Readme
This is a sample application to test hangfire scheduler.

Prerequisites
	1. The two blank databases HangfireDB and HangfireApplication should be created on SQL Server.
Installation steps
  1. Tested with SQL Server 2019 Express edition
  2. Download Hangfire from nuget
  3. Refer https://docs.microsoft.com/en-us/aspnet/core/security/authentication/scaffold-identity?view=aspnetcore-3.1&tabs=visual-studio to add identity tables. Below steps will add tables in the database HangfireApplication
	  a. Install-Package Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore -Version 3.0.0 
			Reason - Current dotnetcore version is netcore3.0
	  b. Add-Migration CreateIdentitySchema
	  c. Update-Database
  4. Once the application is up and running then create a new user.
  5. Login with the new user.
  6. Append /hangfireDashboard on the address bar of Home page. A page with hangfire dashboard will open.
  7. This page will have 4 options Jobs, Retires, Recurring Jobs, Servers along with graph for Realtime and History.