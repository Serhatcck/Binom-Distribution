# Binom-Distribution
Returns the binomial line according to the entered value

``` c
#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
int dizi[30][30] = {{1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1},{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},
{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},{1},};
void yazdir(int n)
{
    int i=0;
    int y=0;
    for(i=n-1;i>=0;i--)
    {
        printf("%d\t",dizi[i][y]);
        y++;
    }printf("\n");
}
int main()
{
    int i=0;
    int y=0;
    printf("Enter Row Number\n");
    int n;
    scanf("%d",&n);
    for(i=1;i<n-1;i++)
    {
        for(y=1;y<n;y++)
        {
            dizi[i][y] = dizi[i][y-1]+dizi[i-1][y];
        }
    }
    y=0;

    printf("All lines up to the value you entered are listed..\n");


    for(i=0;i<n+1;i++)
    {
        yazdir(i);
    }
    printf("\n\nJust write the line you entered..\n\n");
    for(i=n-1;i>=0;i--)
    {
        printf("%d\t",dizi[i][y]);
        y++;
    }printf("\n");
    system("pause");

}
```
