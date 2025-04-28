# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int M, N;

    // Input M and N
    printf("Enter the starting number (M): ");
    scanf("%d", &M);

    printf("Enter the ending number (N): ");
    scanf("%d", &N);

    // Validate range
    if (M > N) {
        printf("Invalid range: M should be less than or equal to N.\n");
        return 1;
    }

    printf("Even numbers between %d and %d are:\n", M, N);

    // Find the first even number >= M
    if (M % 2 != 0) {
        M++;  // Make M even if it's odd
    }

    for (int i = M; i <= N; i += 2) {
        printf("%d ", i);
    }

    printf("\n");

    return 0;
}

```

## OUTPUT:
![image](https://github.com/user-attachments/assets/2c3d1dc8-2fc1-4c89-9ae3-3daac2265829)











## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 


# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int M, N;

    // Input M and N
    printf("Enter the starting number (M): ");
    scanf("%d", &M);

    printf("Enter the ending number (N): ");
    scanf("%d", &N);

    // Validate range
    if (M > N) {
        printf("Invalid range: M should be less than or equal to N.\n");
        return 1;
    }

    printf("Even numbers between %d and %d are:\n", M, N);

    // Find the first even number >= M
    if (M % 2 != 0) {
        M++;  // Make M even if it's odd
    }

    // Print even numbers from M to N
    for (int i = M; i <= N; i += 2) {
        printf("%d ", i);
    }

    printf("\n");
    printf("Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully.\n");

    return 0;
}
```


## OUTPUT:

![image](https://github.com/user-attachments/assets/59025f0d-a398-499a-a435-2e02b60d594e)




## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 
 


# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:
```
#include <stdio.h>

// Function to add two numbers (with arguments, no return type)
void add(int a, int b) {
    int sum = a + b;
    printf("Sum: %d\n", sum);
}

// Function to subtract two numbers (with arguments, no return type)
void subtract(int a, int b) {
    int difference = a - b;
    printf("Difference: %d\n", difference);
}

int main() {
    int num1, num2;

    // Input from user
    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    // Function calls
    add(num1, num2);
    subtract(num1, num2);

    return 0;
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/eb474e25-ea30-4c3b-b303-cbc2abdf36ae)







## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 


# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int num, digit, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    // Make a copy of the number for loop control
    int temp = num;

    // Count digits to control the loop
    int count = 0;
    for (int x = temp; x > 0; x /= 10) {
        count++;
    }

    // Extract each digit using for loop
    for (int i = 0; i < count; i++) {
        digit = num % 10;       // Get last digit
        if (digit % 2 != 0) {   // Check if odd
            sum += digit;
        }
        num /= 10;              // Remove last digit
    }

    printf("Sum of odd digits: %d\n", sum);

    return 0;
}
```

## OUTPUT:


![image](https://github.com/user-attachments/assets/09c405de-5782-4eee-a019-b1c23766f8f2)


## RESULT:

Thus the program to find the sum of odd digits using for loop has been executed successfully.




# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:
```
#include <stdio.h>

// Function to calculate factorial (with return type and argument)
int factorial(int n) {
    int fact = 1;
    for(int i = 1; i <= n; i++) {
        fact *= i;
    }
    return fact;
}

int main() {
    int num;

    // Get input from user
    printf("Enter a positive integer: ");
    scanf("%d", &num);

    // Check for negative input
    if (num < 0) {
        printf("Factorial is not defined for negative numbers.\n");
    } else {
        int result = factorial(num);
        printf("Factorial of %d is: %d\n", num, result);
    }

    return 0;
}
```


## OUTPUT:
![image](https://github.com/user-attachments/assets/d10f1b0e-1418-475e-859e-6d5027cadbf4)



## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
