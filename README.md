# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```c
#include <stdio.h>
int main() {
    int num = 44;  
    int shifts = 3; 
    int result = num << shifts;

    printf("Original number: %d\n", num);
    printf("After left shifting by 3 positions: %d\n", result);

    return 0;
}
```
## OUTPUT

![image](https://github.com/user-attachments/assets/652575ca-fe77-4409-bfa0-f365a3c47c9d)








## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.




 
 


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT


## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM
```c

#include <stdio.h>

int main() {
    int num1, num2;
    printf("Enter first number: ");
    scanf("%d", &num1);
     printf("Enter second number: ");
    scanf("%d", &num2);
    if (num1 == num2) {
        printf("The numbers are equal.\n");
    } else {
        printf("The numbers are not equal.\n");
    }

    return 0;
}

```

## OUTPUT
 ![image](https://github.com/user-attachments/assets/48ad37cf-8337-43dc-9d7b-eb932a7e41f5)
       
## RESULT

Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
 
 


# EX-18-STRING-LOWERCASE-CONVERSION
## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```c
#include <stdio.h>
#include <ctype.h>
int main() {
    char str[100];
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  
    for (int i = 0; str[i] != '\0'; i++) {
        str[i] = tolower(str[i]); 
    }
    printf("String in lowercase: %s", str);

    return 0;
}

```
## OUTPUT
![image](https://github.com/user-attachments/assets/daef5cdb-94f1-42d2-b1bd-dcb5a8d84829)




## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 
 


# EX-19-COUNT-OF-WORDS-IN-A-STRING
## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM
```c
#include <stdio.h>
#include <ctype.h>
int main() {
    char str[100];
    int i = 0, words = 0;
    char prevChar = ' ';
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    do {
        if (isspace(str[i]) || str[i] == '\0') {
            if (!isspace(prevChar)) {
                words++;
            }
        }
        prevChar = str[i];
        i++;
    } while (str[i - 1] != '\0');
    printf("Total number of words: %d\n", words);

    return 0;
}

```
## OUTPUT
![image](https://github.com/user-attachments/assets/0ab549a1-0cf7-414d-81c6-4e336016ae6a)





## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 


# EX  -20 -COMPARING TWO STRINGS
## AIM
write a Program to compare two strings without using strcmp().
## ALGORITHM
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
             flag and initialize it to 0, and i for indexing.      
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
            (i.e., can include spaces).
Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
            spaces in the second string).
Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):
•	If c1[i] is not equal to c2[i], set flag = 1.
•	Increment i by 1.
Step 7: After the loop, check the value of flag:
•	If flag == 0, print "strings are same".
•	Otherwise, print "strings are not same".
Step 8: End the program.

## PROGRAM
```c
#include <stdio.h>
int compareStrings(const char *str1, const char *str2) {
    while (*str1 != '\0' && *str2 != '\0') {
        if (*str1 != *str2) {
            return 0; // Strings are not equal
        }
        str1++;
        str2++;
    }
    return (*str1 == '\0' && *str2 == '\0');
}

int main() {
    char str1[100], str2[100];
    printf("Enter first string: ");
    fgets(str1, sizeof(str1), stdin);
    printf("Enter second string: ");
    fgets(str2, sizeof(str2), stdin);
    str1[strcspn(str1, "\n")] = '\0';
    str2[strcspn(str2, "\n")] = '\0';

    if (compareStrings(str1, str2)) {
        printf("The strings are equal.\n");
    } else {
        printf("The strings are not equal.\n");
    }

    return 0;
}

```

## OUTPUT
 ![image](https://github.com/user-attachments/assets/0e9c946c-7515-42e4-8914-d19c2e2171d5)


## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

