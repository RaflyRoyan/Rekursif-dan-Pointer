# Rekursif-dan-Pointer
#include <stdio.h>

int pangkat(int x, int y){
	if(y == 0){
		return 1;
	}
	else{
		return x * pangkat(x,y-1);
	}
}
main(){
	int x, y;
	
	printf("Bilangan yang dipangkatkan : ");
	scanf("%d", &x);
	printf("Pangkat Bilangan : ");
	scanf("%d", &y);
	printf("Hasil Bilangan %d pangkat %d adalah %d\n", x, y, pangkat(x,y));
	printf("Hasil bilangan pangkat = %d\n", pangkat(x,y));
	
	int i = pangkat(x,y);
	int *ptr;
	int **pptr;
	
	ptr = &i;
	pptr = &ptr;
	
	printf("Slot memori bilangan pangkat = %d\n", *ptr);
	printf("Slot memori bilangan pangkat menggunakan double pointer = %d\n", **pptr);
}
