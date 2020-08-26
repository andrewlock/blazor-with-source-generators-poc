# Source Generators don't work with Razor componenets

This project uses [a "Hello world" source generator](https://devblogs.microsoft.com/dotnet/introducing-c-source-generators/) and the latest .NET 5 preview (5.0.100-preview.8.20417.9) to demonstrate that Source Generators don't work correctly with any ASP.NET Core application that includes a Razor template.

This solution includes 4 projects:

* The Hello World Source Generator [from here](https://devblogs.microsoft.com/dotnet/introducing-c-source-generators/)
* A basic .NET 5 Console application, demonstrating usage of the source generator. This project compiles, builds, and runs perfectly.
* A basic Blazor WASM application, demonstrating an identical usage, which _doesn't_ compile, due to using the output of the generator in _Program.cs_
* An empty Web project (`dotnet new web`), with the addition of a single basic Razor component. Without the component, the project builds. With the component, the build fails due to using the output of the generator in _Program.cs_
