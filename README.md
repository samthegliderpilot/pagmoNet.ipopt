# PagmoNet IPOPT add-on

Optional IPOPT (Interior Point OPTimizer) wrapper for the [PagmoNet](https://github.com/PagmoNet) pagmo2 bindings.

- .NET package: `PagmoNet.Ipopt`
- Java/Kotlin artifact: `pagmonet4j-ipopt`

## Contents

| Directory | Purpose |
|---|---|
| `swig/ipopt.i` | SWIG interface for the IPOPT pagmo2 algorithm |
| `dotnet/generated/` | SWIG-generated C# wrapper classes |
| `dotnet/extensions/` | Hand-written C# extension for `ipopt` |
| `java/generated/` | SWIG-generated Java wrapper class |
| `ports/coin-or-ipopt/` | Custom vcpkg port for IPOPT |

## License

The wrapper code in this repository is LGPL-2.1-or-later (see [LICENSE](LICENSE)).  
IPOPT itself is EPL-2.0 — see [NOTICE](NOTICE) for details.

## Dependencies

- [PagmoNet/pagmoNet](https://github.com/PagmoNet/pagmoNet) (submodule — SWIG + native bridge)
- [PagmoNet/pagmo.NET](https://github.com/PagmoNet/pagmo.NET) or [PagmoNet/PagmoNet4j](https://github.com/PagmoNet/PagmoNet4j)
