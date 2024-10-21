# Experiment 06: Implementation of Pseudorandom Number Generation using Standard Library

## Aim:
To implement Pseudorandom Number Generation using the Standard Library.

## Algorithm:
1. **Step 1:** Get the number of random numbers to generate from the user.
2. **Step 2:** Read the minimum and maximum values for the random number range.
3. **Step 3:** Initialize the random seed using the current time.
4. **Step 4:** Generate a random number by calculating the remainder of division with the range (max - min + 1) and adding the minimum value.
5. **Step 5:** Repeat the random number generation for the specified count.
6. **Step 6:** Print each generated random number.
7. **Step 7:** End the program.

## Code:
```c
#include <stdio.h>

#define A 1664525
#define C 1013904223
#define M 4294967296 // 2^32

unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M;
}

int main() {
    unsigned int seed;
    int n, i;
    printf("  ***Pseudorandom number generator***\n\n");
    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("Random numbers:\n");
    for (i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }
    return 0;
}
```

## Output:
![image](https://github.com/user-attachments/assets/0ad5a318-5846-4d0b-91af-ac0e0c0ebc17)

## Result:
The program for Pseudorandom Number Generation is executed successfully


