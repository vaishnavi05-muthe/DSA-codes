# DSA-codes
#include <stdio.h>
//insertion sort
int main()
{
    int a[20], n, i, j, k, temp;
    printf("Enter size of an array:");
    scanf("%d", &n);
    printf("Enter the array elements:");
    for (int i = 0; i < n; i++)
    {
        scanf("%d", &a[i]);
    }
    for (i = 1; i < n; i++)
    {
        for (j = 0; j < i; j++)
        {
            if (a[j] > a[i])
            {
                temp = a[i];
                for (k = i - 1; k >= j; k--)
                {
                    a[k + 1] = a[k];
                }
                a[j] = temp;
            }
        }
        printf("After pass %d:\n", i);
        for (k = 0; k < n; k++)
        {
            printf("%d ", a[k]);
        }
        printf("\n");
    }
    printf("Sorted element:\n");
    for (i = 0; i < n; i++)
    {
        printf("%d\n", a[i]);
    }
    return 0;
}
