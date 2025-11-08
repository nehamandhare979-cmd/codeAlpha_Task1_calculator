# codeAlpha_Task1_calculator
"Basic Calculator program using switch case in C"
# 💻 CodeAlpha Internship - Task 1

## 🧮 Basic Calculator Program (C Programming)

This is a simple *Calculator Program in C* language that performs the following basic arithmetic operations using a *switch case* statement:
- Addition
- Subtraction
- Multiplication
- Division

---

### 🧑‍💻 *Intern Details*
- *Name:* Neha Sunil Mandhare  
- *Student ID:* CA/SE1/4855  
- *Domain:* C Programming  
- *Internship Duration:* 10th November 2025 - 10th December 2025  

---

### ⚙ *Program Description*
The program allows the user to:
1. Select an operation (1–4)  
2. Enter two numbers  
3. The program performs the selected arithmetic operation and displays the result.  

If division by zero is attempted, the program displays an appropriate error message.

---

### 🧾 *C Program Code*
```c
#include <stdio.h>

int main() {
    float num1, num2, result;
    int choice;

    printf("------- Simple Calculator -------\n");
    printf("1. Addition\n");
    printf("2. Subtraction\n");
    printf("3. Multiplication\n");
    printf("4. Division\n");
    printf("Enter your choice (1-4): ");
    scanf("%d", &choice);

    printf("Enter first number: ");
    scanf("%f", &num1);
    printf("Enter second number: ");
    scanf("%f", &num2);

    switch(choice) {
        case 1:
            result = num1 + num2;
            printf("Result = %.2f\n", result);
            break;
        case 2:
            result = num1 - num2;
            printf("Result = %.2f\n", result);
            break;
        case 3:
            result = num1 * num2;
            printf("Result = %.2f\n", result);
            break;
        case 4:
            if (num2 != 0)
                result = num1 / num2;
            else {
                printf("Error! Division by zero not allowed.\n");
                return 0;
            }
            printf("Result = %.2f\n", result);
            break;
        default:
            printf("Invalid choice! Please select 1 to 4.\n");
    }

    return 0;
}

