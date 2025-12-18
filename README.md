# Vaja4-interrupt-button-STM32L1

PINOUT KONFIGURACIJE:\
![konfig](https://github.com/Hudi452/Vaja4-interrupt-button-STM32L1/blob/main/Pinout_konfiguracija.png)

VIDEO DELOVANJA:\


ODGOVORI NA VPRAŠANJA:\
Postopek inicializacije programa:\
b) Modro tipko lahko uporabimo kot digitalni vhod s prekinitvijo. To je pin PA0.\
c) pin za zeleno LED: PC9\
   pin za modro LED: PC8

Program:\
c) HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_9);\
d)fsysclk = 32 MHz\
Predpostavimo, da je ena ponovitev enaka času enega cikla:\
delay = 1/(32*10^6) * 10000 = 0,0003125 s = 312,5 us \
e)HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_8);\
f) HAL_Delay(500);

Opažanja:\
e) Modra LED ves čas utripa s frekvenco 1 Hz. Ko pritisnemo na modro tipko se zeleni LED spremeni stanje. \ 
f) Pritisk na modro tipko ne vpliva na utripanje modre LED zaradi zunanje prekinitve, ki se izvede, ko pritisnemo na modro tipko. Tako lahko modra LED utripa neodvisno od stanja modre tipke. 
