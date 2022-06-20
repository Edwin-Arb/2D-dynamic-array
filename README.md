#include <iostream>
using namespace std;

void main()
{
	int rows;
	int cols;

	cout << "enter rows count: " << endl;
	cin >> rows;
	cout << "enter cols count: " << endl;
	cin >> cols;
	cout << endl;

	int** arr = new int* [rows];

	for (int i = 0; i < rows; i++)
	{
		 arr[i] = new int[cols];
	}

	for (int i = 0; i < rows; i++)
	{
		for (int j = 0; j < cols; j++)
		{
			arr[i][j] = rand() % 20;
		}
	}
	for (int i = 0; i < rows; i++)
	{
		for (int j = 0; j < cols; j++)
		{
			cout << arr[i][j]<<"\t";
		}
		cout << endl;
	}
	for (int i = 0; i < rows; i++)
	{
		delete[] arr[i];
	}
	delete[] arr;
}
