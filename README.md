
# include <stdio.h>
# include "dev.h" 
int main() {
    int num, size;
    //leap year
   printf("Enter a year: ");
   scanf("%d", &year);
   if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
        printf("%d is a leap year.\n", year);
        } else {
            printf("%d is not a leap year.\n", year);
        }

  //adams number
int reverse(int num) {
    int rev = 0;
    while (num > 0) {
        rev = rev * 10 + num % 10;
        num /= 10;
    }
    return rev;
}
    int num, revNum, sqOriginal, sqReversed;

    printf("Enter a number: ");
    scanf("%d", &num);

    revNum = reverse(num);

    sqOriginal = num * num;
    sqReversed = revNum * revNum;

    sqReversed = reverse(sqReversed);

    if (sqOriginal == sqReversed) {
        printf("%d is an Adam number.\n", num);
    } else {
        printf("%d is not an Adam number.\n", num);
    }

    //second largest element
    printf("Enter size of array: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements: ", size);
    for (int i = 0; i < size; i++)
        scanf("%d", &arr[i]);
    int second = secondLargest(arr, size);
    if (second == -1)
        printf("Not enough elements for second largest.\n");
    else
        printf("Second largest element: %d\n", second);
    
    return 0;
}
#efrgh