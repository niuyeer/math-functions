#include <stdio.h>
#include "time.h"//clock()函数获取系统时间
#include <stdlib.h>

#define SIZE 2
float array[SIZE][SIZE];

float detArray( int n, float a[SIZE][SIZE] )// n is the dimension // a is the array
{
    float b[SIZE][SIZE] = {{0}};
    int i = 0, j = 0;
    float det = 0;
    int x = 0, c = 0, p = 0;
    if (n == 1)
        return a[0][0];
    for (i = 0; i <= n-1; i++)
    {
        for (c = 0; c < n - 1; c++)
        {
            for (j = 0; j < n - 1; j++)
            {
                if (c < i) {
                    p = 0;
                }
                else {
                    p = 1;
                }
                b[c][j] = a[c + p][j + 1];
            }
        }
        if (i % 2 == 0) {
            x = 1;
        }
        else {
            x = (-1);
        }
        float t=detArray(n-1, b);
        det += a[i][0] * t * x;
    }
    return det;
}

int main(int argc, char ** argv)
{
    srand((unsigned)time(NULL));
    int n,m,a;
    
    // square matrix array
    
    for (n=0;n<SIZE;n++)
    {
        for(m=0;m<SIZE;m++)
        {
            while (1) {
                a=rand()%10;
                if (a!=0) {
                    
                    // printf("%d\n",a);
                    break;
                }
            }
            array[n][m]=a;
           
        }
    }
    printf("array is \n");
    for (n=0;n<SIZE;n++)
    {
        
        for(m=0;m<SIZE;m++)
        {
            printf(" %f ",array[n][m]);
        }
        printf("\n");
    }
    printf("det of array is %f\n",detArray(SIZE,array));
}
