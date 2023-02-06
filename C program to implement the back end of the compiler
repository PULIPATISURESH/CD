#include<stdio.h>
#include<conio.h>
#include<string.h>
int main()
{
	int n,i,j;
	char a[50][50];
	printf("enter the no: intermediate code:");
	scanf("%d",&n);
	for(i=0;i<n;i++)
	{
		printf("enter the 3 address code:%d:",i+1);
		for(j=0;j<6;j++)
		{
			scanf("%c",&a[i][j]);
		}
	}
	printf("the generated code is:");
	for(i=0;i<n;i++)
	{
		printf("\n mov %c,R%d",a[i][3],i);
		if(a[i][4]=='-')
		{
			printf("\n sub %c,R%d",a[i][5],i);
		}
		if(a[i][4]=='+')
		{
			printf("\n add %c,R%d",a[i][5],i);
		}
		if(a[i][4]=='*')
		{
			printf("\n mul %c,R%d",a[i][5],i);
		}
		if(a[i][4]=='/')
		{
			printf("\n div %c,R%d",a[i][5],i);
		}
		printf("\n mov R%d,%c",i,a[i][1]);
		printf("\n");
	}
	return 0;
}

Output:
enter the no: intermediate code:2
enter the 3 address code:1:a=b+c
enter the 3 address code:2:d=n*d
the generated code is:
 mov b,R0
 add c,R0
 mov R0,a

 mov n,R1
 mul d,R1
 mov R1,d
