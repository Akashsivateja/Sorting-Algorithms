//Sorting-Algorithms.
//1.Bubble sort algorithm.
#include <stdio.h>
#include <string.h>
int main() 
{
    int n;
    printf("Enter the size of the array: ");
    scanf("%d",&n);
    int a[n],b[n];
    int swap=0, comparissons=0;
    printf("Enter the array to be sorted: ");
    for(int i=0;i<n;i++) 
    {
        scanf("%d",&a[i]);
    }
    for(int i=0;i<n-1;i++) 
    {
        for(int j=0;j<n-i-1;j++) 
        {
            comparissons++;
            if(a[j]>a[j+1]) 
            {
                swap++;
                int temp = a[j];
                a[j] = a[j+1];
                a[j+1] = temp;
            }
        }
        printf("pass %d: ", i+1);
        for(int k=0; k<n; k++) {
            printf("%d ", a[k]);
        }
        printf("comparissons: ");
        printf("%d ",comparissons);
        printf("swaps: ");
        printf("%d ",swap);
        printf("\n");
    }
    printf("Sorted array: ");
    for(int i=0;i<n;i++) 
    {
        printf("%d ",a[i]);
    }
    printf("\n");
    printf("Total comparisons during sorting: %d\n",comparissons);
    printf("Total swaps during sorting: %d\n",swap);
    return 0;
}
