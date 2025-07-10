# crun
Runs C++ sources.

Who say you need Python for scripting?

# Building
Not required, it's just a tiny shell script

# Installation
Self installing in bin:
``` bash
./crun --install
```

# Usage

For example you have helloworld.cpp

``` C++
#include <iostream>

int main(int argc, char** argv)
{
  std::cout << "Hello World\n";

  for (int i = 0; i < argc; i++)
  {
    std::cout << i << ": " << argv[i] << std::endl;
  }

  return 0;
}
```

To run it just use:
``` bash
crun helloworld.cpp foo bar baz
```

The output would be:
```
Hello World
0: ./helloworld.cpp
1: foo
2: bar
3: baz
```
