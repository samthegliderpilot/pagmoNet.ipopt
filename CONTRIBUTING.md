# Contributing to pagmoNet.ipopt

This repo contains the IPOPT add-on for PagmoNet. It ships the generated C# and Java
bindings for [IPOPT](https://github.com/coin-or/Ipopt) (EPL-2.0) and the vcpkg overlay
port that builds it as part of the native DLL.

## Prerequisites

- .NET 10 SDK (for .NET add-on)
- JDK 21+ (for Java add-on)
- The base `pagmoNet` repo (will be a submodule)
- vcpkg with `VCPKG_ROOT` set

## Building

IPOPT support is compiled into the base `PagmoWrapper.dll` / `libPagmoWrapper.so`
when `PAGMONET_WITH_IPOPT=ON` is passed to CMake (the default in `pagmoNet/scripts/build-native.ps1`).
The `ports/coin-or-ipopt/` overlay in this repo must be present on the vcpkg overlay path.

```powershell
# Windows
$env:VCPKG_ROOT = "C:\vcpkg"
pwsh pagmoNet/scripts/build-native.ps1 -Configuration Release
```

## Repo layout

| Path | Contents |
|---|---|
| `dotnet/generated/` | SWIG-generated `ipopt.cs`, log-entry types |
| `dotnet/extensions/` | Hand-written C# extensions for `ipopt` |
| `java/generated/` | SWIG-generated `ipopt.java` |
| `ports/coin-or-ipopt/` | vcpkg overlay port for COIN-OR IPOPT |
| `swig/` | `ipopt.i` SWIG interface file |

## Third-party notices

IPOPT is licensed under the Eclipse Public License 2.0 (EPL-2.0). See [NOTICE](NOTICE).

## License

The wrapper code in this repository is LGPL-2.1-or-later. See [LICENSE](LICENSE).
