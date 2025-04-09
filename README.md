#include <iostream>
#include <ctime>
using namespace std;

void main()
{

	setlocale(LC_ALL, "ru");


	srand(time(NULL));

	int const SIZE = 5;
	int arr[SIZE];
	bool allr;

	for (int i = 0; i < SIZE; )
	{
		allr = false;
		int nrv = rand() % 10;

		for (int j = 0; j < i; j++)
		{
			if (arr[j] == nrv)
			{
				allr = true;
				break;
			}

		}

		if (!allr)
		{
			arr[i] = nrv;
			i++;
		}

	}


		for (int i = 0; i < SIZE; i++)
		{
			cout << arr[i] << endl;
		}

	int min = arr[0];
	for (int i = 1; i < SIZE; i++)
	{
		if (arr[i] < min)
		{
			min = arr[i];
			
		}
		
	}
	cout << "Наименьшее число массива" << min << endl;
}
