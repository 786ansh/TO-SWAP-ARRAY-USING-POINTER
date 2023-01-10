# TO-SWAP-ARRAY-USING-POINTER
 #include <stdio.h>
int main()
{
    int i,a[25],b[25];
    printf("enter the elements of Ist array\n");
    for(i=0;i<7;i++)
    {
        scanf("%d",&a[i]);
    }

    printf("enter the elements of 2nd array\n");
    for(i=0;i<7;i++)
    {
        scanf("%d",&b[i]);
    }
    printf("************BEFORE SWAPPING*****************\n");
    printf("array 1:\n");
     for(i=0;i<7;i++)
    {
        printf("%d",a[i]);
    }
    
     printf("\narray 2:\n");
     for(i=0;i<7;i++)
    {
        printf("%d",b[i]);
    }
    
    int temp;
    int(*p)[7];
    int(*q)[7];
    p=a,q=b;
    for(i=0;i<=6;i++)
    {
       temp=(*(*q+i));
      (*(*q+i))=(*(*p+i));
      (*(*p+i))=temp;
        
  }
  
  printf("\n************AFTER SWAPPING***************\n");
  printf("array 1:\n");
     for(i=0;i<7;i++)
    {
        printf("%d ",a[i]);
    }
    
     printf("\narray 2:\n");
     for(i=0;i<7;i++)
    {
        printf("%d ",b[i]);
    }
    
    
    return 0;
}
