# Continuity

Continuity is a platform for using react-native within a native application.

## Building

Continuity uses CMake and Ninja.

### Windows

1. Install the Visual Studio 2017 build tools package

```
choco install visualstudio2017buildtools
```

2. Generate Ninja build scripts

```
"%ProgramFiles(x86)%\Microsoft Visual Studio\2017\BuildTools\VC\Auxiliary\Build\vcvarsall.bat" x86 10.0.18362.0

cmake -B build\Debug\%VSCMD_ARG_TGT_ARCH% -S . -G Ninja -DCMAKE_BUILD_TYPE=Debug
cmake -B build\Release\%VSCMD_ARG_TGT_ARCH% -S . -G Ninja -DCMAKE_BUILD_TYPE=Release

"%ProgramFiles(x86)%\Microsoft Visual Studio\2017\BuildTools\VC\Auxiliary\Build\vcvarsall.bat" x64 10.0.18362.0

cmake -B build\Debug\%VSCMD_ARG_TGT_ARCH% -S . -G Ninja -DCMAKE_BUILD_TYPE=Debug
cmake -B build\Release\%VSCMD_ARG_TGT_ARCH% -S . -G Ninja -DCMAKE_BUILD_TYPE=Release
```

3. Run the build

```
"%ProgramFiles(x86)%\Microsoft Visual Studio\2017\BuildTools\VC\Auxiliary\Build\vcvarsall.bat" x86 10.0.18362.0

ninja -C build\Debug\%VSCMD_ARG_TGT_ARCH%
ninja -C build\Release\%VSCMD_ARG_TGT_ARCH%

"%ProgramFiles(x86)%\Microsoft Visual Studio\2017\BuildTools\VC\Auxiliary\Build\vcvarsall.bat" x64 10.0.18362.0

ninja -C build\Debug\%VSCMD_ARG_TGT_ARCH%
ninja -C build\Release\%VSCMD_ARG_TGT_ARCH%
```

The public headers are under `include/Continuity`, and the Windows DLLs are:

- `build\Debug\x86\src\Continuity\Continuity.dll`
- `build\Debug\x64\src\Continuity\Continuity.dll`
- `build\Release\x86\src\Continuity\Continuity.dll`
- `build\Release\x64\src\Continuity\Continuity.dll`

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
