# Envoy gRPC dotnet
This project is a .net library project which generates and compiles dotnet classes from Envoy's gRPC definitions.

This turns out to be non-trivial because envoy's protocol buffer definitions reference definitions from several other repositories, and the Grpc.Tools package cannot build them in that arrangement without some tweaking.

This project references those repositories as git submodules and tweaks the Grpc msbuild tools as necessary to build them.

This should make it possible to just add them as packages from nuget.

```
dotnet add package Envoy.Grpc
```