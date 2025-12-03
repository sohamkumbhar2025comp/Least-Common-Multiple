# Least-Common-Multiple
#include <stdio.h>

int lcmDivide(int a, int b, int div) {
   if (a == 1 && b == 1)
        return 1;
 int divided = 0;

   if (a % div == 0) {
        a /= div;
        divided = 1;
    }
    if (b % div == 0) {
        b /= div;
        divided = 1;
    }
  if (divided)
        return div * lcmDivide(a, b, div);
return lcmDivide(a, b, div + 1);
}
int main() {
    int a, b;
  printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

  int result = lcmDivide(a, b, 2);
    printf("LCM = %d\n", result);

  return 0;
