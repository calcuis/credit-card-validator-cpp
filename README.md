## credit card number validator
The provided C++ code is a credit card number validator. It prompts the user to enter a credit card number and then performs validation on that number.

The code begins by including the necessary header file `<iostream>`, which is required for input/output operations. It then declares three function prototypes: `getDigit`, `sumOddDigits`, and `sumEvenDigits`. These functions are used to calculate the sum of odd digits, the sum of even digits (after performing a specific calculation on them), and to retrieve the individual digits of a number respectively.

In the main function, the program starts by displaying a header message: "********** card # validator **********". It then prompts the user to enter a credit card number using the `std::cin` object and stores the input in the variable `cardNumber`.

The program calculates the result of the validation by adding the sum of even digits and the sum of odd digits. The `sumEvenDigits` and `sumOddDigits` functions are called with `cardNumber` as the argument, and their results are added together and stored in the result variable.

Next, the program checks if the result is divisible by 10 (i.e., `result % 10 == 0`). If it is, the program outputs a message indicating that the card number is valid. Otherwise, it outputs a message indicating that the card number is not valid.

Finally, the main function returns 0 to indicate successful program execution.

The `getDigit` function takes an integer number as an argument, extracts the last two digits of the number using the modulo operator (`number % 10`) and integer division (`number / 10 % 10`), and returns their sum.

The sumOddDigits function takes a string cardNumber as an argument. It initializes a variable sum to 0 and then iterates over the characters of `cardNumber` starting from the last character (i.e., `cardNumber.size() - 1`) and moving backwards by 2 positions in each iteration. In each iteration, it converts the character to an integer by subtracting the character '0' (the ASCII value of '0') and adds the resulting integer to the sum. Finally, it returns the calculated sum.

The `sumEvenDigits` function is similar to `sumOddDigits` but with some additional calculations. It also takes a string `cardNumber` as an argument. It initializes a variable sum to 0 and then iterates over the characters of `cardNumber` starting from the second-to-last character (i.e., `cardNumber.size() - 2`) and moving backwards by 2 positions in each iteration.

In each iteration, it performs the following steps:

1) It converts the character to an integer by subtracting the character '0' (the ASCII value of '0').

2) It multiplies the resulting integer by 2.

3) It passes the multiplied value to the `getDigit` function, which extracts the last two digits of the number and returns their sum.

4) It adds the returned sum to the sum.

Finally, the `sumEvenDigits` function returns the calculated sum.

## reference
Luhn algorithm: 
https://en.wikipedia.org/wiki/Luhn_algorithm
