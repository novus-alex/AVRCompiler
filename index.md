## Welcome to AVRCompiler docs

This software was created to compile and upload C or ASM files to microcontroller such as atmega328p

### Basic Blink Example

this is a basic example of led blinking made for atmega328p
```C
#ifndef F_CPU
#define F_CPU 1600000UL
#endif

#include <avr/io.h>
#include <util/delay.h>

int main(void) {
	DDRC |= (1 << PC5);
	while (1) {

		// Toggle LED at port PC5
		PORTC ^= (1 << PC5);

		// Delay for 500ms
		_delay_ms(500);
	}
	return 0;
}
```
