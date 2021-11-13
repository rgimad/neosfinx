## The Syntax of Sphinx C-- (v0.239 b26)

### Pointers
You can declare pointers:
```
char *string [4] = {"string1", "string2", "string3", 0}; // a pointer array
char *str = "string4";
```
You can get address of variable using ```#``` operator (same as ```&``` in C):
```
int x = 999;
int *ptr = #x;
int **ptr2 = #ptr; // pointers to pointers to ... are allowed
```
You can dereference pointers using ```*```:
```
dword x = 0xBEEFF00D;
dword *ptr1 = #x;
byte *ptr2 = #x;
int a = *ptr1; // a = 0xBEEFF00D
int b = *ptr2; // b = 0xD
```
So, like in C, dereferenced value depends on pointer type

#### Limitations:
You cannot dereference expressions:
```
byte *p = #aboba;
byte b = *(p + 1); // gives error
```
