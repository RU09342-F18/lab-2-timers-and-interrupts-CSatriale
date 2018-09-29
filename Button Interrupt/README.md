# Button Interrupt
Last lab you were introduced to the idea of "Polling" where in you would constantly check the status of the P1IN register to see if something has changed. While your code may have worked, it ends up spending a ton of time just checking something that has not changed. What we can do instead is use another two registers available to us from the GPIO peripheral, P1IE and P1IES, to allow our processor to just chill out and wait until something happens to act upon it. Without spending too much space on this README with explanations, what makes these interrupts tick is the following code:

```c
#pragma vector=PORT1_VECTOR
__interrupt void Port_1(void)
{
}
```

While you still need to initialize the Ports to be interrupt enabled and clear the flags, this "Pragma Vector" tells the compiler that when a particular interrupt occurs, run this code. 

# README
The code toggles the state of an LED based on a timer and interrupt instead of a clock. An interrupt is set to occur whenever a button is pressed. The interrupt service routine toggles the state of the LED. The processor then goes in to low power mode to reduce power consumption. The code is written for both the MSP430G2553 and MSP430F5529 which have different pins for buttons.
