# Welcome to AVRCompiler docs

This software was created to compile and upload C or ASM files to microcontroller such as atmega328p

## Setup

Works with java-11+ . Be sure to use the correct java version

Please install avrdude and make sure you can use it in the cmd

## How to use

First, you need to choose the correct port and microcontroller, then click "Upload", this button will open a file explorer window, choose your C/ASM file. Finally click open and that's all !

## Can't compile ?

Don't worry, i'm working on an update to automatically refresh the serial ports. But now, if you can't compile, just unplug your microcontroller and then connect it again.

## Pull Requests

If you have any problems, feel free to make a pull request !

## Basic Blink Example

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
## Table of Context

AVRCompiler docs
* [Main Functions](https://novus-alex.github.io/AVRCompiler/main_functions)
