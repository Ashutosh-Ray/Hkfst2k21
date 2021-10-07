#include <stdio.h>
#include <stdlib.h>

void flip(int array[], int i)
{
	int temp, start = 0;
	while (start < i) {
		temp = array[start];
		array[start] = array[i];
		array[i] = temp;
		start++;
		i--;
	}
}

int findMax(int array[], int n)
{
	int mi, i;
	for (mi = 0, i = 0; i < n; ++i)
		if (array[i] > array[mi])
			mi = i;
	return mi;
}


void pancakeSort(int* array, int n)
{
	for (int curr_size = n; curr_size > 1;
								--curr_size)
	{

		int mi = findMax(array, curr_size);

		if (mi != curr_size - 1) {

			flip(array, mi);

			flip(array, curr_size - 1);
		}
	}
}


void printArray(int array[], int n)
{
	for (int i = 0; i < n; ++i)
		printf("%d ", array[i]);
}


int main()
{
	int array[] = { 32, 19, 83, 67, 98, 0, 17 };
	int n = sizeof(array) / sizeof(array[0]);

	pancakeSort(array, n);

	puts("Sorted Array ");
	printArray(array, n);

	return 0;
}
