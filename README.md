# Salting-Password-C_language
This C code requests the user for a password and then uses a "salting" method on it. Salting is a popular cryptography and security strategy in which random data is added to the input password before hashing to make it more resistant to attacks such as rainbow tables.

step:-1 
#include<stdio.h>
#include<string.h>
These lines provide the required header files for input/output operations (stdio.h) and string manipulation methods (string.h).

step:2:- void salting(char password[]); 
defines a function that accepts a character array (string) password as an input.

step:3-
Int main() { char password[100]; printf("Enter your password: ");

    scanf("%s", password); salting(password);
It declares a 100-element array password to hold the user's password.
It requests the user for their password.
It reads the user's input with scanf and saves it to the password array.
It calls the salting method and passes the password as an input.

step🔢
void salting(char password[])
{ char salt[]="microsoft@9896"; 
char newpass[200];

    strcpy(newpass,password);
    strcat(newpass,salt); 
    puts(newpass);
    }
It declares a character array salt containing a predetermined string that serves as the salt.
It declares a 200-character array newpass.
It uses strcpy to copy the password array's contents to the newpass array.
It uses strcat to append the salt array's contents to the newpass array.
The concatenated string is printed using puts.
    
step🕔
This software basically accepts a password as input, concatenates it with a predetermined salt string, and then outputs the result.
This salted string can then be used for other cryptographic processes, such as hashing, to increase security.


