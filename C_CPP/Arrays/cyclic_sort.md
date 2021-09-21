# What is Cycle Sort?

## Cyclic Sort is a comparision sorting algoritm which factored array to be factored into a number of cycles where each of them can be rotated to produce a sorted array.

### C++ Code
```
#include<bits/stdc++.h>
using namespace std;

void cyclic_sort(int n,int arr[]){
    int k=0;
    while(k<n){
        int correct=arr[k]-1;
        if(arr[correct]!=arr[k]){
            swap(arr[correct],arr[k]);
        }else{
            k++;
        }
    }
}
int main(){
  int n;
  cin>>n;
  int arr[n];
  for(int i=0;i<n;i++){
      cin>>arr[i];
  }
  cyclic_sort(n,arr);
  for(int i:arr)cout<<i<<" ";
return 0;
}
```
### Limitations of cyclic sort:
Cannot be used if the array is discontinuous
