# Port.initi.function
SYSCTL_RCGCGPIO_R|=0x20; //INTIALIZE THE CLOCK OF PORTF
while((SYSCTL_PRGPIO_R & 0x20)==0); //delay
GPIO_PORTF_LOCK_R = 0x4C4F434B; //unlocking the ports have the same value
GPIO_PORTF_CR_R |= 0x0E; //Allow changing pin 3,2,1 in portF
GPIO_PORTF_AMSEL_R &=~0x0E; //disable the analog function
GPIO_PORTF_PCTL_R &=~0x0000FFF0;
GPIO_PORTF_AFSEL_R &=~0x0E; //disable the alternate function
GPIO_PORTF_DIR_R |= 0x0E; //Pin1,2,3 is output
GPIO_PORTF_DEN_R |=0x0E;
GPIO_PORTF_DATA_R &=~0x0E; //intialize pins 1,2,3 to be off
}


define set_bit(reg,bit) reg |= 1<<bit
define clear_bit(reg,bit) reg &= ~(1<<bit)
define toggle_bit(reg,bit) reg |= 1<<bit
define read_bit(reg,bit) reg |= 1<<bit 

                                      
void port_init(unsignedchar port_name)
    switch(port_name){
    case'A':
     {  
        set_bit (SYSCTL_RCGCGPIO_R,0)                             
        while((SYSCTL_PRGPIO_R & 0x01)==0); //delay                              
        GPIO_PORTA_LOCK_R = 0x4C4F434B;                              
        GPIO_PORTA_CR_R |= 0xFF;
        GPIO_PORTA_DEN_R |=0xFF;                              
                                      
                                      
                                                            
               
                                      }  
    case'A':
     {  
        set_bit (SYSCTL_RCGCGPIO_R,0)                             
        while((SYSCTL_PRGPIO_R & 0x01)==0); //delay                              
        GPIO_PORTA_LOCK_R = 0x4C4F434B;                              
        GPIO_PORTA_CR_R |= 0xFF;
        GPIO_PORTA_DEN_R |=0xFF;                              
                                      
                                      
                                      
                                      
                                      
     }       
      case'A':
     {  
        set_bit (SYSCTL_RCGCGPIO_R,0)                             
        while((SYSCTL_PRGPIO_R & 0x01)==0); //delay                              
        GPIO_PORTA_LOCK_R = 0x4C4F434B;                              
        GPIO_PORTA_CR_R |= 0xFF;
        GPIO_PORTA_DEN_R |=0xFF;                              
                                      
                                      
                                      
                                      
                                      
     }       
      case'A':
     {  
        set_bit (SYSCTL_RCGCGPIO_R,0)                             
        while((SYSCTL_PRGPIO_R & 0x01)==0); //delay                              
        GPIO_PORTA_LOCK_R = 0x4C4F434B;                              
        GPIO_PORTA_CR_R |= 0xFF;
        GPIO_PORTA_DEN_R |=0xFF;                              
                                      
                                      
                                      
                                      
                                      
     }                                       
