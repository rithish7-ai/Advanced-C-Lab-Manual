EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:
#include <stdio.h>

int main() {
    int num;
    printf("Enter a number (0-9): ");
    scanf("%d", &num);

    switch (num) {
        case 0:
            printf("zero\n");
            break;
        case 1:
            printf("one\n");
            break;
        case 2:
            printf("two\n");
            break;
        case 3:
            printf("three\n");
            break;
        case 4:
            printf("four\n");
            break;
        case 5:
            printf("five\n");
            break;
        case 6:
            printf("six\n");
            break;
        case 7:
            printf("seven\n");
            break;
        case 8:
            printf("eight\n");
            break;
        case 9:
            printf("nine\n");
            break;
        default:
            printf("Invalid input! Please enter a number between 0 and 9.\n");
    }

    return 0;
}





Output:

![image](https://github.com/user-attachments/assets/fe4b92a5-541f-46da-97de-b5708561ed36)







Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
#include <stdio.h>

int main() {
    int freq[10] = {0}; 
    char ch;

    printf("Enter digits (press Enter to finish):\n");

    while ((ch = getchar()) != '\n') {
        if (ch >= '0' && ch <= '9') {
            freq[ch - '0']++; 
        }
    }

    for (int i = 0; i < 10; i++) {
        if (i <= 3) {
            printf("%d ", freq[i]);
        } else {
            printf("0 "); 
        }
    }

    printf("\n");
    return 0;
    }




Output:

![image](https://github.com/user-attachments/assets/e2024886-8f7a-4f5c-b581-82601e10eff2)







Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:

#include <stdio.h>
#include <string.h>
#include <stdlib.h>
void swap(char *x, char *y) {
    char temp = *x;
    *x = *y;
    *y = temp;
}
void sortString(char *str) {
    int n = strlen(str);
    for (int i = 0; i < n-1; i++) {
        for (int j = i+1; j < n; j++) {
            if (str[i] > str[j]) {
                swap(&str[i], &str[j]);
            }
        }
    }
}

int nextPermutation(char *str) {
    int n = strlen(str);
    int i = n - 2;
    while (i >= 0 && str[i] >= str[i+1])
        i--;

    if (i < 0) return 0; 
    int j = n - 1;
    while (str[j] <= str[i])
        j--;
    swap(&str[i], &str[j]);
    int left = i + 1, right = n - 1;
    while (left < right) {
        swap(&str[left], &str[right]);
        left++;
        right--;
    }

    return 1; 
}

int main() {
    char str[100];

    printf("Enter the string: ");
    scanf("%s", str);

    sortString(str);

    do {
        printf("%s\n", str);
    } while (nextPermutation(str));

    return 0;
}







Output:


![image](https://github.com/user-attachments/assets/7f68ef5e-4589-4e81-980c-60b1f74a094d)







Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
#include <stdio.h>

int main() {
    int n, num = 1;
    printf("Enter N: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {  
        for (int j = 1; j <= i; j++) {  
            printf("%d ", num);
            num++;
        }
        printf("\n");
    }

    return 0;
}







Output:
![image](https://github.com/user-attachments/assets/57eafad3-0301-4e6d-83ec-9d44188b0b69)







Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:

#include <stdio.h>
int findSquare() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num * num;  
}

int main() {
    int square;
    square = findSquare();
    
    printf("Square of the given number is: %d\n", square);

    return 0;
}






Output:


![image](https://github.com/user-attachments/assets/2244d71e-bd74-407c-a7fc-aca252a75767)







Result:
Thus, the program is verified successfully



























