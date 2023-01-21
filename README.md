# InfrastructureAspNetCoreLibrary

Project which includes:
1. Adds swager support.
2. Request logging.
3. Adds a new Serilog logging provider.

# Development

### Reference
Add a reference to the Infrastructure project in MainProject.csproj
```
<ItemGroup>
        <ProjectReference Include="..\FolderProject\Infrastructure.csproj" />
</ItemGroup>
```
_or via IDE functions_

### Call the method
In the asp.net main project, in the program.cs file, call the method `AddInfrastructure`.
```
static IHostBuilder CreateHostBuilder(string[] args)
{
    return Host.CreateDefaultBuilder(args)
        .ConfigureWebHostDefaults(webBuilder => { webBuilder.UseStartup<Startup>(); })
        .AddInfrastructure();
}
```
