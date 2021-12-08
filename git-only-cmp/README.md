# Example Git-only Component

This component is an example of a component hosted on GitHub only with a dependency on an other component from registry

To use it with your ESP-IDF project make sure that [the component manager](https://pypi.org/project/idf-component-manager/) is installed and create the manifest `idf_component.yml` in the project's `main` component directory:

```yaml
dependencies:
  git-only-cmp:
    path: git-only-cmp
    git: https://github.com/espressif/example_components.git
```

## API

This component defines only one function `void git_only_cmp_hello()` that prints a welcome message defined in [example/cmp](https://components.espressif.com/component/example/cmp).

### Example

```C
#include "git-only-cmp.h"

void app_main(void)
{
    git_only_cmp_hello();
}
```
