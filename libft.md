# notion
## void * = Generic Pointer;
- A void * is a pointer to any type of data. It's a "generic" or "typeless" pointer.
- char *ptr;     // Compiler knows: 1 byte per element
- int *ptr;      // Compiler knows: 4 bytes per element  
- double *ptr;   // Compiler knows: 8 bytes per element
- void *ptr;     // Compiler knows: ??? (no size information!)
## size_t
Always ≥ 0,Handles larger values

##Function	NULL handling
ft_memset	No check - let it crash (standard behavior)
ft_memcpy	Check if (!dest && !src) for edge case

##len vs size
char src[] = "hello";
// Memory layout:
[h][e][l][l][o][\0]
 0  1  2  3  4  5    ← indices
strlen(src) = 5      ✅ Does NOT count \0
sizeof(src) = 6      ✅ Counts \0 (total bytes)
