# Example Component

This component is an example, to be used with the IDF component manager.

To use it with your ESP-IDF project make sure that [the component manager](https://pypi.org/project/idf-component-manager/) is installed and create the manifest `idf_component.yml` in the project's `main` component directory:

```yaml
dependencies:
  example/cmp: "^3.3.3"
```

## API

This component defines only one function `void cmp_hello()` that prints a welcome message.

### Example

```C
#include "cmp.h"

void app_main(void)
{
    cmp_hello();
}
```

