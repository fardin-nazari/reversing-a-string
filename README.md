#include<stdio.h>
#include<string.h>
#define MAX 100

int top = -1;
char stack[MAX];
char push(char string)
{
	if(top == (MAX-1))
		printf("there is stack overflow");
	else
		stack[++top] =string;
}
char pop()
{
	if(top == -1)
		printf("there is empty stack");
	else
		return stack[top--];
}
int main()
{
	char a[100];
	int i;
	printf("Enter the string : " );
	gets(a);
	for(i=0;i<strlen(a);i++)
		push(a[i]);
	for(i=0;i<strlen(a);i++)
		a[i]=pop();
	printf("Reversed string is : ");
	puts(a);
}
