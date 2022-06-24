# Robotic-Arm-Diary


Robotic Arm Code

}

int main(void)
{
    OSC_config();               // Configure internal oscillator for 48 MHz
    UBMP4_config();             // Configure on-board UBMP4 I/O devices
    
    // Servo output pin configuration
    TRISC = 0b00000010;         // Set H1 as output for Servo1
    TRISC = 0b00000100;         // Set H2 as output for Servo2
	
    while(1)
	{
        // Pulse timing test code
//        servo_pulse(SERVO1,servo1Pos);
        
        // Read pushbuttons and adjust servo position
        if(SW5 == 0 && servo1_pos > 0)
        {
            servo1_pos --;
        }
        
        if(SW4 == 0 && servo1_pos < 255)
        {
            servo1_pos ++;
        }

        // Pulse timing test code
//        servo_pulse(SERVO2,servo2Pos);
        
        // Read pushbuttons and adjust servo position
        if(SW3 == 0 && servo2_pos > 0)
        {
            servo2_pos --;
        }
        
        if(SW2 == 0 && servo2_pos < 255)
        {
            servo2_pos ++;
        }
        
//        // Delay between servo pulses
//        __delay_ms(15);
        
        // Delay between pushbutton updates
        __delay_ms(4);

        
        // Activate bootloader if SW1 is pressed.
        if(SW1 == 0)
        {
            RESET();
        }
    }
}

/* Learn More - Program Analysis Activities
 * 
 * 1. 
 */
 
 
 Diary:
 
This Is Where my progress of my robotic arm project

"Quick Note that there were pictures but they were lost"

June 1: i had to make something interesting for my project, since most people are doing cars then i might as well do something different. i have to come up with an idea 

June 2: Just came up with an idea! what if i make a robotic arm i said to myself. i found this one video on youtube that shows a simple robotic arm that can move automatically.

June 3 - 4: basically i was browsing for the right kit to make my robotic arm this would surely do since making an arm was my passion.

June 5: i bought the materials and was coming up with a plan

June 6: when i came to school i was confident that i would get the arm itself assembled in only one day, i was basically wrong

June 7: I Got Stuck in placing the 3rd motor base, a single screw would not come in but i was calm and i tried to place it in and at the end it worked

June 8: This time i got stuck in the crane part because of a screw that did not fit so i ended up adding tape instead. it should hopefully hold it in place
 
June 9: spent the whole period working on it. i then got a brain idea, "i wonder if Aurdino code ( which is actually what the robotic arm is supposed to run on) is compatible with Microcontroller code". i was excited

June 10: to put it to the test i asked Mr Lam if that was possible and he said No so i was now stumped because that technically means i have to make the whole code from scratch

June 11  - 14: Spent four days on how to try and connect the servo motors to my ubmp4

June 15 - 16: i was in a sort of overthinking moment in this day because i was thinking about the code first before the basics and obviously i dont want to fail

June 17: It Is Getting Close so thats when i started panicking because i still could not figure out the code, thats when Cedric told me to understand how the servo works and that i should instead connect all the motors to each button so make it manual and not automatic. he basically saved me

June 18 - 19: started learniung about how the servo works and then i followed some internet tutorials

June 20: now i need to start the program itself since i have a deadline to meet and i only have a few days left

June 21: The Code is halfway complete, i programmed one servo to function now i just have to figure out the rest of them

June 22: The Code is finished so the robotic arm is done and is ready to be presented, i just have to modify the code itself

