## open and openat functions
A file is opened or created by calling either the open function or the openat function.
```c
#include <fcntl.h>
int open(const char *path, int oflag, ... /* mode_t mode */ );
int openat(int fd, const char *path, int oflag, ... /* mode_t mode */ );
```
We show the last argument as ..., which is the ISO C way to specify that the number
and types of the remaining arguments may vary.

The path parameter is the name of the file to open or create. This function has a
multitude of options, which are specified by the oflag argument. This argument is
formed by ORing together one or more of the following constants from the <fcntl.h>
header:

..* one