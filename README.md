#include <iostream>
void Initializion(int arr[], int size);
void Show(int arr[], const int size);
void Found(int arr[], int size, int value);
int main()
{	
	srand(static_cast <unsigned> (time(nullptr)));
	const int size = 10;
	int arr[size];
	int value;
	Initializion(arr, size);
	Show(arr, size);
	std::cout << std::endl;
	std::cin >> value;
	Found(arr, size, value);
	

	
}
void Initializion(int arr[], int size)
{
	for (int i = 0; i < size; i++)
	{
		arr[i] = rand() % 100;
	}
}
void Show(int arr[], const int size)
{
	for (int i = 0; i < size; i++)
	{
		std::cout << arr[i] << " ";
	}
}
void Found(int arr[], int size, int value)
{
	bool isFound = false;
	for (int i = 0; i < size; i++)
	{
		if (value == arr[i])
		{
			isFound = true;
			break;
		}
	}
	if (isFound == true)
		std::cout << "your number here!";
	else if ( isFound == false)
		std::cout << "array has not your number";
}# 126
