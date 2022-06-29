# Pic 16F887 Entradas Digitales

<img src="https://github.com/IDiegoUlises/Pic-Entradas-Digitales/blob/main/Images/16f887-Pic.png"  />

* **Todos los puertos que funcionan como salida funcionan como entradas digitales**
* Vdd: Positivo del microcontrolador
* Vss: Negativo del microcontrolador
* Clkin: Osicilador conectado a negativo
* Clkout: Osicilador conectado a negativo

### Codigo

```c
#include <16f887.h> //Nombre del microcontrolador
#fuses xt,nowdt  //para osciladores de 4 MegaHertz se usa xt para mayores usa hs
#use delay(clock=4M) //Velocidad del oscilador, la "M" signfica mega

void main()
{
   while(true)
   {
      if(input(pin_a0) == 1) //Cuando esta en HIGH
      {
         output_high(pin_c0); //Enciende el led
      }
      else
      {
         output_low(pin_c0); //Apaga el led
      }
      
   }
}
```

### Compilar en Css Compiler
<img src="https://github.com/IDiegoUlises/Pic-Entradas-Digitales/blob/main/Images/Codigo-Imagen.png"  />

