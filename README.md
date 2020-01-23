Snappy for Visual C++
=====================

This repository was forked from [https://github.com/robertvazan/snappy-visual-cpp](https://github.com/robertvazan/snappy-visual-cpp).

Changes:

 * Re-targeted to VS2019.
 * Removed architecture suffix from library.
 * Export C++ symbols.

### Building

    msbuild snappy.sln /p:Configuration=Release /p:Platform=x64


### Running Unit Tests

    .\x64\Release\runtests.exe

### Example

```cpp
char compressed[1000];
size_t length = 1000;
snappy_status status = snappy_compress("Hello World!", 12, compressed, &length);
```
