# 1	Find the largest and second-largest elements
```c
#include<stdio.h>
#include<limits.h>
void main()
{
    int arr[]={1,12,3,4,5,6,7,18,9};
    int le=sizeof(arr)/sizeof(arr[0]);
    int l=INT_MIN,sl=INT_MIN;
    for(int i=1;i<le;i++)
    {
        if(l<arr[i])
        {
            sl=l;
            l=arr[i];
        }
        if(sl<arr[i] && l!=arr[i])
            sl=arr[i];
    }
    printf("%d and %d",l,sl);
}
```
# 2	Find the missing number from 1 to N
```c
#include<stdio.h>

void main()
{
    int arr[]={9,1,2,3,4,5,6,8};
    int le=sizeof(arr)/sizeof(arr[0]);
    int Xor_sum=0;
    for(int i=0;i<le;i++)
    {
        Xor_sum ^= arr[i] ^ (i+1);
    }
    Xor_sum ^= (le+1);
    printf("Missing Number is %d",Xor_sum);
}
```
# 3	Find duplicate elements in an array
```c
```
# 4	Move all zeros to the end
```c
#include<stdio.h>

void main()
{
    int arr[]={9,0,2,3,0,5,0,8};
    int i,le=sizeof(arr)/sizeof(arr[0]);
    int c=0;
    for(i=0;i<le;i++)
    {
        if(arr[i]!=0)
            arr[c++]=arr[i];
    }
    for(i=c;i<le;i++)
        arr[i]=0;
    for(i=0;i<le;i++)
        printf("%d ",arr[i]);
    
}
```
# 5	Rotate array by K positions
```c
#include<stdio.h>

void main()
{
    int arr[]={1,2,3,4,5,6,7,8,9};
    int i,l=sizeof(arr)/sizeof(arr[0]);
    int k;
    printf("Enter K value");
    scanf("%d",&k);
    k=k%l;
    while(k--)
    {
        int temp= arr[0];
        for(i=0;i<l;i++)
        {
            arr[i]=arr[i+1];
        }
        arr[l-1]=temp;        
    }
    for(i=0;i<l;i++)
        printf("%d ",arr[i]);
    
}
```
