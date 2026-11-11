<h1 align="center">Etebase - Encrypt Everything</h1>

> [!NOTE]
> **This is an independent fork** of [etebase-csharp](https://github.com/etesync/etebase-csharp), the original
> project of the EteSync authors. This fork is not affiliated with, endorsed by or supported by EteSync or
> Etebase in any way. The history of the original project is kept as it is, with its authors, and the
> changes of this fork follow it. Like the original, it's licensed under the [BSD-3-Clause](./LICENSE) license.

A C# library for Etebase

**Star** and **watch** for updates.

![GitHub tag](https://img.shields.io/github/tag/nikossvnk/etebase-csharp.svg)


# Documentation

The C# bindings are not yet documented, but the API is almost identical to the Python one, with the main difference being the CamelCase vs the snake case. See [etebase-py](https://github.com/nikossvnk/etebase-py) and its type stubs.

# Using

We plan on adding a NuGet package soon (help needed!), though until then, you can download the libraries from the release page on github. The libraries are as follows:

* `etebase_csharp.dll` - the reference DLL that should be added to your project
* `libetebase_csharp_native.{so,dll,dylib}` - the per-platform Etebase library (actual Etebase code) - should be in the runtime path (e.g. on Windows it's just the same directory).

# Build

## Install deps

Make sure you have `cargo` (Rust Cargo) and `dotnet` (dotnet SDK) installed and working.

## Build

Build the main library and the C# p/invoke wrapper:
```
cargo build
cd target/dotnet-out/
dotnet build
```

You can then copy the libraries listed in the "Using" section above.
