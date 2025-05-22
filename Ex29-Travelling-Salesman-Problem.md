# Ex29 Travelling Salesman Problem
## DATE:
## AIM:
To write a C Program to implement Travelling Salesman Problem for finding shortest path.
## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
Program to implement Travelling Salesman Problem for finding shortest path
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/

#include<stdio.h>
int ary[10][10],visited[10],n,cost=0;
void get()
{
    int i,j;
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            scanf("%d",&ary[i][j]);
        }
        visited[i]=0;
    }
}
int least(int c)
{
    int i,nc=999;
    int min=999,kmin;
    for(i=0;i<n;i++)
    {
        if((ary[c][i]!=0) && (visited[i]==0))
            if(ary[c][i]<min)
            {
                min=ary[i][0]+ary[c][i];
                kmin=ary[c][i];
                nc=i;
            }
    }
    if(min!=999)
        cost+=kmin;
    return nc;
}
void mincost(int city)
{
    int ncity;
    int least(int);
    visited[city]=1;
    printf("%d -->",city+1);
    ncity=least(city);
    if(ncity==999)
    {
        ncity=0;
        printf("%d",ncity+1);
        cost+=ary[city][ncity];
        return;
    }
    mincost(ncity);
}
void put()
{
    printf("\n\nMinimum cost:%d\n ",cost);
}
int main()
{
    get();
    mincost(0);
    put();
    return 0;
}
```

## Output:

![Screenshot 2025-05-22 144634](https://github.com/user-attachments/assets/4fc0949b-2d54-4697-a3c0-9c79e5007674)


## Result:
Thus, the C program to implement Travelling Salesman Problem for finding shortest path is implemented successfully.
