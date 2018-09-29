# TIMER A Blink
The TIMER peripherals can be used in many situations thanks to it flexibility in features. For this lab, you will be only scratching the surface as to what this peripheral can do. 

## README
A timer in up mode was used to toggle two LEDs at different speeds. Two timers were created to trigger an interrupt at the positive edge. Both timers had different frequencies wich allowed them to complete the interrput at differnt rates. Both interrupts were toggles for the given LED but at different values of the function, timerConvert. The function timerConvert took an input which allowed the timer to be short or long in terms of Hz. 

The code is written to work on the MSP430G2553 and F5529. 
