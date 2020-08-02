# Source Generators don't work with Blazor WASM example

This project uses [a "Hello world" source generator](https://devblogs.microsoft.com/dotnet/introducing-c-source-generators/) and the latest .NET 5 preview (5.0.0-preview.7.20364.11) to demonstrate that Source Generators don't work correctly with Blazor WASM.

This solution includes 3 projects:

* The Hello World Source Generator [from here](https://devblogs.microsoft.com/dotnet/introducing-c-source-generators/)
* A basic .NET 5 Console application, demonstrating usage of the source generator. This project compiles, builds, and runs perfectly.
* A basic Blazor WASM application, demonstrating an identical usage, which _doesn't_ compile.
