# 5Functions-ObjectiveC
A function is a name associated with a chunk of code. 

# When should I use a function?

# How do I write and use a function?

# How functions work together

# Local variables, frames, and the stack

# Recursion

# Looking at the frames in the debugger

# return

When you return 0 to the system, you are saying “Everything went OK.” If you are terminating the program because something has gone wrong, you’ll return 1.

# Global and static variables

## Global Variables

- Global variables are the ones that you can access from any function, any time.
- Any complex program will involve dozens of files containing different functions.
- Global variables are available to the code in every one of those files

``` c
#include <stdio.h>
#include <stdlib.h>
// Declare a global variable
float lastTemperature;
float fahrenheitFromCelsius(float cel)
{
    lastTemperature = cel;
    float fahr = cel * 1.8 + 32.0;
    printf("%f Celsius is %f Fahrenheit\n", cel, fahr);
    return fahr;
}
int main(int argc, const char * argv[])
{
float freezeInC = 0;
float freezeInF = fahrenheitFromCelsius(freezeInC);
printf("Water freezes at %f degrees Fahrenheit\n", freezeInF); printf("The last temperature converted was %f\n", lastTemperature); return EXIT_SUCCESS;
}
```

## Static Variables

- Sometimes sharing a variable between different files is what you want.
- But as you can imagine, having a variable that can be accessed by multiple functions can also lead to great confusion.
- To deal with multiple functions, we have static variables. 
- A static Variable is like a global variable in that it is declare outside of any function. However a static variable is only accessible from the code in the file where it was declared. So you get the non-local, "exist outside of any function" benefit while avoiding the "you touched my variable!" issue.

``` c
// Declare a static variable 
static float lastTemperature;
```




### 


