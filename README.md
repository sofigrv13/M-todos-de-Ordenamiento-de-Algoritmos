## Metodos de Ordenamiento de Algoritmos

En C++ es un concepto en donde los elementos de un arreglo son re-ordenados en un orden lógico. Este orden puede ir desde el más bajo al más alto y viceversa. El operador de comparación es utilizado para decidir el nuevo orden de elementos en la respectiva estructura de datos.

- #### Selection Sort
Este funciona seleccionando repetidamente el elemento más pequeño (o más grande) de la porción sin clasificar de la lista y moviéndola a la lista clasificada.

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



