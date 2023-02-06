%{
#include<stdio.h>
#define NUMBER 400
#define COMMENT 401
#define STRINGS 402
#define IDENTIFIER 403
%}

/* Rules Section */
%%
[\t  ]+     ;
[0-9]+ | [0-9]*\.[0-9]+ { return NUMBER;}
#.* 			{ return COMMENT;}
\"[^ \"\n]*\"      	{ return STRINGS;}
[a-zA-Z][a-zA-Z0-9]+	{ return IDENTIFIER;}
\n			{ return '\n';}
%%

/* User Subroutine section */
main( )
{
	int val;
	while( val = yylex( ))
	printf("value is %d\n",val);
}

int yywrap( )
{
	return 1;
}
