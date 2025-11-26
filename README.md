# string-operations
c

#include <stdio.h>
#include <string.h>

int main() {
    char str1[100], str2[100], copyStr[100];

    printf("Enter first string: ");
    fgets(str1, sizeof(str1), stdin);

    printf("Enter second string: ");
    fgets(str2, sizeof(str2), stdin);

    str1[strcspn(str1, "\n")] = 0;
    str2[strcspn(str2, "\n")] = 0;

    
    printf("\nLength of first string: %lu\n", strlen(str1));


    strcpy(copyStr, str1);
    printf("Copied string: %s\n", copyStr);
    
    if (strcmp(str1, str2) == 0)
        printf("Both strings are SAME.\n");
    else
        printf("Strings are DIFFERENT.\n");

    return 0;
}
