# Blazor United App Project Template

[Blazor United](https://github.com/dotnet/aspnetcore/issues/46636) is a feature in ASP.NET Core roadmap for .NET 8. **Blazor United** will have similar features which can be found in JavaScript frameworks, such as **Next.js**, **Nuxt.js** or **Angular Universal**. 

In these frameworks, Server-side rendering (SSR), Client-side rendering (CSR) and Static site generation (SSG) are mixed up in web application development. They are full stack frameworks. 

In .NET, we can also use Blazor to create Blazor Hybrid app, such as .NET MAUI Blazor app. In this case, we can treat Blazor as a cross-platform full stack framework. 

I created a Visual Studio project template to generate a Blazor cross-platform full stack project. 

After you install Blazor United App project template, you can create a new Blazor United app solution. In the solution, it will generate the following projects for you. 

- `App` - This is a .NET MAUI Blazor Hybrid app so we can build the app for Android, iOS, macOS and Windows. 

- `Client` - This is a Blazor WebAssembly project. 

- `Server` - This is a .NET Core project which provides backend services for our app. 

- `Shared` - This is a Razor class library. We can create most of our code in this library so we can share code in both web and mobile apps. 

- `Shared.Tests` - This is a unit test project to test Razor class library Shared. 

When Blazor United is released in .NET 8, we should be able to integrate Client and Server project into one project.

In the project template, OpenAPI is used in `Server` project. The generated `swagger.json` is in `Shared.OpenAPIs` namespace. The client-side code will be generated from swagger.json for `App` and `Client` projects.