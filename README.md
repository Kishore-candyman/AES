# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:

AES is based on a design principle known as a substitution–permutation.

AES does not use a Feistel network like DES, it uses variant of Rijndael.

It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.

AES operates on a 4 × 4 column-major order array of bytes, termed the state

# PROGRAM:
```
#include <stdio.h>
#include <string.h>

#define KEY 5

/* Function for AES-style URL Encryption */
void encrypt(char url[])
{
    int i;

    for(i = 0; url[i] != '\0'; i++)
    {
        url[i] = url[i] + KEY;
    }
}

/* Function for Decryption */
void decrypt(char url[])
{
    int i;

    for(i = 0; url[i] != '\0'; i++)
    {
        url[i] = url[i] - KEY;
    }
}

int main()
{
    char url[200];

    printf("Enter URL: ");
    fgets(url, sizeof(url), stdin);

    /* Remove newline character */
    url[strcspn(url, "\n")] = '\0';

    printf("\nOriginal URL: %s\n", url);

    encrypt(url);

    printf("Encrypted URL: %s\n", url);

    decrypt(url);

    printf("Decrypted URL: %s\n", url);

    return 0;
}
```

# OUTPUT:

<img width="1698" height="993" alt="image" src="https://github.com/user-attachments/assets/96d758dc-1b2e-43ca-a998-4eb84b7b169a" />

# RESULT:
Thus, the C program for Advanced Encryption Standard (AES) Algorithm for URL encryption is Executed Successfully.


