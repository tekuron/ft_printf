# ft_printf
![Language](https://img.shields.io/badge/Language-C-blue)
![Score](https://img.shields.io/badge/Score-125%2F100-brightgreen)

<p>Reimplementation of the printf function in C, developed as part of the 42 curriculum, capable of handling formatted output with multiple conversions, flags, width, and precision.</p>

---

## Table of Contents
- [Overview](#overview)
- [Usage](#usage)
- [Bonus Part](#bonus-part)
- [Author](#author)

---

## Overview
ft_printf is a reimplementation of the standard C printf function. It provides formatted output of text, numbers, and pointers, supporting multiple conversion specifiers, flags, width, and precision. This project was developed as part of the 42 curriculum to strengthen understanding of variadic functions, C standard library functions, and low-level string formatting.

## Usage
To compile and use ft_printf, run:
```bash
make
```
This generates the static library `libftprintf.a`, which you can link when compiling your programs.

Example usage:
```c
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello %s!\n", "world");
    return 0;
}
```

## Bonus Part
To compile the ft_printf function with the bonus features, run:
```bash
make bonus
```
The bonus part extends ft_printf with additional features, including full support for all conversion specifiers, handling of all standard flags, and edge case management. This ensures more complete compatibility with the standard printf behavior.

Examples of flags and conversions:

1. '+' flag (forces sign on positive numbers)
```c
ft_printf("|%+d|\n", 42);
```
```stdout
|+42|
```
2. '-' flag (left-align within width)
```c
ft_printf("|%-10d|\n", 42);
```
```stdout
|42        |
```
3. 0 flag (pads with zeros, only if no precision)
```c
ft_printf("|%08d|\n", 42);
```
```stdout
|00000042|
```
Note: The 0 flag is ignored when a precision is specified.
```c
ft_printf("|%08.5d|\n", 42); // 0 flag ignored due to precision
```
```stdout
|   00042|
```
4. space flag (adds space before positive numbers)
```c
ft_printf("|% d|\n", 42);
```
```stdout
| 42|
```
5. '#' flag (alternate form, for hex)
```c
ft_printf("|%#x|\n", 255);
```
```stdout
|0xff|
```

Examples of combined flags:
- '+' and 0 with width (no precision)
```c
ft_printf("|%+08d|\n", 42); // + sign, 0 padding, width 8
```
```stdout
|+0000042|
```
- '-' and '#' with width
```c
ft_printf("|%-#10x|\n", 255); // left-align, alternate hex form, width 10
```
```stdout
|0xff      |
```

## Author
- **Name:** Daniel Zamora
- **GitHub:** [tekuron](https://github.com/tekuron)
- **42 Intra:** [danzamor](https://profile-v3.intra.42.fr/users/danzamor)
- **School:** 42
