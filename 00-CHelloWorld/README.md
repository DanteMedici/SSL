## Configuración del Compilador

- **Compilador seleccionado:** GCC  
- **Versión del compilador:** 14.2.0  
- **Versión de C utilizada:** C18 (201710L)

  
## Verificación de la Versión de C en Visual Studio
  
Para verificar qué estándar de C utiliza el compilador en Visual Studio, se utilizó el siguiente programa:

```c
#include <stdio.h>

int main()
{
  #if defined __STDC_VERSION__
    if(__STDC_VERSION__ == 202000)
        printf("Estas usando C23!\n");
    else if (__STDC_VERSION__ == 201710L)
        printf("Estas usando C17!\n");
    else if (__STDC_VERSION__ == 201112L)
        printf("Estas usando C11!\n");
    else if (__STDC_VERSION__ == 199901L)
        printf("Estas usando C99!\n");
  #else
    printf("We are using C90!\n");
  #endif

  return 0;
}
