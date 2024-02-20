## Metodos de Ordenamiento de Algoritmos

En C++ es un concepto en donde los elementos de un arreglo son re-ordenados en un orden lógico. Este orden puede ir desde el más bajo al más alto y viceversa. El operador de comparación es utilizado para decidir el nuevo orden de elementos en la respectiva estructura de datos.

- #### Selection Sort
  Este funciona seleccionando repetidamente el elemento más pequeño (o más grande) de la porción sin clasificar de la lista y moviéndola a la lista clasificada.

###### Implementación de Selection Sort en C++


```C++
// C++ program for implementation of selection sort
#include <bits/stdc++.h>
using namespace std;
  
// Function for Selection sort
void selectionSort(int arr[], int n)
{
    int i, j, min_idx;
  
    // One by one move boundary of
    // unsorted subarray
    for (i = 0; i < n - 1; i++) {
  
        // Find the minimum element in
        // unsorted array
        min_idx = i;
        for (j = i + 1; j < n; j++) {
            if (arr[j] < arr[min_idx])
                min_idx = j;
        }
  
        // Swap the found minimum element
        // with the first element
        if (min_idx != i)
            swap(arr[min_idx], arr[i]);
    }
}
  
// Function to print an array
void printArray(int arr[], int size)
{
    int i;
    for (i = 0; i < size; i++) {
        cout << arr[i] << " ";
        cout << endl;
    }
}
  
// Driver program
int main()
{
    int arr[] = { 64, 25, 12, 22, 11 };
    int n = sizeof(arr) / sizeof(arr[0]);
  
    // Function Call
    selectionSort(arr, n);
    cout << "Sorted array: \n";
    printArray(arr, n);
    return 0;
}

  
// This is code is contributed by rathbhupendra
```
![0415_003](https://github.com/sofigrv13/M-todos-de-Ordenamiento-de-Algoritmos/assets/119021332/fdaec409-0c95-4e86-886a-8570dd65d035)

- #### Bubble Sort
 Bubble Sort u Ordenamiento Burbuja, funciona repetidamente intercambiando los elementos adyacentes si estos se encuentran en el orden erróneo. Este algoritmo no es apto para segmentos grande de datos comunmente y en el peor de los casos su complejidad es bastante alta. 

###### Implementación de Bubble Sort en C++
```C++
// Optimized implementation of Bubble sort
#include <bits/stdc++.h>
using namespace std;
 
// An optimized version of Bubble Sort
void bubbleSort(int arr[], int n)
{
    int i, j;
    bool swapped;
    for (i = 0; i < n - 1; i++) {
        swapped = false;
        for (j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                swap(arr[j], arr[j + 1]);
                swapped = true;
            }
        }
 
        // If no two elements were swapped
        // by inner loop, then break
        if (swapped == false)
            break;
    }
}
 
// Function to print an array
void printArray(int arr[], int size)
{
    int i;
    for (i = 0; i < size; i++)
        cout << " " << arr[i];
}
 
// Driver program to test above functions
int main()
{
    int arr[] = { 64, 34, 25, 12, 22, 11, 90 };
    int N = sizeof(arr) / sizeof(arr[0]);
    bubbleSort(arr, N);
    cout << "Sorted array: \n";
    printArray(arr, N);
    return 0;
}
// This code is contributed by shivanisinghss2110
```
![0415_001](https://github.com/sofigrv13/M-todos-de-Ordenamiento-de-Algoritmos/assets/119021332/777b07ef-b4ad-4a81-a537-ec30c632e86e)


- #### Insertion Sort

  En el metodo de inserción el arreglo es virtualmenete dividido en una parte clasificada y otra sin clasificar. Los valores de la parte no clasificada son tomados y puestos en la posición correcta de la parte clasificada. 
 
###### Implementación de Insertion Sort en C++

```C++
// C++ program for insertion sort
 
#include <bits/stdc++.h>
using namespace std;
 
// Function to sort an array using
// insertion sort
void insertionSort(int arr[], int n)
{
    int i, key, j;
    for (i = 1; i < n; i++) {
        key = arr[i];
        j = i - 1;
 
        // Move elements of arr[0..i-1],
        // that are greater than key,
        // to one position ahead of their
        // current position
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}
 
// A utility function to print an array
// of size n
void printArray(int arr[], int n)
{
    int i;
    for (i = 0; i < n; i++)
        cout << arr[i] << " ";
    cout << endl;
}
 
// Driver code
int main()
{
    int arr[] = { 12, 11, 13, 5, 6 };
    int N = sizeof(arr) / sizeof(arr[0]);
 
    insertionSort(arr, N);
    printArray(arr, N);
 
    return 0;
}
// This is code is contributed by rathbhupendra
```
![0415_002](https://github.com/sofigrv13/M-todos-de-Ordenamiento-de-Algoritmos/assets/119021332/f1b5b6fa-5c69-441f-a4e3-642296aa0fb6)


