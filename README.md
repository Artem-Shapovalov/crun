# crun
Runs C++ sources.

Who say you need Python for scripting?

# Features

- Have its own set of helpers that much more convenient than STL or boost and similar to regular shell commands:
  - mkdir
  - touch
  - rm
  - cp
  - mv
  - ls
  - find
  - abspath
  - curdir
 
- Global context and expression engine:
  - Global context is just a key-value pairs storage for your script
  - Expression engine recursively substitutes the global storage values by keys in '${}'

- Not bloats your system with configs or libraries, all of the needed it keeps inside your cpp.

- Easy to use, have the template source generation with comprehensive comments. Just fill the 'main()'.

# Building
Not required, it's just a tiny shell script

# Installation
Self installing in bin:
``` bash
chmod +x crun
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
