# FirstRepo
#include <stdio.h>
#include <stdlib.h>
#include <setjmp.h>

int main(int argc, char const *argv[]) {
 	jmp_buf env;
 	int val;
 	int colet;

 	val = setjmp(env);

 	if( val != 0) {

 		printf("fake return %d\n", val);
 		exit(0);
 	}
 	printf("true return\n");
 	longjmp(env, 4242)
 	return 0;
 }
