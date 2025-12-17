# Vaja4-interrupt-button-STM32L1

SLIKA KONFIGURACIJE:\
![konfig](]https://github.com/Hudi452/Vaja4-interrupt-button-STM32L1/blob/main/Pinout_konfiguracija.png)

ODGOVORI NA VPRAŠANJA:\
Postopek inicializacije programa:\
b) Modro tipko lahko uporabimo kot digitalni vhod z interupt. to je pin PA0\
c) pin za zeleno LED:PC9\
   pin za modro LED:PC8

Program:\
c) HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_9);\
d)fsysclk = 32 MHz\
delay = 1/(32*10^6) * 10000 = 0,0003125 s \
e)HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_8);\
f) HAL_Delay(500);

Opažanja:\
e) Ko pritisnemo na tipko se zeleni LED spremeni stanje. Modra LED pa ves čas utripa s frekvenco 1 Hz. To je mogoče zaradi zunanje prekinitve.\ 
f) Ne vpliva na utripanje modre LED zaradi zunanje prekinitve, ki se izvede, ko pritisnemo na modro tipko.
