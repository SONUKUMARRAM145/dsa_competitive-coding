## Description 
Bubble sort is used to sort arrays using principle of big bubble (whole array) eventually becoming small bubble by filtering big values at end of an array.

## Code  
```cpp

#include<bits/stdc++.h>
using namespace std;
// Bubble Sort Logic
void bubble_sort(int array[],int n){
    // First loop for every element from end to start (Big bubble to small)
for (int i = 0; i < n-1; i++)
{  bool flag=false;
 // Loop to identify big value and swap it till the end so array can be sorted
    for (int j = 0; j < n-i-1; j++)
    {
        if (array[j]>array[j+1])
        {
            flag=true;
            swap(array[j],array[j+1]);
        } 
    }
    if(!flag) break; 
}
return;
}

//Sorting Algorithm Boiler code to take input of array, call the sorting function and print the array.
int main(){
    cout<<"Enter size of array : ";
    int size;
    cin>>size;
    int arr[size];
    for(int i=0;i<size;i++){
        cout<<"Enter element "<<(i+1)<<": ";
        cin>>arr[i];
    }    
    cout<<"Before Sort : "<<endl;
    for(int i=0;i<size;i++){
        cout<<arr[i]<<" ";
    }
    cout<<endl;
    bubble_sort(arr,size);
    cout<<"After sort : "<<endl;
    for(int i=0;i<size;i++){
        cout<<arr[i]<<" ";
    }
    cout<<endl;
return 0;
}

```
## Run Code
https://ide.geeksforgeeks.org/6145db81-118c-4631-a37a-10d806565a6e


## Complexities
### Time complexity   : 
Best Case  : O(n)  
Worst Case : O(n^2) 
### Space complexity  : 
O(1)
