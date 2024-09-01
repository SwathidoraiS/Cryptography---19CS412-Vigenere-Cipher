## Vigenere Cipher
Vigenere Cipher using with different key values

## AIM:
To develop a simple C program to implement Vigenere Cipher.

## DESIGN STEPS:
Step 1:
Design of Vigenere Cipher algorithnm

Step 2:
Implementation using C or pyhton code

Step 3:
Testing algorithm with different key values.

## PROGRAM:
```
#include <stdio.h>
#include <ctype.h>
#include <string.h>
void encipher();
void decipher();
int main()
{
int choice;
while(1)
{
printf("\n1. Encrypt Text");
printf("\n2. Decrypt Text");
printf("\n3. Exit");
printf("\n\nEnter Your Choice : ");
scanf("%d",&choice);
if(choice == 3)
exit(0);
else if(choice == 1)
encipher();
else if(choice == 2)
decipher();
else
printf("Please Enter Valid Option.");
}
}
void encipher()
{
unsigned int i,j;
char input[50],key[10];
printf("\n\nEnter Plain Text: ");
scanf("%s",input);
printf("\nEnter Key Value: ");
scanf("%s",key);
printf("\nResultant Cipher Text: ");
for(i=0,j=0;i<strlen(input);i++,j++)
{
if(j>=strlen(key))
{ j=0;
}
printf("%c",65+(((toupper(input[i])-65)+(toupper(key[j])-
65))%26));
}}
void decipher()
{
unsigned int i,j;
char input[50],key[10];
int value;
printf("\n\nEnter Cipher Text: ");
scanf("%s",input);
printf("\n\nEnter the key value: ");
scanf("%s",key);
for(i=0,j=0;i<strlen(input);i++,j++)
{
if(j>=strlen(key))
{ j=0; }
value = (toupper(input[i])-64)-(toupper(key[j])-64);
if( value < 0)
{ value = value * -1;
}
printf("%c",65 + (value % 26));
}
return 0;
}
```
## OUTPUT:
![Screenshot 2024-09-01 202704](https://github.com/user-attachments/assets/eef22f9f-d60a-421c-8b16-187f3c1d0f20)


## RESULT:
The program is executed successfully
