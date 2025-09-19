# libft

> A custom implementation of the C standard library — rebuilt from scratch to understand memory management, string handling, and algorithmic fundamentals.

---

## 📚 Project Overview

`libft` is a foundational project in the 42 curriculum. It involves re-creating a selection of the C standard library's most important functions, from memory operations to string manipulation and linked lists — all written in **pure C** without any use of external libraries.

The goal: to develop a deep, working knowledge of C programming, memory handling, and low-level logic.

---

## ✅ Key Features

- 🔁 Full implementation of standard functions like `memcpy`, `strchr`, `atoi`, `calloc`, and many more
- 🧵 Bonus part includes a **linked list library** with `t_list` structure and operations
- 💡 100% Norminette-compliant and leak-free
- 🧪 Extensively tested against real `libc` behavior

---

## 🔧 Project Structure

| File / Folder | Description |
|---------------|-------------|
| `libft.h`     | Header with all prototypes and includes |
| `*.c`         | Implementation of each function |
| `Makefile`    | Build and clean targets |
| `ft_lst*.c` | Linked list operations: add, delete, iterate, map, etc. |

---

## 🧪 Compiling

To build the static library:

```bash
make
```

This creates `libft.a` — a static archive you can link to your own C programs.

To clean:

```bash
make clean     # removes object files
make fclean    # also removes libft.a
make re        # full rebuild
```

---

## 📂 Included Functions

### 🧠 Part 1 — Libc Functions

- `memset`, `memcpy`, `memmove`, `memchr`, `memcmp`
- `strlen`, `strlcpy`, `strlcat`, `strchr`, `strrchr`, `strncmp`
- `atoi`, `isdigit`, `isalpha`, `isalnum`, `isprint`, `isascii`
- `calloc`, `bzero`, `toupper`, `tolower`

### 🧠 Part 2 — Additional Utilities

- `substr`, `strjoin`, `strtrim`, `split`
- `itoa`, `strmapi`, `striteri`
- `putchar_fd`, `putstr_fd`, `putendl_fd`, `putnbr_fd`

### 🧵 Bonus — Linked List API

- `ft_lstnew`, `ft_lstadd_front`, `ft_lstadd_back`
- `ft_lstdelone`, `ft_lstclear`, `ft_lstiter`, `ft_lstmap`
- `ft_lstlast`, `ft_lstsize`

---

## 💡 Example Usage

```c
#include "libft.h"

int main(void)
{
    char *joined = ft_strjoin("Hello, ", "world!");
    ft_putendl_fd(joined, 1);  // prints to stdout
    free(joined);
    return 0;
}
```

---

## 🎯 Why libft Matters

- 🔧 Builds understanding of what’s happening *under the hood* in standard C libraries
- 🧠 Trains discipline in memory allocation and error handling
- 📐 Reinforces modular code and function design
- 💼 Used as a **base library** for many other 42 projects (e.g. `get_next_line`, `ft_printf`, `push_swap`)

---

## 📝 License

This project is part of the 42 School curriculum and intended for educational purposes. For reuse or redistribution, please contact the author.
