# c-algorithm-5
random sum
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <time.h>
#include <stdlib.h>
long long sum(int* a, int n);
int main() {
	int a[101], n;
	printf("정수 n을 입력하세요 : ");
	scanf("%d", &n);
	for (int i = 0; i < n; i++) {
		srand(time(NULL));
		a[i] = rand() % 100 + 1;
	}
	printf("\nsum = %d", sum(a, n));
}
long long sum(int* a, int n){
	int sum = 0;
	for (int i = 0; i < n; i++) {
		sum += a[i];
		printf("a[%d] : %d ", i, a[i]);
		if ((i + 1) % 10 == 0)
			printf("\n");
	}
	return sum;
}
