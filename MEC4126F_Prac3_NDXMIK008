// Description----------------------------------------------------------------|
/*
 *
 */
// DEFINES AND INCLUDES-------------------------------------------------------|

#define STM32F051												   //COMPULSORY
#include "stm32f0xx.h"											   //COMPULSORY
#include "lcd_stm32f0.h"

// GLOBAL VARIABLES ----------------------------------------------------------|
struct age_data{ int day; int month; int year; int age;} age_data;// Creating and naming of structure
char display[2];


// FUNCTION DECLARATIONS -----------------------------------------------------|

void main(void);                                                   //COMPULSORY

// MAIN FUNCTION -------------------------------------------------------------|

void main(void)
{
	age_data.day= 5; // Defining values for structural members 
	age_data.month= 9;
	age_data.year= 2002;
	age_data.age= 20;

	init_LCD();

	while(1)
	{for (uint8_t i=0; i<=age_data.age; i++)/* for loop counts up to age in structure */
	{
		if (i<=age_data.age){
		sprintf(display,"%d", i) /*puts counter variable into display string to be displayed on LCD */;
		delay(80000);
		lcd_command(CLEAR); /* clear LCD */
		delay(80000);
		lcd_putstring(display); /*Displays the string of the age counter */ }
		else {age_data.age=0;} // Else statement ensures infinite loop 
		}
	}
}

// OTHER FUNCTIONS -----------------------------------------------------------|
