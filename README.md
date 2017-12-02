#include <stdio.h>
swap1(int*x,int*y);
int main(void)
{
	int n, i, k, index;
	int a[100];
	
	printf("input the number of your NUMBERs:\n");
	scanf("%d",&n);
	
	printf("input the NUMBERs:\n");
	for(i=0;i<n;i++)
	{
		scanf("%d",&a[i]);
	}
	
	
	for(i=0;i<n-1;i++)
	{
		for(k=i+1;k<n;k++)
		{
			index=i;
			
			if(a[k] < a[index])
			{
				index=k;
			}
			
			if(index!=i)
			{
				swap1(&a[i],&a[index]);
			}
		}
	}
	
	for(i=0;i<n;i++)
	{
		printf("%d\n",a[i]);
	}
}

swap1(int*x,int*y)
{
	int temp=*x;
	*x=*y;
	*y=temp;
}

