# Libft - 42 School

## About the Project
**Libft** is the very first project of the 42 Common Core curriculum.  
The goal is to recreate a subset of the standard C library (libc) functions, along with some additional utility functions that will serve as the foundation for all future C projects at the school.  

Understanding how these low-level functions work under the hood is crucial for mastering memory allocation, pointer manipulation, and basic algorithms in C.  
  
These functions all obey `norminette` an automated tool (linter) that checks C code to ensure it strictly follows the school's precise rules on styling, formatting, and structure (such as limiting functions to 25 lines and forbidding more than 5 variables per function).

---

## 🛠️ Functions

### 1. Libc Functions (Recreated Standard C Functions)
These functions mimic the behavior of their original counterparts in <ctype.h>, <string.h>, and <stdlib.h>.

| Function | Description |
| :--- | :--- |
| `ft_isalpha` | Checks for an alphabetic character. |
| `ft_isdigit` | Checks for a digit (0 through 9). |
| `ft_isalnum` | Checks for an alphanumeric character. |
| `ft_isascii` | Checks whether the character fits in the ASCII character set. |
| `ft_isprint` | Checks for any printable character. |
| `ft_strlen` | Calculates the length of a string. |
| `ft_memset` | Fills memory with a constant byte. |
| `ft_bzero` | Zeroes a byte string. |
| `ft_memcpy` | Copies a memory area. |
| `ft_memmove` | Copies a memory area, handling overlapping regions safely. |
| `ft_strlcpy` | Size-bounded string copying. |
| `ft_strlcat` | Size-bounded string concatenation. |
| `ft_toupper` | Converts a char to uppercase. |
| `ft_tolower` | Converts a char to lowercase. |
| `ft_strchr` | Locates the first occurrence of a character in a string. |
| `ft_strrchr` | Locates the last occurrence of a character in a string. |
| `ft_strncmp` | Compares two strings up to n bytes. |
| `ft_memchr` | Scans memory for a character. |
| `ft_memcmp` | Compares memory areas. |
| `ft_strnstr` | Locates a substring in a string, searching up to n characters. |
| `ft_atoi` | Converts a string to an integer. |
| `ft_calloc` | Allocates memory and initializes all bits to zero. |
| `ft_strdup` | Creates a duplicate of a string using malloc. |

### 2. Additional Functions
Non-standard functions either not present in libc or modified to fit 42 project requirements.

| Function | Description |
| :--- | :--- |
| `ft_substr` | Extracts a substring from a string. |
| `ft_strjoin` | Concatenates two strings into a new dynamically allocated string. |
| `ft_strtrim` | Trims specified characters from the beginning and end of a string. |
| `ft_split` | Splits a string into an array of strings using a delimiter character. |
| `ft_itoa` | Converts an integer to a string. |
| `ft_strmapi` | Applies a function to each character of a string to create a new string. |
| `ft_striteri` | Applies a function to each character of a string (modifies in-place). |
| `ft_putchar_fd` | Outputs a character to a given file descriptor. |
| `ft_putstr_fd` | Outputs a string to a given file descriptor. |
| `ft_putendl_fd` | Outputs a string followed by a newline to a given file descriptor. |
| `ft_putnbr_fd` | Outputs an integer to a given file descriptor. |

### 3. Bonus Functions (Linked List Manipulation)
These functions utilize a custom structure to implement and manipulate singly linked lists.
```
List Structure:
typedef struct s_list
{
    void            *content;
    struct s_list   *next;
}   t_list;
```
| Function | Description |
| :--- | :--- |
| `ft_lstnew` | Creates a new list node. |
| `ft_lstadd_front` | Adds a node at the beginning of a list. |
| `ft_lstsize` | Counts the number of nodes in a list. |
| `ft_lstlast` | Returns the last node of a list. |
| `ft_lstadd_back` | Adds a node at the end of a list. |
| `ft_lstdelone` | Frees the memory of a node's content using a custom function, then frees the node. |
| `ft_lstclear` | Deletes and frees a list and all its successors. |
| `ft_lstiter` | Iterates over a list and applies a function to the content of each node. |
| `ft_lstmap` | Iterates over a list and applies a function to create a new list. |

---

## Getting Started

### Prerequisites
To compile and use this library, you will need a C compiler (gcc or clang) and make installed on your system.

### Compilation
The provided Makefile is set up to compile the library using the standard flag requirements (-Wall -Wextra -Werror).

1. Compile the mandatory functions:
   `make`

2. Compile the bonus functions:
   `make bonus`

3. Clean up object files (.o):
   `make clean`

4. Clean up everything (object files and libft.a):
   `make fclean`

5. Rebuild the library from scratch:
   `make re`

6. See all options on the terminal:
   `make help`
---

##  How to Use It in Your Projects

1. Copy the libft directory (or just the source files, libft.h, and Makefile) into your project folder.
2. Include the header file in your C source files:
   #include "libft.h"
3. Compile your project source files along with `libft.a` .

---