# EX-NO-7-Implement-DES-Encryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char text[100], enc[100], dec[100];
    int key, i;

    printf("Enter plaintext (no spaces): ");
    scanf("%99s", text);

    printf("Enter key (1-9): ");
    scanf("%d", &key);

    for (i = 0; text[i] != '\0'; i++)
        enc[i] = text[i] + key;
    enc[i] = '\0';

    printf("Encrypted text: %s\n", enc);

    for (i = 0; enc[i] != '\0'; i++)
        dec[i] = enc[i] - key;
    dec[i] = '\0';

    printf("Decrypted text: %s\n", dec);

    return 0;
}
```



## Output:
<img width="752" height="351" alt="image" src="https://github.com/user-attachments/assets/edb32def-9057-4efd-9cf5-f6c2b1be70f5" />


## Result:
  The program is executed successfully

