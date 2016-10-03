# fips-nlohmann-json

- nlohmann/json: https://github.com/nlohmann/json
- fips:  https://github.com/floooh/fips

Requires C++ exceptions enabled, add the following line
to you toplevel CMakeLists.txt file before fips_setup()
is called, or build with a fips config that sets FIPS\_EXCEPTIONS to ON:

```cmake
set(FIPS_EXCEPTIONS ON CACHE BOOL "Enable C++ exceptions" FORCE)
fips_setup()
...
```

This is a header-only lib, simply add to your fips.yml as import
and include json.hpp:

```yaml
imports:
    fips-nlohmann-json:
        git:    https://github.com/sgerbino/fips-nlohmann-json
```

```cpp
#include <json.hpp>
```
