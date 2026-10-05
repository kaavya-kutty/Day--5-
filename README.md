# Day--5-
#include <stdio.h>

int main() {
    int n, i, j;

  printf("Enter number of rows: ");
    scanf("%d", &n);

  // Upper half
    for (i = 1; i <= n; i++) {
        for (j = i; j < n; j++)
            printf(" ");

  printf("*");

   if (i > 1) {
            for (j = 1; j <= 2 * i - 3; j++)
                printf(" ");
            printf("*");
        }

  printf("\n");
    }

 // Lower half
    for (i = n - 1; i >= 1; i--) {
        for (j = n; j > i; j--)
            printf(" ");

   printf("*");

 if (i > 1) {
            for (j = 1; j <= 2 * i - 3; j++)
                printf(" ");
            printf("*");
        }

  printf("\n");
    }

return 0;
}
#include <stdio.h>

int main() {
    int n = 7;
    int i, j, spaces;

   // Upper half
    for (i = n; i >= 1; i -= 2) {
        spaces = (n - i) / 2;

   for (j = 1; j <= spaces; j++)
            printf("  ");

   for (j = 1; j <= i; j++)
            printf("* ");

 printf("\n");
    }

// Lower half
    for (i = 3; i <= n; i += 2) {
        spaces = (n - i) / 2;

  for (j = 1; j <= spaces; j++)
            printf("  ");

  for (j = 1; j <= i; j++)
            printf("* ");

 printf("\n");
    }
  return 0;
}
#include <stdio.h>

int main() {
    int n, i, j, space;
    int num;

   printf("Enter number of rows: ");
    scanf("%d", &n);

  for (i = 0; i < n; i++) {

 // Print spaces
        for (space = 0; space < n - i - 1; space++)
            printf("   ");

 num = 1;
        for (j = 0; j <= i; j++) {
            printf("%4d", num);

   num = num * (i - j) / (j + 1);
        }
  printf("\n");
    }

return 0;
}
