# Pic-Entradas-Digitales

```c
#include <16f887.h> //Nombre del microcontrolador
#fuses xt,nowdt  //para osciladores de 4 MegaHertz se usa xt para mayores usa hs
#use delay(clock=4M) //Velocidad del oscilador, la "M" signfica mega

void main()
{
   while(true)
   {
      if(input(pin_a0) == 1)
      {
         output_high(pin_c0); 
      }
      else
      {
         output_low(pin_c0);
      }
      
   }
}
```
