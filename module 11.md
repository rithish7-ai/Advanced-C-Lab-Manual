

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
#include <stdio.h>
int greatest(int, int, int);

int main() {
    int num1, num2, num3;
    scanf("%d %d %d", &num1, &num2, &num3);
    printf("The greatest number is: %d\n", greatest(num1, num2, num3));

    return 0;
}
int greatest(int a, int b, int c) {
    if (a >= b && a >= c) {
        return a;
    } else if (b >= a && b >= c) {
        return b;
    } else {
        return c;
    }
}


Output:
![image](https://github.com/user-attachments/assets/42b8db3a-427a-4bf9-8ddd-580c58758561)


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 write a program to print the maximum values for the AND, OR and XOR comparisons

Aim:
To write a program to print the maximum values for the AND, OR and XOR comparisons
Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:

#include <stdio.h>

void calculate_the_max(int n, int k) {
    int a = 0, o = 0, x = 0;
    for (int i = 1; i <= n; i++) {
        for (int j = i + 1; j <= n; j++) {
            int and_result = i & j;
            int or_result = i | j;
            int xor_result = i ^ j;

            if (and_result < k && and_result > a) {
                a = and_result;
            }
            if (or_result < k && or_result > o) {
                o = or_result;
            }
            if (xor_result < k && xor_result > x) {
                x = xor_result;
            }
        }
    }
    printf("Maximum AND less than %d: %d\n", k, a);
    printf("Maximum OR less than %d: %d\n", k, o);
    printf("Maximum XOR less than %d: %d\n", k, x);
}

int main() {
    int n, k;
    scanf("%d %d", &n, &k);
    calculate_the_max(n, k);

    return 0;
}


Output:
![image](https://github.com/user-attachments/assets/73fe204a-0205-4100-b0f2-d87aabfc4304)

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
#include <stdio.h>

void handleRequest1() {
    printf("Handling request 1: Displaying information.\n");
}

void handleRequest2() {
    printf("Handling request 2: Performing a calculation.\n");
}

void handleRequest3() {
    printf("Handling request 3: Exiting the program.\n");
}

int main() {
    int choice;

    while (1) {
        printf("\nRequest Menu:\n");
        printf("1. Request 1: Display Information\n");
        printf("2. Request 2: Perform Calculation\n");
        printf("3. Request 3: Exit Program\n");
        printf("Enter your choice (1-3): ");
        scanf("%d", &choice);
        switch (choice) {
            case 1:
                handleRequest1();  
                break;
            case 2:
                handleRequest2();  
                break;
            case 3:
                handleRequest3();
                return 0;
            default:
                printf("Invalid choice. Please enter a number between 1 and 3.\n");
        }
    }

    return 0;
}



Output:
![image](https://github.com/user-attachments/assets/0293e5b7-e2dd-4a0c-a0ec-02d4640b1d86)



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
#include <stdio.h>

int main() {
    int n, sum = 0;
    scanf("%d", &n);

    int arr[n];  
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    for (int i = 0; i < n; i++) {
        sum += arr[i]; 
    }
    printf("The sum of the elements in the array is: %d\n", sum);

    return 0;
}




Output:
![image](https://github.com/user-attachments/assets/9a99adc4-09eb-47c4-ad7f-7d8962ec60b7)


 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
#include <stdio.h>
#include <ctype.h> 

int main() {
    char sentence[1000];
    int wordCount = 0, i = 0;
    char ch;
    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin); 
    while (sentence[i] != '\0') {
 
        if (!isspace(sentence[i]) && (i == 0 || isspace(sentence[i - 1]))) {
            wordCount++;
        }
        i++;
    }
    printf("The number of words in the sentence is: %d\n", wordCount);

    return 0;
}


Output:
![image](https://github.com/user-attachments/assets/ac22d2d9-8814-4e93-9414-6589c15db925)


Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
